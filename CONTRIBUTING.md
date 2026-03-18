# Contributing

Thank you for your interest in improving this GDPR compliance guide. Contributions are welcome and encouraged.

## Language

All content must be written in **English**. Legal references (law names, provision titles) should keep their original language where they are proper nouns (e.g., "Garante per la Protezione dei Dati Personali"), with an English translation in parentheses on first use.

## Requirement Format

Every requirement must follow this structure:

```
### X.Y Requirement Title

**Requirement:** Clear, actionable statement of what must be done.

**Source:** Official legal reference with link to the authoritative source.

**Notes:** (Optional) Clarifications, examples, edge cases.
```

## Rules

1. **Mandatory sources** — Every requirement MUST cite its legal source (article, provision, ruling, guideline) with a link to the official text. Requirements without sources will not be accepted.
2. **One requirement per block** — Each `###` block should cover one specific, atomic requirement.
3. **Actionable language** — Use clear, imperative statements. "The consent banner must include..." not "It is recommended to consider..."
4. **EU-wide vs country-specific** — Place EU-level requirements in `docs/`. Place national-specific requirements in `countries/<country>.md`.

## Adding a New Country

1. Copy `countries/_template.md` to `countries/<country-name>.md`
2. Fill in the country-specific information
3. Include only requirements that are specific to that country — do not duplicate EU-wide requirements from `docs/`
4. Use the country prefix for numbering (e.g., `DE-1`, `FR-1`)

## Pull Requests

- **One PR per topic** — Keep changes focused
- **Descriptive title** — e.g., "Add France country-specific requirements" or "Update consent banner requirements for EDPB Guidelines 2024"
- **Explain what and why** — In the PR description, explain what changed and why (e.g., new regulation, correction, clarification)

## Regulatory Updates

When updating content due to regulatory changes:

- Include the **date** of the new regulation/provision/ruling
- Include a **link** to the official document
- Note what changed compared to the previous version

## Build

After modifying content in `docs/` or `countries/`, run the build script to regenerate the full document:

```bash
./scripts/build.sh
```

Include the updated `full/gdpr-compliance-guide.md` in your PR.
