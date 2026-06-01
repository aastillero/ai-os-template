---
name: weekly-delivery-review
description: "Runs a weekly delivery review. Use when preparing weekly project reviews, delivery health checks, cadence reviews, stakeholder reporting inputs, project retrospection, risk scans, plan-vs-actual checks, or next-week focus from workspace files."
---

## Purpose

Help a Delivery Lead perform a consistent weekly review across status, plan, risks, dependencies, decisions, and stakeholder communication.

## When to use this skill

Use this skill when the user asks for:

- weekly delivery review
- weekly project health check
- weekly stakeholder reporting prep
- plan-versus-actual review
- weekly risk and dependency scan
- next-week focus planning

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- `cadence/weekly-review.md`
- `projects/<project-name>/cadence/weekly-project-review.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`
- `projects/<project-name>/connections/dependencies.md`

## Process

1. Confirm the review period and project/workstream scope.
2. Compare current status against plan, milestones, and recent commitments.
3. Review risks, blockers, dependencies, decisions, and stakeholder asks.
4. Identify what changed since the previous review, if previous context exists.
5. Summarize next-week focus and decisions/escalations needed.
6. Produce outputs that can feed status updates and stakeholder communications.

## Output format

```markdown
# Weekly Delivery Review — <Project or Workstream> — <Week>

## Health summary

Overall: Green / Amber / Red / Unknown

## What changed this week

## Progress against plan

| Milestone / deliverable | Planned | Current state | Evidence | Concern |
|---|---|---|---|---|
|  |  |  |  |  |

## Risks, blockers, and dependencies

## Decisions needed

## Stakeholder messages needed

## Next-week focus

1.
2.
3.

## Missing inputs / assumptions
```

## Quality checklist

- Review is tied to a period.
- Health label is evidence-backed.
- Plan changes and decision needs are visible.
- Next-week focus is limited and actionable.
- Output can feed a stakeholder update.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
