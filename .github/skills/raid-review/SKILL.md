---
name: raid-review
description: Reviews delivery risks, assumptions, issues, and dependencies. Use when preparing RAID reviews, risk updates, blocker reviews, dependency checks, escalation notes, delivery health assessments, or mitigation plans from project context.
---

## Purpose

Help a Delivery Lead review RAID items and turn loose risk/blocker notes into actionable delivery management output.

RAID means:

- Risks: uncertain events that may affect delivery.
- Assumptions: beliefs being treated as true but not yet validated.
- Issues: current problems already affecting delivery.
- Dependencies: people, teams, systems, decisions, or dates needed for delivery.

## When to use this skill

Use this skill when the user asks for:

- RAID review
- risk review
- blocker review
- dependency check
- escalation prep
- delivery health review
- mitigation planning

## Inputs to gather

Look for available context in:

- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/dependencies.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/connections/stakeholders.md`
- `templates/risk-entry.md`
- user-provided notes or pasted context

## Process

1. Extract candidate RAID items from the available context.
2. Classify each item as Risk, Assumption, Issue, or Dependency.
3. For each item, identify impact, likelihood or urgency, owner, mitigation, next action, and escalation path when known.
4. Separate active blockers from future risks.
5. Flag missing owners, missing dates, unclear mitigations, and stale items.
6. Prioritize the few items that need immediate Delivery Lead attention.

## Output format

```markdown
# RAID Review — <Project or Workstream>

## Summary

Overall delivery concern: Low / Medium / High / Unknown

Top concerns:
1.
2.
3.

## RAID table

| Type | Item | Impact | Owner | Next action | Due / trigger | Status |
|---|---|---|---|---|---|---|
| Risk / Assumption / Issue / Dependency |  |  |  |  |  |  |

## Escalations or decisions needed

-

## Stale or unclear items

-

## Assumptions / missing inputs

-
```

## Quality checklist

- Every high-priority item has an owner or is flagged as missing one.
- Issues are not mislabeled as risks.
- Dependencies include who/what is depended on.
- Mitigations and next actions are concrete.
- Escalations explain the impact of not acting.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent owners, dates, impacts, decisions, approvals, commitments, or stakeholder positions.
- If a risk is plausible but not evidenced, label it as an assumption or question.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
