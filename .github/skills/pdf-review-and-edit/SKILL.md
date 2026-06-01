---
name: pdf-review-and-edit
description: "Reviews and edits PDF-originated content from pasted or extracted text. Use when checking PDF reports, contracts, briefs, forms, audit packets, exported documents, formatting notes, correction requests, or review comments without directly editing PDF binaries by default."
---

## Purpose

Help a Delivery Lead review PDF-originated content and produce edit instructions, revised source text, or a correction checklist while keeping binary PDF editing optional.

## When to use this skill

Use this skill when the user asks for:

- PDF review
- PDF edit plan
- PDF-originated text rewrite
- audit packet review
- exported report correction
- PDF QA checklist
- review comments for a PDF

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- pasted or extracted PDF text
- page/section references if available
- review objective and audience
- known source document if the PDF was generated from Word/Markdown/HTML
- formatting or compliance constraints

## Process

1. Clarify whether the user needs content edits, formatting QA, source-document corrections, or a PDF correction checklist.
2. Review pasted/extracted text for clarity, consistency, factual claims, missing sections, and sensitive data.
3. Prefer editing the source document when known rather than treating the PDF as the primary editing surface.
4. Provide page/section-specific corrections when references are available.
5. Separate content edits from layout/export issues.
6. Keep direct PDF binary editing tools optional and outside the default skill path.

## Output format

```markdown
# PDF Review and Edit Plan — <Document Title>

## Review objective

## Source / page references

## Summary of findings

## Content corrections

| Page / section | Issue | Recommended edit | Reason |
|---|---|---|---|
|  |  |  |  |

## Formatting / export issues

## Sensitive-data or metadata concerns

## Revised source text

## Final PDF QA checklist
```

## Quality checklist

- Edits are tied to page/section references when available.
- Content and formatting issues are separated.
- Source-first correction is preferred.
- Sensitive data and metadata are considered.
- Direct PDF editing is not assumed.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
