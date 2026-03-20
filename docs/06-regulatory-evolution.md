> **Disclaimer:** This document is for informational purposes only and does not constitute legal advice. See [full disclaimer](../DISCLAIMER.md).

# 6. Ongoing Regulatory Developments

This section covers legislative and regulatory developments that are not yet in force but may significantly affect compliance in the coming months and years. Information is current as of March 2026.

## 6.1 Digital Omnibus Package (European Commission, November 2025)

**Status:** Legislative proposal. Not yet in force. Optimistically, adoption by end of 2026, entry into force in 2027.

The Digital Omnibus Package proposes substantial changes to the rules on cookies and consent:

1. **Legitimate interest for analytics cookies**: controllers may be able to rely on legitimate interest (Art. 6(1)(f) GDPR) as the legal basis for analytics and measurement cookies, without requiring prior consent, provided data is processed in aggregate and privacy-preserving form.
2. **Automated browser signals**: users will transmit privacy preferences through machine-readable signals from the browser or operating system. Websites will be required to honour these signals without prompting manual interaction with a consent banner.
3. **Media exemption**: publishers and news platforms will be permitted to disregard automatic do-not-track signals in order to preserve personalised advertising models.
4. **Mandatory one-click "Reject" button**: parity between acceptance and rejection must be enforced.
5. **Aggregate statistics without consent**: usage analysis in aggregated and anonymised form will be permitted without consent.

**Source:** [Digital Omnibus Proposal — European Commission, 19 November 2025](https://digital-strategy.ec.europa.eu/en/library/digital-omnibus-regulation-proposal); Analysis: [Kennedys Law](https://www.kennedyslaw.com/en/thought-leadership/article/2026/the-2025-european-commission-eu-digital-omnibus-package-the-e-privacy-directive/)

**Practical impact:** If adopted, the proposal could significantly reduce the obligation to obtain consent for basic analytics, while increasing technical requirements (browser signal support). Until final adoption, the current framework — the ePrivacy Directive and the GDPR — remains fully in force and must be complied with in its entirety.

---

## 6.2 Growing Enforcement Across Europe (2025–2026)

European supervisory authorities have significantly stepped up enforcement activity on cookie banners in 2025–2026.

- **France (CNIL)**: fined Google €150 million (€90M to Google LLC + €60M to Google Ireland Limited, decision SAN-2021-023 of 31 December 2021) for making cookie rejection disproportionately difficult compared to acceptance (accept: 1 click; reject: at least 5 steps).
- **Sweden (IMY)**: issued an order requiring equal visual prominence between accept and reject buttons.
- **Austria**: the Supreme Court ruled in 2025 that a coloured "Accept" button paired with a faded grey "Reject" link violates GDPR parity requirements.

**Practical impact:** Enforcement risk is real and growing. A banner that is formally compliant on paper is no longer sufficient — the design must be substantively fair and free of dark patterns.

---

## 6.3 AI Act — Regulation (EU) 2024/1689

**Status:** Published on 12 July 2024. Phased entry into force:
- **2 February 2025**: prohibitions on unacceptable-risk AI systems (Art. 5)
- **2 August 2025**: obligations for general-purpose AI models (Chapter V)
- **2 August 2026**: full application of high-risk AI system obligations and transparency obligations (Art. 50)

The AI Act introduces transparency obligations that directly affect privacy notices for websites and services using AI:

1. **Art. 50(1) — AI interaction disclosure**: providers must inform users when they are interacting with an AI system (chatbots, virtual assistants, AI-powered customer service). This requires either a notice in the privacy policy or a just-in-time disclosure in the interface.
2. **Art. 50(2) — AI-generated content marking**: synthetic content (text, images, audio, video) must be marked as AI-generated in a machine-readable format.
3. **Art. 26(11) — High-risk AI deployer obligations**: deployers of high-risk AI (Annex III) that make decisions or assist in making decisions related to natural persons must inform those persons that they are subject to a high-risk AI system. Combined with Art. 22 GDPR, this creates a dual transparency obligation.
4. **Art. 86 — Right to explanation**: affected persons have the right to clear explanations of AI-assisted decisions.

**Interaction with GDPR:** The AI Act and GDPR apply cumulatively. Art. 2(7) AI Act explicitly states that the regulation is "without prejudice to" the GDPR. This means:
- AI transparency obligations under Art. 50 do not replace GDPR obligations under Art. 13–14 and Art. 22 — both must be satisfied
- DPIAs under Art. 35 GDPR are required for high-risk AI systems that process personal data
- The right to explanation (Art. 86 AI Act) complements the GDPR right to "meaningful information about the logic involved" (Art. 13(2)(f) / Art. 15(1)(h))

**Source:** [Regulation (EU) 2024/1689 — Official text](https://eur-lex.europa.eu/eli/reg/2024/1689/oj)

**Practical impact:** Websites using AI-powered features (chatbots, recommendation engines, automated moderation, dynamic pricing, AI-generated content) must update their privacy notices to include AI Act disclosures by 2 August 2026. It is recommended to begin adapting privacy notices in advance, as GDPR obligations on automated decision-making (Art. 22) already require much of this transparency.

---

## 6.4 NIS2 Directive — Directive (EU) 2022/2555

**Status:** In force. National transposition deadline: 17 October 2024. Most Member States have transposed or are in the process of transposing.

The NIS2 Directive on cybersecurity significantly expands the scope of cybersecurity obligations to include a wide range of "essential" and "important" entities across sectors including digital infrastructure, ICT service management, and digital providers.

**Relevance to privacy notices:** NIS2 does not directly impose privacy notice obligations, but it affects GDPR compliance in the following ways:
- **Incident notification**: NIS2 requires notification of significant cybersecurity incidents to the competent authority within 24 hours (early warning) and 72 hours (full notification). If the incident involves a personal data breach, the GDPR 72-hour notification under Art. 33 also applies — both obligations run in parallel.
- **Security measures**: NIS2 mandates risk-based cybersecurity measures (Art. 21) that overlap with GDPR Art. 32 security obligations. The security measures described in the privacy notice (see Section 4.42) should reflect NIS2 compliance where applicable.
- **Supply chain security**: NIS2 requires entities to assess cybersecurity risks in their supply chains, which aligns with GDPR Art. 28 processor due diligence.

**Source:** [Directive (EU) 2022/2555 — Official text](https://eur-lex.europa.eu/eli/dir/2022/2555/oj)

**Practical impact:** Entities subject to NIS2 should ensure that their privacy notices and security disclosures reflect the enhanced cybersecurity posture required by NIS2, and that incident response procedures cover both NIS2 and GDPR notification obligations.

---
