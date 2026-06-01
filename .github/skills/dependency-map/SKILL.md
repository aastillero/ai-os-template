---
name: dependency-map
description: "Maps delivery dependencies. Use when identifying cross-team dependencies, external blockers, upstream/downstream work, system handoffs, decision dependencies, sequencing risks, or owner gaps from project context."
---

## Purpose

Help a Delivery Lead make dependencies visible so sequencing, ownership, risks, and escalations are easier to manage.

## When to use this skill

Use this skill when the user asks for:

- dependency mapping
- cross-team dependency review
- sequencing review
- blocker analysis
- external team handoff planning
- owner gap review

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- `projects/<project-name>/connections/dependencies.md`
- `projects/<project-name>/connections/stakeholders.md`
- `projects/<project-name>/connections/systems-and-links.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- user-provided dependency notes

## Process

1. List known deliverables, milestones, teams, systems, decisions, and approvals.
2. Identify upstream dependencies, downstream consumers, and two-way coordination points.
3. Classify dependencies by type: team, system, decision, data, environment, release, vendor, or approval.
4. Assess impact, urgency, owner clarity, and escalation path.
5. Highlight critical path items and dependencies without owner/date.
6. Recommend the smallest next action to de-risk each priority dependency.

## Output format

```markdown
# Dependency Map — <Project or Workstream>

## Summary

## Critical dependencies

| Dependency | Type | Needed from | Needed by | Impact if late | Owner | Due / trigger | Next action |
|---|---|---|---|---|---|---|---|
|  | Team / System / Decision / Data / Environment / Release / Vendor / Approval |  |  |  |  |  |  |

## Dependency flow

- Upstream:
- Internal coordination:
- Downstream:

## Owner/date gaps

## Escalations or decisions needed

## Assumptions / missing inputs
```

## Quality checklist

- Critical path dependencies are visible.
- Owners/dates are evidenced or marked missing.
- Dependencies are specific, not generic team names only.
- Next actions are concrete.
- Escalations explain delivery impact.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
