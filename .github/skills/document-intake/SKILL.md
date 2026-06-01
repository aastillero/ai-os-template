---
name: document-intake
description: "Intakes pasted or extracted documents. Use when summarizing a project document, requirements note, brief, policy, contract excerpt, meeting artifact, PDF text, Word text, or long stakeholder document into delivery-relevant facts, risks, decisions, actions, and questions."
---

## Purpose

Help a Delivery Lead turn a long or messy document into structured delivery context without needing OCR, document parsing tools, or live integrations.

## When to use this skill

Use this skill when the user asks for:

- document summary or intake
- requirements or brief review
- contract or policy excerpt review
- PDF or Word text that has already been pasted or extracted
- document-to-actions conversion
- finding risks, decisions, owners, dates, and open questions in a document

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- the pasted/extracted document text
- the document title, source, and date if known
- the intended audience or decision context
- `projects/<project-name>/context/project-brief.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`

## Process

1. Identify document type, source, date, audience, and stated purpose.
2. Extract delivery-relevant facts: scope, dates, owners, commitments, constraints, decisions, risks, issues, dependencies, and acceptance criteria.
3. Separate explicit statements from inferred implications.
4. Flag contradictions, missing context, stale information, and unclear ownership.
5. Convert useful findings into actions, RAID items, decisions, and follow-up questions.
6. If the document appears sensitive, minimize quoted content and summarize only what is needed.

## Output format

```markdown
# Document Intake — <Document or Topic>

## Source

- Title/source:
- Date/version:
- Provided as: pasted text / extracted text / notes

## Executive summary

## Delivery-relevant facts

| Area | Finding | Evidence / note | Confidence |
|---|---|---|---|
| Scope / Timeline / Owner / Risk / Decision / Dependency |  |  | High / Medium / Low |

## Actions and follow-ups

| Action | Owner | Due / trigger | Source |
|---|---|---|---|
|  |  |  |  |

## RAID candidates

| Type | Item | Impact | Next action |
|---|---|---|---|
| Risk / Assumption / Issue / Dependency |  |  |  |

## Decisions or approvals referenced

## Contradictions / gaps / questions

## Assumptions made
```

## Quality checklist

- Source and date are captured or marked unknown.
- Facts are separated from interpretation.
- Actions have owners/dates only when evidenced.
- Sensitive details are minimized.
- Open questions are specific enough to resolve.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
