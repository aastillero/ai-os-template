---
name: linear-board-review
description: "Reviews Linear or similar board exports from pasted content. Use when triaging Linear issues, delivery boards, statuses, cycles, labels, priorities, blockers, stale cards, ownership gaps, release candidates, or planning views without requiring Linear API access."
---

## Purpose

Help a Delivery Lead review a Linear-style board from pasted/exported content and produce a practical delivery triage summary.

## When to use this skill

Use this skill when the user asks for:

- Linear board review
- board triage
- cycle review
- delivery board cleanup
- stale card review
- priority and owner review
- planning view review

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- pasted/exported board data with title, ID, status, priority, assignee, labels, cycle, project, age, and notes where available
- delivery objective and planning horizon
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/dependencies.md`

## Process

1. Clarify review objective: planning, cycle health, stale cleanup, blocker scan, release readiness, or prioritization.
2. Group items by status, priority, age, owner, label, dependency, and release/cycle relevance.
3. Flag blockers, stale items, owner gaps, overloaded columns, unclear next steps, and items needing decision.
4. Recommend board hygiene actions and follow-up questions without claiming to update Linear.
5. Translate board findings into delivery risks, dependencies, and next actions.
6. Keep live Linear API access optional/deferred.

## Output format

```markdown
# Linear Board Review — <Project / Board>

## Review objective

## Board health summary

## Priority findings

| Finding | Items | Impact | Recommended action |
|---|---|---|---|
| Blocker / Stale / Owner gap / Priority issue / Dependency |  |  |  |

## Status / flow observations

## Risks and dependencies

## Board hygiene recommendations

## Questions for owners
```

## Quality checklist

- Findings are based on pasted/exported board data.
- No live Linear updates are implied.
- Blocked/stale/ownerless items are visible.
- Recommendations are specific.
- Board findings map to delivery impact.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
