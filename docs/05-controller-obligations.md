> **Disclaimer:** This document is for informational purposes only and does not constitute legal advice. See [full disclaimer](../DISCLAIMER.md).

## 5. Controller Organisational Obligations

This section covers GDPR obligations that go beyond privacy notices and the consent banner, but that are necessary for full compliance.

### 5.1 Data Protection by Design and by Default

**Requirement:** The controller must implement appropriate technical and organisational measures to apply data protection principles from the design stage (by design) and to ensure that, by default, only personal data necessary for each specific purpose are processed (by default).

**Source:** Art. 25 GDPR.

**Notes:** Practical applications for websites: (a) data minimisation in forms (collect only necessary fields), (b) pseudonymisation where possible, (c) privacy-restrictive default settings (cookies off, private profile), (d) privacy impact assessment before integrating new third-party services. The by-default principle is also reflected in consent banner toggles pre-set to refused (see 2.9).

---

### 5.2 Records of Processing Activities (ROPA)

**Requirement:** The controller (and the processor) must maintain a record of processing activities carried out under their responsibility.

**Source:** Art. 30 GDPR.

**Notes:** The record must contain at least: (a) name and contact details of the controller and the DPO, (b) purposes of processing, (c) categories of data subjects and data, (d) categories of recipients, (e) transfers to third countries, (f) envisaged time limits for erasure, (g) description of technical and organisational security measures. The formal obligation applies to organisations with more than 250 employees, although supervisory authorities generally recommend maintaining records even for smaller organisations, particularly where processing is not occasional (Art. 30(5) GDPR). In practice, any website that collects data via forms, analytics cookies, or marketing cookies should maintain records of processing activities.

---

### 5.3 Data Protection Impact Assessment (DPIA)

**Requirement:** The controller must carry out a DPIA prior to processing likely to result in a high risk to the rights and freedoms of natural persons, taking into account the nature, scope, context, and purposes of the processing.

**Source:** Art. 35 GDPR; EDPB Guidelines WP248 rev.01.

**Notes:** A DPIA is mandatory in particular when: (a) profiling with significant effects is carried out, (b) special category data are processed on a large scale, (c) systematic monitoring of a publicly accessible area is performed. For a standard website with only contact forms and analytics cookies, a DPIA is generally not required. It becomes relevant if implementing: behavioural profiling, large-scale remarketing, biometric data collection, or automated processing with legal effects. A DPIA must include: a description of the processing, an assessment of necessity and proportionality, a risk assessment, and mitigation measures.

**Tools:** The French DPA (CNIL) provides an open-source DPIA tool: [PIA — Privacy Impact Assessment tool](https://www.cnil.fr/en/open-source-pia-software-helps-carry-out-data-protection-impact-assessment). The EDPB has published a list of criteria for identifying high-risk processing (WP248 rev.01, Annex) that can be used as a checklist.

---

### 5.4 Personal Data Breach Notification

**Requirement:** In the event of a personal data breach, the controller must: (a) notify the breach to the competent supervisory authority within 72 hours of becoming aware of it, unless the breach is unlikely to result in a risk to the rights of individuals; (b) communicate the breach to the data subject without undue delay where the risk is high.

**Source:** Art. 33 GDPR (notification to the supervisory authority); Art. 34 GDPR (communication to the data subject); EDPB Guidelines 9/2022 on personal data breach notification.

**Notes:** The notification to the supervisory authority must include: (a) the nature of the breach and approximate categories and number of data subjects and records concerned, (b) name and contact details of the DPO, (c) likely consequences of the breach, (d) measures taken or proposed to address the breach. If notification is not made within 72 hours, it must be accompanied by reasons for the delay. The controller must document all breaches (including those not notified) in an internal data breach register, available to the supervisory authority upon request.

---

### 5.5 Appointment and Agreement with Processors

**Requirement:** Where processing is carried out on behalf of the controller by an external party (processor), the relationship must be governed by a contract or other legal act (Data Processing Agreement — DPA) that binds the processor to the controller.

**Source:** Art. 28 GDPR.

**Notes:** The DPA must cover at least: (a) the subject matter and duration of the processing, (b) the nature and purpose of the processing, (c) the type of personal data and categories of data subjects, (d) the obligations and rights of the controller, (e) security measures, (f) authorisation for sub-processors, (g) assistance to the controller for the exercise of data subject rights, (h) deletion or return of data upon termination. Typical processors for a website include: hosting providers (e.g. AWS), email services, CRM systems, analytics services (where the provider acts as a processor rather than an independent controller). Always verify whether the vendor offers a standard DPA and whether it is adequate.

---

### 5.6 Technical and Organisational Security Measures

**Requirement:** The controller and the processor must implement appropriate technical and organisational measures to ensure a level of security appropriate to the risk.

**Source:** Art. 32 GDPR.

**Notes:** Relevant measures for websites: (a) mandatory HTTPS on all pages, (b) encryption of sensitive data at rest and in transit, (c) protection against common attacks (XSS, CSRF, SQL injection), (d) regular updates of frameworks and dependencies, (e) regular backups, (f) access controls to data (principle of least privilege), (g) logging of administrative access. The adequacy of measures must be assessed in relation to the nature, scope, and purposes of the processing.

---

### 5.7 Authorised Persons for Processing (Internal Staff)

**Requirement:** Individuals who process personal data under the direct authority of the controller (employees, collaborators, interns) must be formally authorised to carry out processing and must be provided with instructions regarding permitted operations.

**Source:** Art. 29 GDPR.

**Notes:** The controller must: (a) formally designate authorised persons in writing, (b) define the scope of processing permitted to each authorised person (principle of least privilege), (c) provide documented operational instructions, (d) ensure periodic training on data protection. Relevant for websites managed by a team: every team member who accesses users' personal data (e.g. emails from contact forms, CRM data, analytics) must be formally authorised.

---

### 5.8 API Integrations, Webhooks, and Automated Data Flows

**Requirement:** Every flow of personal data from the website/application to external systems (CRM, email marketing, analytics, third-party services) via APIs, webhooks, or automated integrations must be documented, and each recipient must be identified either as a processor (with a DPA in place) or as an independent controller.

**Source:** Art. 13(1)(e) GDPR (recipients); Art. 28 GDPR (processors); Art. 30 GDPR (records of processing activities).

**Notes:** Typical data flows to verify: (a) contact form → CRM (e.g. HubSpot, Salesforce), (b) newsletter subscription → email marketing platform (e.g. Mailchimp, SendGrid, Brevo), (c) user events → analytics (e.g. GA4 via Measurement Protocol), (d) conversions → advertising platforms (e.g. Meta CAPI, Google Ads API), (e) user data → support services (e.g. Zendesk, Intercom). For each flow, verify: (a) existence of a DPA with the recipient, (b) disclosure in the privacy notice, (c) applicable legal basis, (d) safeguards for non-EEA transfers, (e) security measures in transmission (HTTPS, API authentication, encryption).

---

### 5.9 Infrastructure Services (Hosting, CDN, DNS)

**Requirement:** Infrastructure services that process users' personal data (hosting providers, CDNs, DNS services, WAFs) must be treated as processors and covered by an adequate Data Processing Agreement (DPA).

**Source:** Art. 28 GDPR (processors); Art. 13(1)(e) GDPR (recipients); Art. 44–49 GDPR (international transfers).

**Notes:** Typical infrastructure services and their privacy implications:

| Service | Data processed | Implications |
|---------|----------------|--------------|
| **Hosting** (e.g. AWS Amplify, Vercel, Netlify) | User IP, HTTP headers, access logs, request content | DPA mandatory. Verify server region (data residency). For AWS: accept the [AWS GDPR DPA](https://aws.amazon.com/compliance/gdpr-center/) and configure an EU region (e.g. eu-west-1). |
| **CDN** (e.g. CloudFront, Cloudflare, Fastly) | User IP, approximate geolocation, HTTP headers | The CDN acts as a processor. If the CDN has non-EEA nodes, EU user traffic may transit through servers outside the EEA — verify geo-restriction settings. For Cloudflare: accept the DPA and verify the Data Localisation Suite configuration if required. |
| **DNS** (e.g. Route 53, Cloudflare DNS) | User IP (in DNS queries), requested domain | DNS queries contain the resolver's IP (not always the end user's). If using a DNS resolver with logging, verify the DPA and data retention. For authoritative DNS managed by the provider, verify the DPA as for hosting. |
| **WAF/DDoS protection** (e.g. AWS WAF, Cloudflare) | User IP, HTTP headers, request payloads (potentially containing personal data) | The WAF analyses traffic in real time and may log suspicious requests. Verify that WAF logs comply with data minimisation and limited retention principles. |
| **Transactional email** (e.g. SES, SendGrid, Postmark) | Recipient email address, message content, delivery metadata | DPA mandatory. Verify whether the provider processes email content for its own purposes. |

For each infrastructure service: (a) verify the existence of a valid DPA and confirm its acceptance, (b) declare the provider in the privacy notice as a recipient/processor, (c) verify safeguards for non-EEA transfers (EU–US Data Privacy Framework, SCCs, BCRs), (d) configure data residency in the EU region where possible, (e) configure log data retention to the minimum necessary.

---
