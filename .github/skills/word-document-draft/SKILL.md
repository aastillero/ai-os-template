---
name: word-document-draft
description: "Drafts Word-ready documents. Use when creating polished Markdown or structured content intended for Word documents, delivery plans, briefs, proposals, reports, governance notes, review packs, or client/stakeholder documents without requiring docx tooling."
---

## Purpose

Help a Delivery Lead draft content that can be pasted into Microsoft Word or converted later, while keeping the default workflow source-first and Markdown-based.

## When to use this skill

Use this skill when the user asks for:

- Word document draft
- docx-ready content
- formal report draft
- delivery brief document
- proposal or governance note
- polished stakeholder document

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- document purpose, audience, and desired length
- source notes or project context
- `projects/<project-name>/context/project-brief.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/work-plan.md`
- `templates/` files if relevant

## Process

1. Clarify document type, audience, purpose, and approval path.
2. Choose a structure appropriate for a Word document: title, summary, sections, tables, appendices, and review notes.
3. Draft in clean Markdown with Word-friendly headings and simple tables.
4. Use placeholders for missing facts rather than inventing them.
5. Add reviewer notes or questions separately from final copy.
6. Keep optional .docx generation outside the default skill path.

## Output format

```markdown
# Word-Ready Document Draft — <Title>

> Intended audience:
> Purpose:
> Status: Draft for review

## Executive summary

## Background

## Current state

## Analysis / key points

## Recommendations / next steps

## Decisions or approvals needed

## Appendix / supporting detail

## Reviewer notes and open questions
```

## Quality checklist

- Draft is source-first Markdown and Word-ready.
- Sections match the document purpose.
- Review notes are separate from final copy.
- Missing facts are marked clearly.
- No binary .docx tooling is required by default.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
