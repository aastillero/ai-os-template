---
name: qa-and-acceptance-review
description: "Reviews QA and acceptance readiness. Use when checking acceptance criteria, UAT notes, test evidence, defect summaries, release acceptance, signoff readiness, quality risks, or delivery evidence before marking work complete."
---

## Purpose

Help a Delivery Lead assess whether work has enough QA and acceptance evidence to support completion, release, or stakeholder signoff.

## When to use this skill

Use this skill when the user asks for:

- QA review
- acceptance review
- UAT review
- test evidence check
- definition of done check
- signoff readiness
- quality risk assessment

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- acceptance criteria, user stories, test notes, UAT feedback, defect list, or release evidence
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`

## Process

1. Identify the work item, expected outcome, and acceptance criteria.
2. List available evidence and map it to acceptance criteria.
3. Classify each criterion as Met, Partially met, Not met, or Unknown based on evidence.
4. Surface defects, unresolved questions, and risk acceptance needs.
5. Separate QA completeness from stakeholder/business acceptance.
6. Recommend next actions before signoff or release.

## Output format

```markdown
# QA and Acceptance Review — <Work Item / Release>

## Scope under review

## Acceptance criteria coverage

| Criterion | Evidence | Status | Gap / risk | Next action |
|---|---|---|---|---|
|  |  | Met / Partial / Not met / Unknown |  |  |

## Defects / concerns

## Signoff readiness

Ready / At risk / Blocked / Unknown

## Recommended next actions

## Missing evidence
```

## Quality checklist

- Every acceptance claim maps to evidence.
- QA and business signoff are distinguished.
- Unknowns are not treated as passed.
- Defects and residual risks are visible.
- Next actions are actionable.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
