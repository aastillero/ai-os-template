---
name: word-document-edit
description: "Edits Word document content from pasted or extracted text. Use when improving structure, tone, clarity, consistency, executive readability, stakeholder language, change notes, or review comments for Word-originated documents without directly editing docx binaries by default."
---

## Purpose

Help a Delivery Lead review and rewrite Word-originated content using pasted/extracted text, with actual `.docx` editing kept optional.

## When to use this skill

Use this skill when the user asks for:

- Word document edit
- docx content rewrite
- document review
- tone and clarity pass
- executive readability edit
- stakeholder document cleanup
- review comment response

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- pasted or extracted document text
- editing goal and audience
- style/tone expectations
- sections needing attention
- known constraints, required terms, or approved wording

## Process

1. Identify the document purpose, audience, and requested edit type.
2. Preserve meaning, commitments, and required wording unless the user asks for substantive changes.
3. Improve structure, headings, transitions, clarity, and consistency.
4. Flag factual claims, dates, owners, or approvals that need evidence.
5. Provide either an edit plan, rewritten sections, or a full revised draft depending on the request.
6. Keep direct `.docx` manipulation optional and outside the default workflow.

## Output format

```markdown
# Word Document Edit — <Document Title>

## Edit objective

## Summary of recommended changes

## Issues found

| Area | Issue | Recommendation |
|---|---|---|
|  |  |  |

## Revised content

### <Section heading>

## Fact checks / unresolved questions

## Change notes for reviewer
```

## Quality checklist

- Meaning and commitments are preserved unless intentionally changed.
- Tone matches audience.
- Factual uncertainty is flagged.
- Revised content is easy to paste back into Word.
- Direct binary editing is not assumed.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
