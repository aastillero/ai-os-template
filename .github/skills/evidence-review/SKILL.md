---
name: evidence-review
description: "Checks whether delivery claims are evidence-backed. Use when reviewing status claims, completion claims, acceptance claims, release readiness claims, stakeholder updates, audit notes, or project narratives against available files and user-provided evidence."
---

## Purpose

Help a Delivery Lead distinguish supported facts from unsupported claims before reporting, escalating, or approving work.

## When to use this skill

Use this skill when the user asks for:

- evidence review
- claim check
- status evidence check
- completion evidence
- release evidence
- audit-style review
- stakeholder update validation

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- claim, draft, update, or decision being reviewed
- available evidence files or pasted notes
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`

## Process

1. List the claims being made.
2. Find evidence available in repository context or user-provided notes.
3. Classify each claim as Supported, Partially supported, Unsupported, Contradicted, or Unknown.
4. Identify missing evidence and suggested safer wording.
5. Flag high-risk claims involving dates, approvals, signoff, completion, compliance, or stakeholder commitments.
6. Return a concise evidence table plus revised wording where useful.

## Output format

```markdown
# Evidence Review — <Draft / Claim Set>

## Claims reviewed

| Claim | Evidence found | Rating | Risk | Safer wording / next step |
|---|---|---|---|---|
|  |  | Supported / Partial / Unsupported / Contradicted / Unknown | Low / Medium / High |  |

## High-risk unsupported claims

## Evidence gaps

## Suggested revised wording

## Assumptions
```

## Quality checklist

- Claims are explicit and individually rated.
- Evidence source is named or described.
- Unsupported claims get safer wording.
- High-risk claims are flagged.
- Unknown is used when evidence is absent.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
