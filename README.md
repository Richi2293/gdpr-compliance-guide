# GDPR Compliance Guide

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

A structured, source-referenced GDPR compliance guide for developers and AI assistants.

> [!WARNING]
> **This is not legal advice.** This guide is for informational and educational purposes only. Always verify requirements with a qualified legal professional before implementation. See [full disclaimer](DISCLAIMER.md).

## What This Is

- A structured collection of GDPR compliance requirements for websites and applications
- Every requirement cites its official legal source for verifiability
- Designed to be useful for both human developers and AI coding assistants
- Focused on EU/EEA with country-specific sections

## What This Is Not

- Legal advice or a substitute for professional legal counsel
- A guarantee of compliance — every implementation context is different
- An exhaustive treatise on data protection law

## Structure

| Path | Description |
|------|-------------|
| [`docs/`](docs/) | EU-wide requirements, organized by topic |
| [`countries/`](countries/) | Country-specific requirements and national provisions |
| [`full/`](full/) | Complete guide assembled into a single file |
| [`scripts/`](scripts/) | Build script for generating the full document |

### EU-Wide Requirements (`docs/`)

1. [Legal Framework](docs/01-legal-framework.md) — Applicable EU regulations and guidelines
2. [Consent Banner](docs/02-consent-banner.md) — Cookie/consent banner requirements
3. [Cookie Policy](docs/03-cookie-policy.md) — Cookie policy content requirements
4. [Privacy Policy](docs/04-privacy-policy.md) — Data protection notice (Art. 13-14 GDPR)
5. [Controller Obligations](docs/05-controller-obligations.md) — Organizational obligations
6. [Regulatory Evolution](docs/06-regulatory-evolution.md) — Ongoing regulatory changes
7. [Technical Checklist](docs/07-technical-checklist.md) — Implementation checklist for developers

## How to Use

### For Developers

Browse the [`docs/`](docs/) directory for EU-wide requirements. Check [`countries/`](countries/) for requirements specific to your country. Use the [technical checklist](docs/07-technical-checklist.md) as a starting point for implementation.

### For AI Assistants

Load [`full/gdpr-compliance-guide.md`](full/gdpr-compliance-guide.md) as context. This single file contains all EU-wide requirements and country-specific content, assembled and ready for reference.

## Country Coverage

| Country | Status | Last Updated |
|---------|--------|-------------|
| [Italy](countries/italy.md) | Complete | 2026-03-18 |

Want to add your country? See [Contributing](CONTRIBUTING.md) and use the [country template](countries/_template.md).

## Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting a pull request.

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](LICENSE).
