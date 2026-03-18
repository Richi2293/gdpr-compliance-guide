# Italy

> **Disclaimer:** This document is for informational purposes only and does not constitute legal advice. See [full disclaimer](../DISCLAIMER.md).

## Overview

- **Data Protection Authority:** Garante per la Protezione dei Dati Personali (Italian Data Protection Authority) — https://www.garanteprivacy.it
- **National Transposition Law:** D.Lgs. 196/2003 (Codice in materia di protezione dei dati personali), as amended by D.Lgs. 101/2018
- **Last Updated:** 2026-03-18

## National Legal Framework

Italy transposed the GDPR through D.Lgs. 101/2018, which amended the existing D.Lgs. 196/2003 (known as the "Codice Privacy" — Privacy Code). Rather than replacing the Codice Privacy entirely, Italy chose to adapt it to the GDPR, retaining several national provisions where the GDPR allows member state derogations. Key areas of national specificity include: the minimum age for digital consent (14 years instead of 16), rights concerning deceased persons' data, direct marketing rules, cookie regulation via Art. 122, and detailed provisions on authorized persons for data processing.

The Garante per la Protezione dei Dati Personali actively issues binding provisions (provvedimenti) that supplement the GDPR and the Codice Privacy with detailed operational requirements — particularly in the area of cookies, consent banners, and online tracking.

---

## DPA Provisions and Guidelines

### Provvedimento 10 June 2021 (doc. web 9677876) — Cookie Guidelines

The most comprehensive Italian-specific guidance on cookies and tracking technologies. Published in the Gazzetta Ufficiale n. 163 on 9 July 2021, it provides detailed requirements for consent banners, cookie policies, and consent management that go beyond the general GDPR framework.

- [Full text on garanteprivacy.it](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876)

Key areas covered: banner components (Sez. 7.1), analytics cookie exemptions (Sez. 7.2), re-prompt rules (Sez. 6.2), fingerprinting classification (Sez. 4), accessibility requirements (Sez. 8), and identifier coding criteria (Sez. 8.2).

### Provvedimento 27 February 2025 (doc. web 10118222) — Banner Enforcement

Clarifies that the consent banner must contain three distinct buttons ("Accept all", "Reject all", "Learn more") with equal graphical prominence. Introduces specific requirements for toggle color coding and consent storage.

- [Full text on garanteprivacy.it](https://www.garanteprivacy.it/web/guest/home/docweb/-/docweb-display/docweb/10118222)

### Provvedimento 4 June 2025 (doc. web 10152729) — Banner Enforcement (Admonishment)

Sanctioned (with an admonishment) a website for: (a) banner re-appearing after every visit when closed with the X button, (b) privacy notice containing references to repealed laws, and (c) missing warning that closing with X maintains default settings.

- [Full text on garanteprivacy.it](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10152729)

These enforcement actions confirm that the Garante is actively monitoring website compliance and that even formal violations can result in injunctions and admonishments.

---

## National Case Law

### LG München I — Google Fonts Ruling (20 January 2022, Az. 3 O 17493/20)

Although a German ruling (Landgericht München I), this decision is highly relevant to Italian practice. The court held that loading Google Fonts from external servers (fonts.googleapis.com) is unlawful because it transmits the user's IP address to Google without a valid legal basis. Damages of EUR 100 were awarded for violation of the right to informational self-determination. The Garante's enforcement approach is consistent with this ruling, and self-hosting of static third-party resources is the recommended practice in Italy. See also [requirement 1.10](../docs/01-legal-framework.md) in the EU-wide requirements.

### CJEU C-673/17 (Planet49) — Pre-ticked Checkboxes

The CJEU ruling of 1 October 2019 establishing that pre-ticked checkboxes do not constitute valid consent is directly applied by the Garante in its 2021 Cookie Guidelines (Sez. 7.1). See also [requirement 2.9](../docs/02-consent-banner.md) in the EU-wide requirements.

---

## Country-Specific Requirements

### IT-1 National Cookie Regulation (Art. 122 D.Lgs. 196/2003)

**Requirement:** The storage of information on a user's terminal equipment, or access to information already stored, is only permitted if the user has given consent after receiving clear and complete information pursuant to Art. 13 GDPR. Exempt from consent are only technical operations strictly necessary for the transmission of a communication over a network, or those strictly necessary to provide a service explicitly requested by the user.

**Source:** [Art. 122, comma 1, D.Lgs. 196/2003](https://www.normattiva.it/uri-res/N2Ls?urn:nir:stato:decreto.legislativo:2003-06-30;196) — Italian transposition of Art. 5(3) of the ePrivacy Directive 2002/58/EC.

**Notes:** Art. 122 is the Italian-specific legal basis for cookie consent requirements. While the underlying obligation comes from the ePrivacy Directive, this national transposition provides the enforceable legal reference in Italy. See also [section 2.2](../docs/02-consent-banner.md) and [section 2.3](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-2 Direct Marketing Rules (Art. 130 D.Lgs. 196/2003)

**Requirement:** Direct marketing via email, SMS, or fax requires the user's prior consent. Exception ("soft spam"): the data controller may send commercial communications for products/services similar to those already purchased by the customer, without consent, provided the customer is informed of the right to object.

**Source:** [Art. 130, commi 1-2 and 4, D.Lgs. 196/2003](https://www.normattiva.it/uri-res/N2Ls?urn:nir:stato:decreto.legislativo:2003-06-30;196).

**Notes:** The privacy notice must specify: (a) whether data will be used for marketing, (b) the legal basis (consent or soft spam exception), (c) the unconditional right to object to direct marketing. The right to object to marketing must be presented clearly and separately (Art. 21(4) GDPR). See also [section 4.28](../docs/04-privacy-policy.md) in the EU-wide requirements.

---

### IT-3 Minimum Age for Digital Consent (Art. 2-quinquies D.Lgs. 196/2003)

**Requirement:** In Italy, a minor who has reached the age of 14 may give consent to the processing of their personal data in relation to information society services. Below 14 years of age, consent must be given by the person exercising parental responsibility.

**Source:** [Art. 2-quinquies D.Lgs. 196/2003](https://www.normattiva.it/uri-res/N2Ls?urn:nir:stato:decreto.legislativo:2003-06-30;196) — Italian implementation of Art. 8 GDPR, setting the threshold at 14 instead of the GDPR default of 16.

**Notes:** The data controller must adopt "reasonable measures" to verify that the consent of a minor under 14 is actually given by the person exercising parental responsibility, taking into account available technology (Art. 2-quinquies, comma 2). If the website/service is aimed at minors, the privacy notice must use particularly clear, simple, concise, and comprehensive language. See also [section 4.26](../docs/04-privacy-policy.md) in the EU-wide requirements.

---

### IT-4 Data of Deceased Persons (Art. 2-terdecies D.Lgs. 196/2003)

**Requirement:** The rights under Arts. 15-22 GDPR relating to deceased persons may be exercised by anyone with a legitimate interest, by mandataries, or for family reasons deserving protection. The data subject may expressly prohibit such exercise by written declaration.

**Source:** [Art. 2-terdecies D.Lgs. 196/2003](https://www.normattiva.it/uri-res/N2Ls?urn:nir:stato:decreto.legislativo:2003-06-30;196).

**Notes:** This is an Italy-specific provision with no direct EU equivalent. It is relevant if the service manages data that could outlive the data subject (user accounts, long-term personal data). If not applicable to the specific service, it may be omitted from the privacy notice. See also [section 4.27](../docs/04-privacy-policy.md) in the EU-wide requirements.

---

### IT-5 Mandatory Banner Components (Provvedimento Garante 2021, Sez. 7.1)

**Requirement:** The consent banner must contain all of the following components:
1. A warning that closing the banner via the X button maintains default settings (no tracking)
2. A brief notice indicating: (a) the site uses technical cookies, (b) it may use profiling cookies or other tracking tools subject to consent, (c) the specific purposes of non-technical cookies (e.g., behavioral advertising, service personalization, behavioral analysis)
3. A link to the extended cookie policy (second layer), accessible with a single click
4. A command to accept all cookies
5. A link to the granular selection area (customization by category and/or individual third party)
6. An X button in the top right corner to close the banner

**Source:** [Provvedimento Garante 10 June 2021, Sez. 7.1 (points i-v)](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876).

**Notes:** The banner must have adequate dimensions to create a "perceivable discontinuity" in the page content. Dimensions must be evaluated across different device types (mobile, tablet, desktop) and must avoid the risk of unintended or unconscious user actions. See also [section 2.4](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-6 Three-Button Banner Requirement (Provvedimento Garante 2025)

**Requirement:** The consent banner must contain three distinct buttons — "Accept all" (Accetta tutti), "Reject all" (Rifiuta tutti), and "Learn more" (Scopri di più) — with equal graphical prominence. No button may be visually dominant over the others.

**Source:** [Provvedimento Garante 27 February 2025 (doc. web 10118222)](https://www.garanteprivacy.it/web/guest/home/docweb/-/docweb-display/docweb/10118222).

**Notes:** This 2025 provision clarified that while the 2021 Guidelines envisaged the X button as the primary rejection mechanism, an explicit "Reject all" button is effectively required to ensure parity between acceptance and rejection. It is strongly recommended to include both the X button and an explicit "Reject all" button with equal graphical emphasis. See also [section 2.6](../docs/02-consent-banner.md) and [section 2.7](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-7 Toggle Color Coding (Provvedimento Garante 2025)

**Requirement:** In the granular selection area, toggle switches must follow a specific color coding: green for necessary/non-modifiable cookies, grey for optional/modifiable cookies. All optional toggles must be pre-set to off (rejection) by default.

**Source:** [Provvedimento Garante 27 February 2025 (doc. web 10118222)](https://www.garanteprivacy.it/web/guest/home/docweb/-/docweb-display/docweb/10118222).

**Notes:** The green color for necessary cookies signals that they are always active and cannot be disabled. The grey color for optional cookies signals that they are inactive by default and require user action to enable. This reinforces the privacy-by-default principle (Recital 32 GDPR, CJEU C-673/17 Planet49). See also [section 2.9](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-8 Consent Storage Obligation (Provvedimento Garante 2025)

**Requirement:** The data controller must store the user's consent choice to avoid re-presenting the banner at every visit. The consent storage mechanism (technical cookie or equivalent) must persist the choice reliably.

**Source:** [Provvedimento Garante 27 February 2025 (doc. web 10118222)](https://www.garanteprivacy.it/web/guest/home/docweb/-/docweb-display/docweb/10118222); [Provvedimento Garante 2021, Sez. 7.1](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876).

**Notes:** The consent storage cookie is classified as a technical cookie (strictly necessary) and does not require consent itself. It should be configured with appropriate security attributes: `Secure`, `SameSite=Lax` or `SameSite=Strict`, and a duration consistent with the 6-month re-prompt period (see IT-10). See also [section 2.22](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-9 Analytics Cookie Exemption Conditions (Provvedimento Garante 2021, Sez. 7.2)

**Requirement:** Analytics cookies may be treated as technical cookies (exempt from consent) only if ALL of the following conditions are met:
1. IP address masked: at least the last octet for IPv4 (uncertainty of 1/256, approximately 0.4%), equivalent procedures for IPv6
2. Limited to a single site/app (no cross-site tracking)
3. Only aggregate statistics
4. Third parties must not combine masked data with other datasets
5. Third parties must not transmit data to further third parties
6. Conditions 1-5 must be guaranteed by contractual obligations between the controller and the third-party analytics provider (DPA under Art. 28 GDPR or specific contractual clauses)

**Source:** [Provvedimento Garante 2021, Sez. 7.2](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876); [Provvedimento Garante 2014 (doc. web 3118884)](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/3118884).

**Notes:** If even one condition is not met, analytics cookies require consent like any other non-technical cookie. The objective is to prevent "singling out" (direct identification of the data subject). Exception: analysis across multiple domains, websites, or apps belonging to the same publisher or business group is permitted, provided the statistical analysis is conducted by the controller itself and does not assume characteristics of processing for commercial decisions. See also [section 2.19](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-10 Re-prompt Rules (Provvedimento Garante 2021, Sez. 6.2)

**Requirement:** The consent banner may be re-presented only in three cases:
1. The processing conditions have significantly changed (e.g., new third parties, new purposes)
2. The controller cannot verify whether the consent storage cookie is still present (the user deleted it)
3. At least 6 months have elapsed since the previous banner presentation

**Source:** [Provvedimento Garante 2021, Sez. 6.2](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876).

**Notes:** Excessive re-presentation of the banner is considered an autonomous ground of unlawfulness: "the excessive re-presentation of the banner when the user has previously refused appears liable to impair their freedom" by inducing consent for the sole purpose of continuing navigation (anti-consent-fatigue principle). The system must prevent re-prompt before 6 months if the user has made a choice. See also [section 2.14](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-11 Enforcement: Re-appearing Banner After X Closure (Provvedimento Garante 2025)

**Requirement:** A banner that re-appears at every visit after the user has closed it with the X button is non-compliant. The X closure must be treated as a valid user choice (maintaining default settings with no tracking) and must be persisted.

**Source:** [Provvedimento Garante 4 June 2025 (doc. web 10152729)](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10152729).

**Notes:** The Garante sanctioned this behavior with an admonishment, confirming that the re-prompt rules (IT-10) apply also when the user closes the banner via the X button. See also IT-8 on consent storage obligation.

---

### IT-12 Enforcement: Outdated Legal References in Privacy Notices (Provvedimento Garante 2025)

**Requirement:** Privacy notices must not contain references to repealed laws or outdated legal provisions. All legal references must reflect the current regulatory framework.

**Source:** [Provvedimento Garante 4 June 2025 (doc. web 10152729)](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10152729).

**Notes:** The Garante sanctioned a website that still referenced repealed provisions. This reinforces the obligation to keep privacy notices up to date and accurate, as part of the transparency principle (Art. 5(1)(a) GDPR) and the accountability principle (Art. 5(2) GDPR).

---

### IT-13 Enforcement: Missing X-Closure Warning (Provvedimento Garante 2025)

**Requirement:** The consent banner must include a warning informing the user that closing the banner via the X button maintains the default settings (no tracking cookies installed).

**Source:** [Provvedimento Garante 4 June 2025 (doc. web 10152729)](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10152729); [Provvedimento Garante 2021, Sez. 7.1 (point i)](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876).

**Notes:** The absence of this warning was one of the grounds for the 2025 admonishment. This requirement was already present in the 2021 Guidelines but the 2025 enforcement action confirms it is actively monitored. See also IT-5 on mandatory banner components.

---

### IT-14 Fingerprinting Classification (Provvedimento Garante 2021, Sez. 4)

**Requirement:** Browser/device fingerprinting and any passive identification technique (canvas fingerprinting, audio fingerprinting, font enumeration, WebGL fingerprinting) are classified as equivalent to non-technical cookies and require the user's prior consent.

**Source:** [Provvedimento Garante 2021, Sez. 4](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876); Art. 5(3) ePrivacy Directive.

**Notes:** The Garante (Sez. 4) expressly includes fingerprinting among "other tracking tools" (altri strumenti di tracciamento) subject to the same rules as cookies. Unlike cookies, fingerprinting does not store information on the device but reads it — however, Art. 5(3) ePrivacy covers both storage and access to information already present on the terminal. Preventive blocking applies fully. See also [section 2.27](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-15 Accessibility Requirements for Banner and Notices (Provvedimento Garante 2021, Sez. 8)

**Requirement:** The consent banner and all consent mechanisms must comply with accessibility requirements and be usable through assistive technologies without discrimination.

**Source:** [Provvedimento Garante 2021, Sez. 8](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876); Legge 9 gennaio 2004, n. 4 (Legge Stanca — Law on Accessibility of IT Tools); Directive (EU) 2019/882 (European Accessibility Act), applicable from 28 June 2025.

**Notes:** The Legge Stanca (Law 4/2004) is the Italian accessibility law, originally targeting public administration and later extended to large enterprises. Since 28 June 2025, the European Accessibility Act (transposed in Italy by D.Lgs. 82/2022) extends accessibility requirements to all digital services for consumers, including consent banners and privacy notices. The reference standard is EN 301 549 v3.2.1 (harmonized with WCAG 2.1 level AA). The Garante (Sez. 8) also provides for the possibility of delivering information through multiple channels and modalities: video, informational pop-ups, voice interactions, virtual assistants, chatbots, and telephone. See also [section 2.23](../docs/02-consent-banner.md) in the EU-wide requirements.

---

### IT-16 Identifier Coding Criteria (Provvedimento Garante 2021, Sez. 8.2)

**Requirement:** The cookie policy must classify the cookies used into distinct categories, making the coding criteria adopted for each category manifest. The identifier coding criteria must be made explicit in the privacy notice and provided to the Garante upon request.

**Source:** [Provvedimento Garante 2021, Sez. 8.2](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9677876).

**Notes:** Minimum categories are: (1) technical/necessary cookies, (2) analytics cookies (specifying whether treated as technical or subject to consent), (3) profiling/marketing cookies. The controller must enable the user to distinguish between categories. In the granular selection area, users must be able to select by category and, where applicable, by individual third party. See also [section 3.6](../docs/03-cookie-policy.md) in the EU-wide requirements.

---

### IT-17 Authorized Persons for Data Processing (Art. 2-quaterdecies D.Lgs. 196/2003)

**Requirement:** Persons who process personal data under the direct authority of the controller (employees, collaborators, interns) must be formally authorized for the processing and instructed on the permitted operations.

**Source:** [Art. 2-quaterdecies D.Lgs. 196/2003](https://www.normattiva.it/uri-res/N2Ls?urn:nir:stato:decreto.legislativo:2003-06-30;196); Art. 29 GDPR.

**Notes:** Art. 2-quaterdecies is an Italy-specific provision that implements Art. 29 GDPR in greater detail. The controller must: (a) formally designate authorized persons in writing, (b) define the scope of processing permitted for each authorized person (least privilege principle), (c) provide documented operational instructions, (d) ensure periodic training on data protection. Relevant for websites managed by teams: every team member who accesses users' personal data (e.g., emails from contact forms, CRM data, analytics) must be formally authorized. See also [section 5.7](../docs/05-controller-obligations.md) in the EU-wide requirements.

---

### IT-18 Browser-Level Cookie Management Instructions (Art. 122 D.Lgs. 196/2003)

**Requirement:** The cookie policy must provide instructions on how the user can manage cookies at the browser level, with links to the guides of the main browsers.

**Source:** [Art. 122, comma 2, D.Lgs. 196/2003](https://www.normattiva.it/uri-res/N2Ls?urn:nir:stato:decreto.legislativo:2003-06-30;196).

**Notes:** Art. 122(2) provides that consent may be expressed through configurations of computer programs that are easy and clearly usable. Include links to guides for Chrome, Firefox, Safari, Edge, and Opera. Specify that disabling cookies via the browser may impair the functionality of certain site services. See also [section 3.14](../docs/03-cookie-policy.md) in the EU-wide requirements.

---

### IT-19 Complaint to the Garante (Art. 77 GDPR — Italian Authority Details)

**Requirement:** The privacy notice must inform the user of the right to lodge a complaint with the competent supervisory authority. For Italy, the relevant authority is the Garante per la protezione dei dati personali.

**Source:** Art. 13(2)(d) GDPR; Art. 77 GDPR.

**Notes:** Contact details for the Italian DPA: Garante per la protezione dei dati personali — www.garanteprivacy.it — Piazza Venezia 11, 00187 Roma — email: protocollo@gpdp.it — PEC: protocollo@pec.gpdp.it. The data subject may lodge a complaint in the member state of habitual residence, place of work, or place of the alleged infringement. See also [section 3.12](../docs/03-cookie-policy.md) and [section 4.21](../docs/04-privacy-policy.md) in the EU-wide requirements.

---

### IT-20 Double Opt-in for Newsletters (Italian Best Practice)

**Requirement:** For subscription to newsletters and commercial mailing lists, the double opt-in procedure is strongly recommended (and in practice required): (1) the user fills out the form, (2) receives a confirmation email with a link, (3) must click the link to complete the subscription.

**Source:** Art. 7(1) GDPR (burden of proof of consent); [Art. 130, commi 1-2, D.Lgs. 196/2003](https://www.normattiva.it/uri-res/N2Ls?urn:nir:stato:decreto.legislativo:2003-06-30;196); consolidated practice of the Garante.

**Notes:** Double opt-in is not formally mandatory by law, but it is the safest method to demonstrate that consent was actually given by the data subject (and not by a third party who entered their email address). Without double opt-in, the controller may not be able to satisfy the burden of proof under Art. 7(1) GDPR. See also [section 4.29](../docs/04-privacy-policy.md) in the EU-wide requirements.

---

### IT-21 Data Breach Notification to the Garante (Italian Procedure)

**Requirement:** In case of a personal data breach, the controller must notify the Garante within 72 hours of becoming aware of it, unless the breach is unlikely to result in a risk to the rights and freedoms of natural persons.

**Source:** Art. 33 GDPR; Art. 34 GDPR.

**Notes:** For Italy, the notification is submitted through the form available on the Garante's website: [garanteprivacy.it — Data breach notification](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9131436). The controller must maintain an internal data breach register, available to the Garante upon inspection. See also [section 5.4](../docs/05-controller-obligations.md) in the EU-wide requirements.

---

### IT-22 Records of Processing Activities — Garante Template (Art. 30 GDPR)

**Requirement:** The controller must maintain a record of processing activities (ROPA). While the formal obligation under Art. 30(5) GDPR applies to organizations with more than 250 employees, the Italian Garante recommends the ROPA for smaller organizations as well, especially when processing is not occasional.

**Source:** Art. 30 GDPR; Garante simplified ROPA template.

**Notes:** The Garante provides a simplified ROPA template: [garanteprivacy.it — Records of processing activities](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/9047529). In practice, any website that collects data through forms, analytics cookies, or marketing should maintain a ROPA. See also [section 5.2](../docs/05-controller-obligations.md) in the EU-wide requirements.
