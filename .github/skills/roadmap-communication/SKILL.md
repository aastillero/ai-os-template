---
name: roadmap-communication
description: "Creates roadmap communication drafts. Use when explaining roadmap changes, sequencing, milestones, trade-offs, delays, scope movement, delivery themes, stakeholder impacts, or future-state plans in clear stakeholder language."
---

## Purpose

Help a Delivery Lead communicate roadmap direction and changes without overpromising dates, scope, or certainty.

## When to use this skill

Use this skill when the user asks for:

- roadmap communication
- roadmap update
- scope sequencing explanation
- milestone narrative
- roadmap change message
- delay or trade-off explanation
- future-state stakeholder update

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- roadmap items, milestones, themes, or changes provided by the user
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/decisions.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/stakeholders.md`

## Process

1. Clarify audience, planning horizon, and reason for communication.
2. Separate confirmed roadmap commitments from directional intent.
3. Explain sequencing using value, dependency, risk, capacity, or decision rationale.
4. Highlight stakeholder impact and what is not changing.
5. State uncertainties and next decision points.
6. Produce a reviewable draft with optional shorter variants.

## Output format

```markdown
# Roadmap Communication — <Topic / Period>

## Audience

## Message objective

## Roadmap summary

## What is changing

## What is not changing

## Why this sequence / trade-off

## Stakeholder impact

## Draft message

## Short version

## Questions / approvals needed
```

## Quality checklist

- Confirmed vs tentative items are distinguished.
- Sequencing rationale is understandable.
- No false precision on dates.
- Stakeholder impact is addressed.
- Message has a clear call to action or next update point.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
