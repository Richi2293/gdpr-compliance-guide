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

The [`full/gdpr-compliance-guide.md`](full/gdpr-compliance-guide.md) file (~130 KB) contains all EU-wide requirements and country-specific content assembled into a single file, optimized for loading as AI context.

#### Quick Start

The simplest approach: add the guide to your project and instruct your AI tool to reference it.

**As a git submodule** (recommended — stays in sync with updates):

```bash
git submodule add https://github.com/<owner>/gdpr-compliance-guide.git docs/gdpr
```

Update when needed:

```bash
git submodule update --remote
```

**As a file copy** (simpler, but requires manual updates):

```bash
cp full/gdpr-compliance-guide.md /path/to/your-project/docs/
```

#### AI-Powered IDEs

Most AI-powered editors support project-level instructions that tell the assistant when and how to use reference files.

**Claude Code** — add to your `CLAUDE.md`:

```markdown
## GDPR Compliance
- When implementing features related to cookies, consent, tracking, privacy policies,
  or personal data processing, consult docs/gdpr/full/gdpr-compliance-guide.md
- Use docs/gdpr/docs/07-technical-checklist.md to verify implementations
- Always cite the specific section number and legal source in your explanations
```

**Cursor** — add to your `.cursor/rules/gdpr.mdc`:

```markdown
---
description: GDPR compliance requirements for cookie consent, privacy, and data processing
globs:
alwaysApply: false
---
When working on features involving cookies, consent banners, tracking, privacy policies,
or personal data processing, reference @docs/gdpr/full/gdpr-compliance-guide.md for
requirements and verify against @docs/gdpr/docs/07-technical-checklist.md
```

**GitHub Copilot** — add to your `.github/copilot-instructions.md`:

```markdown
When implementing features related to cookies, consent, tracking, privacy policies,
or personal data processing, consult docs/gdpr/full/gdpr-compliance-guide.md for
compliance requirements.
```

**Other editors** (Windsurf, Cline, etc.) — check your tool's documentation for the equivalent project instructions file and follow the same pattern.

#### Chat Interfaces

**Claude Projects** — upload `full/gdpr-compliance-guide.md` to the project knowledge base. Add to the project instructions: *"Use the GDPR compliance guide as your primary reference. Always cite the specific section and legal source."*

**ChatGPT** — upload `full/gdpr-compliance-guide.md` as a file attachment in a conversation, or add it to a Custom GPT's knowledge base.

**Google Gemini** — upload the file as context in Google AI Studio or attach it in a Gemini conversation.

#### API / Programmatic Usage

Load the guide as part of the system prompt or as a document in the conversation context:

```python
with open("docs/gdpr/full/gdpr-compliance-guide.md") as f:
    gdpr_guide = f.read()

# Use as system context (works with any LLM API)
system_prompt = f"""You are a developer assistant with GDPR compliance expertise.
Use the following guide as your primary reference. Always cite the specific
section number and legal source when providing guidance.

{gdpr_guide}"""
```

For larger projects, consider using the individual files in `docs/` with a RAG (Retrieval-Augmented Generation) pipeline to load only the relevant sections based on the query.

#### Best Practices

- **Full file vs. individual sections** — use `full/gdpr-compliance-guide.md` when you need comprehensive coverage. Use individual files from `docs/` when you only need a specific topic (e.g., just consent banners) or want to save context window space.
- **Keep it updated** — GDPR requirements evolve. If using a submodule, update periodically. If using a copy, check this repository for changes.
- **Always verify** — AI assistants can misinterpret requirements. Cross-check AI-generated implementations against the cited legal sources, and consult a qualified legal professional for your specific context.

## Country Coverage

| Country | Status | Last Updated |
|---------|--------|-------------|
| [Italy](countries/italy.md) | Complete | 2026-03-18 |

Want to add your country? See [Contributing](CONTRIBUTING.md) and use the [country template](countries/_template.md).

## Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting a pull request.

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](LICENSE).
