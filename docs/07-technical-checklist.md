> **Disclaimer:** This document is for informational purposes only and does not constitute legal advice. See [full disclaimer](../DISCLAIMER.md).

## 7. Technical Implementation Checklist

This section provides concrete, actionable technical checks designed to allow a developer (or an AI) to audit and correct GDPR compliance implementation on a website or application. Each item indicates what to verify in the code and which requirement section it satisfies.

### 7.1 Consent Banner — Technical Checks

**Checklist:**

1. **Prior blocking**: verify that no third-party scripts (analytics, marketing, social, session recording) are loaded before consent. Check: `<script>` tags in `<head>` and `<body>`, tag managers (GTM), inline scripts, iframes. → Ref. 2.2
2. **Google Consent Mode v2**: verify that `gtag('consent', 'default', {...})` (or the GTM equivalent) sets all signals to `'denied'`:
   ```javascript
   gtag('consent', 'default', {
     ad_storage: 'denied',
     ad_user_data: 'denied',
     ad_personalization: 'denied',
     analytics_storage: 'denied'
   });
   ```
   The default must be executed BEFORE any `gtag('config', ...)` call or tag loading. → Ref. 2.25
3. **Banner buttons**: verify the presence of three distinct actions: "Accept all", "Reject all", X close button. → Ref. 2.4, 2.5, 2.6
4. **Visual parity**: verify that "Accept all" and "Reject all" have the same size, same visual weight, same element type (both `<button>`, not one `<button>` and one `<a>`), same chromatic emphasis. The X button must have comparable visibility. → Ref. 2.7
5. **X close notice**: verify that the banner contains text informing the user that closing with X keeps the default settings (no tracking). → Ref. 2.4
6. **Cookie policy link**: verify that the banner contains a link to the cookie policy reachable with a single click. → Ref. 2.4
7. **Granular customisation**: verify the presence of a "Customise" link/button that opens a selection area for categories (minimum: technical, analytics, profiling) and optionally per individual third party. → Ref. 2.8
8. **Pre-set toggles**: in the customisation area, verify that all toggles are OFF by default, except technical cookies (ON and non-editable). → Ref. 2.9
9. **Choice persistence**: verify that after consent/rejection, a technical cookie stores the choice and the banner does not reappear. → Ref. 2.22
10. **Re-prompt**: verify that the banner is not shown again before 6 months from the choice, unless conditions change or the cookie is deleted. → Ref. 2.14
11. **"Review your choices" link**: verify the presence in the footer of every page of a link to reopen the consent management panel. → Ref. 2.13
12. **Audit log**: verify that every consent event is recorded with: anonymous identifier, timestamp, event type, choices made, consent version. Anonymised IP. → Ref. 2.15
13. **Accessibility**: verify keyboard navigation (Tab, Enter, Escape), focus trap in modal, ARIA attributes (`role="dialog"`, `aria-label`, `aria-modal="true"`), screen reader support. Verify conformance with EN 301 549 / WCAG 2.1 AA for the European Accessibility Act. → Ref. 2.23, 1.9
14. **Consent cookie security attributes**: verify that the technical cookie storing the choice has: `Secure`, `SameSite=Lax` or `Strict`, duration consistent with 6 months. Verify `HttpOnly` if the cookie does not need to be read by client-side JavaScript. → Ref. 2.22
15. **SEO/CLS impact**: verify that the banner does not cause a Cumulative Layout Shift (CLS) greater than 0.1. Implement as a fixed overlay (`position: fixed`) or reserve space in the layout. Verify that main content is accessible to crawlers without banner interaction. → Ref. 2.34
16. **No manipulative A/B testing**: verify that no A/B tests are active on the banner aimed at optimising the acceptance rate. → Ref. 2.32
17. **Web Storage for tracking**: verify that localStorage, sessionStorage and IndexedDB are not used for tracking/analytics purposes without consent. Check the use of `localStorage.setItem()` and `sessionStorage.setItem()` in JavaScript code. → Ref. 2.35
18. **Email tracking pixels**: if the site sends emails via email marketing platforms (Mailchimp, SendGrid, Brevo, etc.), verify that open and click tracking pixels are declared in the privacy notice and that specific consent is collected. → Ref. 2.36
19. **Push notifications**: if the site implements web push notifications, verify that: (a) an informational pre-prompt is shown before the browser permission prompt, (b) the privacy notice covers the data collected (subscription endpoint, keys), (c) consent can be easily revoked. → Ref. 2.37

---

### 7.2 Prior Blocking — Common Third Parties

For each third-party service, verify that the script/iframe is blocked until user consent.

| Service | Element to block | Notes |
|---------|-----------------|-------|
| Google Analytics 4 | `gtag.js` / `analytics.js` / GTM with GA4 | Consent Mode v2 can manage blocking, but verify default is `denied` |
| Google Tag Manager | `gtm.js` | If GTM loads other tags, blocking GTM cascades to everything. Alternatively, use GTM consent-aware triggering |
| Meta Pixel (Facebook) | `fbevents.js` / `<noscript><img>` pixel | Block both the script and the `<noscript>` tag |
| YouTube embed | `<iframe src="youtube.com/...">` | Replace with placeholder + notice. `youtube-nocookie.com` does not eliminate all cookies |
| Google Maps embed | `<iframe src="google.com/maps/...">` | Replace with static image or placeholder until consent |
| Hotjar / Clarity | `hotjar.js` / `clarity.js` | Full blocking until consent |
| LinkedIn Insight Tag | `snap.licdn.com/li.lms-analytics` | Full blocking until consent |
| TikTok Pixel | `analytics.tiktok.com` | Full blocking until consent |
| Intercom / Zendesk widget | Widget script | If it installs non-technical cookies, requires consent |
| Google Fonts (hosted) | `fonts.googleapis.com` | **Unlawful without legal basis** (LG München judgment, 20.01.2022 — Sec. 1.10). The user's IP is transmitted to Google without technical necessity. Only compliant solution: self-hosting the font files. See Sec. 7.7 |
| reCAPTCHA | `google.com/recaptcha` | Classifiable as technical if strictly necessary for security. However, Google may use the data for its own purposes — consider privacy-friendly alternatives (e.g. hCaptcha, Cloudflare Turnstile) |

→ Ref. 2.2, 2.24

---

### 7.3 Google Analytics 4 — Compliant Configuration

**Checks:**

1. **Consent Mode v2**: default set to `denied` for all 4 signals (see 7.1 item 2). → Ref. 2.25
2. **IP anonymisation**: GA4 anonymises IP by default in the EU (unlike Universal Analytics). Verify that anonymisation settings have not been disabled. → Ref. 2.19
3. **Data retention**: in GA4 settings, set data retention to the minimum necessary (2 months, not 14 months, unless strictly required). → Ref. 3.9
4. **Google Signals**: if enabled, collects cross-device data for users with Google accounts — requires disclosure and specific consent for profiling. → Ref. 2.16
5. **Data Processing Agreement**: verify acceptance of Google's data processing terms for GA4 (Google Data Processing Terms). → Ref. 5.5
6. **Cross-border transfer**: verify that Google operates under the EU-US Data Privacy Framework or that adequate SCCs are in place. Declare the transfer in the privacy notice. → Ref. 3.13, 4.12
7. **User-ID and Client-ID**: if User-ID is used, this data is personal and must be declared in the privacy notice with the relevant legal basis. → Ref. 3.5
8. **Enhanced Measurement**: verify which events are active (page view, scroll, outbound click, site search, video engagement, file download). Each collects potentially personal data. → Ref. 3.5

---

### 7.4 HTML Forms — Technical Requirements

**Checklist for each form on the site:**

1. **Privacy notice link**: presence of a link to the privacy policy visible before the submit button. Recommended format: "I have read the [privacy policy](/privacy-policy)" or equivalent text with link. → Ref. 4.32
2. **Marketing consent checkbox**: if the form collects data for additional purposes (newsletter, marketing), a dedicated checkbox NOT pre-ticked (`<input type="checkbox">` without the `checked` attribute). → Ref. 4.32, 2.9
3. **Separate consents**: distinct checkboxes for different purposes (e.g. one for "response to request", one for "newsletter", one for "third-party commercial communications"). → Ref. 2.16
4. **Required fields**: visual indicator (e.g. asterisk) and `required` attribute only for fields genuinely necessary for the purpose. → Ref. 4.23, 5.1
5. **Data minimisation**: do not request data beyond what the purpose requires (e.g. date of birth on a contact form). → Ref. 5.1
6. **HTTPS**: the form must be submitted over a secure connection (verify the `action` URL and that the entire site is HTTPS). → Ref. 5.6
7. **Double opt-in** (for newsletters): verify that a confirmation email with an activation link is sent. → Ref. 4.29
8. **Honeypot / CAPTCHA**: if present, verify that the CAPTCHA does not install profiling cookies (see table 7.2 for reCAPTCHA). → Ref. 7.2

---

### 7.5 Structure Schema — Cookie Policy

Minimum expected structure for a compliant cookie policy. Can be used to verify the completeness of an existing cookie policy or to generate a new one.

```
1. Title and last updated date                                  → Ref. 3.17
2. Identity and contact details of the controller              → Ref. 3.3
3. DPO contact details (if appointed)                          → Ref. 3.4
4. What cookies are (accessible definition)                    → Ref. 3.15
5. Categories of cookies used                                  → Ref. 3.6
   5a. Technical/necessary cookies                             → Ref. 2.3
   5b. Analytics cookies (specify whether consent required)    → Ref. 2.19
   5c. Profiling/marketing cookies                             → Ref. 3.5
6. Detailed cookie table                                        → Ref. 3.7
   (name, provider, purpose, duration, type)
7. Third-party cookies — list with links to policies           → Ref. 3.8
8. Legal basis for each category                               → Ref. 3.5
9. How to give or withdraw consent                             → Ref. 3.11, 2.12
10. International data transfers                               → Ref. 3.13
11. Data retention period                                      → Ref. 3.9
12. Data subject rights (or reference to the privacy policy)   → Ref. 3.10
13. Right to lodge a complaint with a supervisory authority    → Ref. 3.12
14. Managing cookies via browser — links to guides             → Ref. 3.14
15. Recommended duration by category                           → Ref. 3.20
16. Contact details for exercising rights                      → Ref. 4.37
```

---

### 7.6 Structure Schema — Privacy Policy

Minimum expected structure for a compliant privacy policy. Can be used to verify the completeness of an existing privacy policy or to generate a new one.

```
1. Title and last updated date                                  → Ref. 4.30
2. Identity and contact details of the controller              → Ref. 4.6
3. DPO contact details (if appointed)                          → Ref. 4.7
4. Types of data collected                                     → Ref. 4.40
   4a. Navigation data (server logs, IP)                       → Ref. 4.38
   4b. Voluntarily provided data (forms, registration)
   4c. Data from third parties (social login, if applicable)   → Ref. 4.33
   4d. Data not collected from the data subject (Art. 14)      → Ref. 4.41
5. Processing purposes and legal basis for each                → Ref. 4.8
6. Legitimate interests pursued (if applicable)                → Ref. 4.9
7. Mandatory or optional nature of data provision              → Ref. 4.23
8. Data recipients                                             → Ref. 4.10
   8a. Data processors (with DPA)
   8b. Independent controllers
   8c. General categories
9. International data transfers                                → Ref. 4.12
10. Retention period per purpose                               → Ref. 4.13
11. Data subject rights                                        → Ref. 4.14-4.22
    - Access (Art. 15)
    - Rectification (Art. 16)
    - Erasure (Art. 17)
    - Restriction (Art. 18)
    - Portability (Art. 20)
    - Objection (Art. 21)
    - Withdrawal of consent (Art. 7(3))
    - Automated decisions and profiling (Art. 22)
12. How to exercise rights (contacts, form)                    → Ref. 4.37
13. Right to lodge a complaint with a supervisory authority    → Ref. 4.21
14. Consent of minors (if applicable)                          → Ref. 4.26
    14b. Data of deceased persons (national provisions)        → Ref. 4.27
15. Direct marketing and soft opt-in (if applicable)           → Ref. 4.28
16. Joint controllership (if applicable)                       → Ref. 4.11
17. Security measures                                          → Ref. 4.42, 5.6
18. Infrastructure services (hosting, CDN)                     → Ref. 4.43, 5.9
19. Territorial scope (if relevant)                            → Ref. 4.39
20. Changes to the privacy policy                              → Ref. 4.24
```

---

### 7.7 Self-Hosting of Third-Party Static Resources

Loading static resources from third-party servers (fonts, CSS/JS libraries, icons) transmits the user's IP address to the external server, constituting a transfer of personal data without a valid legal basis in most cases.

**Resources to verify and migrate to self-hosting:**

| Resource | External domain | Action |
|----------|----------------|--------|
| Google Fonts | `fonts.googleapis.com`, `fonts.gstatic.com` | **Mandatory** self-hosting. Download the `.woff2` files and serve them from your own domain. Tools: [google-webfonts-helper](https://gwfh.mranftl.com/fonts) or `fontsource` (npm). → Ref. 1.10 |
| Font Awesome (CDN) | `cdnjs.cloudflare.com`, `use.fontawesome.com` | Recommended self-hosting. Download the files and serve them locally |
| Bootstrap/jQuery (CDN) | `cdn.jsdelivr.net`, `cdnjs.cloudflare.com` | Recommended self-hosting or bundling with your own code. Using public CDNs transmits the IP and `Referer` header to the CDN provider |
| Google reCAPTCHA | `google.com/recaptcha` | Self-hosting is not possible (requires communication with Google servers). Consider privacy-friendly alternatives: **hCaptcha**, **Cloudflare Turnstile**, **Friendly Captcha** — which do not transfer data to Google |
| Gravatar | `gravatar.com` | Transmits email hash and IP to Automattic. Self-host the avatar or use a local placeholder |

**Technical verification:** Check in the site's `<head>` and `<body>` for `<link>`, `<script>` or `<img>` tags pointing to external domains for static resources. Useful tools: the browser DevTools Network panel (filter by domain), or an audit with Lighthouse/WebPageTest.

→ Ref. 1.10, 5.9, 7.2

---

### 7.8 Infrastructure Services — Technical Checks

**Checklist:**

1. **Hosting provider DPA**: verify acceptance of the hosting provider's Data Processing Agreement (e.g. AWS DPA, Vercel DPA, Netlify DPA). The DPA must be formally accepted, not merely "available". → Ref. 5.5, 5.9
2. **Server region**: verify that the infrastructure is configured on EU regions (e.g. `eu-west-1` for AWS). For CDNs with global nodes, verify geo-restriction or data localisation settings. → Ref. 5.9
3. **Log retention**: verify the retention configuration for access logs. Recommendation: max 90 days. Verify CloudWatch, S3 access logs, or equivalent settings. → Ref. 4.38
4. **IP in logs**: verify whether server logs contain full or anonymised IP addresses. If full, document the legal basis and retention period in the privacy notice. → Ref. 4.38
5. **External resources**: perform an audit of resources loaded from external domains (fonts, CDN, JS libraries). Migrate to self-hosting everything that is feasible. → Ref. 7.7
6. **HTTPS**: verify that the entire site is served over HTTPS, with automatic redirect from HTTP. Verify TLS configuration (minimum TLS 1.2, TLS 1.3 recommended). Verify security headers: `Strict-Transport-Security`, `X-Content-Type-Options`, `X-Frame-Options`. → Ref. 5.6
