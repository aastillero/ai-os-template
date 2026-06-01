---
name: pdf-export
description: "Prepares PDF-ready source content and export specs. Use when creating printable Markdown, HTML-ready content, report packaging notes, PDF export checklists, formatting specifications, or handoff instructions for PDF rendering without requiring PDF tooling by default."
---

## Purpose

Help a Delivery Lead prepare content and instructions that can become a PDF through any approved export path, while keeping the core skill tool-neutral.

## When to use this skill

Use this skill when the user asks for:

- PDF export
- PDF-ready source
- printable report
- export checklist
- PDF packaging notes
- formatting specification
- report handoff for rendering

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- source content or desired document outline
- audience and distribution context
- formatting, branding, pagination, accessibility, or compliance constraints
- required sections, appendices, and review path

## Process

1. Clarify whether the user needs content, an export spec, or a QA checklist.
2. Structure content in printable Markdown or HTML-friendly sections.
3. Specify page, heading, table, image, footer, appendix, and accessibility requirements where known.
4. List export steps generically without requiring a specific tool.
5. Add a PDF QA checklist covering completeness, formatting, links, metadata, and sensitive data.
6. Flag unresolved formatting or source-data gaps.

## Output format

```markdown
# PDF Export Package — <Document Title>

## Purpose and audience

## PDF-ready source content

## Export specification

| Area | Requirement | Notes |
|---|---|---|
| Page size / orientation |  |  |
| Headings |  |  |
| Tables |  |  |
| Images / diagrams |  |  |
| Headers / footers |  |  |
| Links |  |  |
| Accessibility |  |  |

## PDF QA checklist

- [ ] Content complete
- [ ] Formatting reviewed
- [ ] Links checked
- [ ] Sensitive data removed
- [ ] Metadata reviewed

## Open questions
```

## Quality checklist

- Output can be rendered by multiple tools.
- Content and export spec are separated.
- PDF QA includes sensitive-data and metadata review.
- No renderer is required by default.
- Formatting gaps are explicit.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
