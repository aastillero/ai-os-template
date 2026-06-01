---
name: github-issue-triage
description: "Triages GitHub issue lists from pasted or exported content. Use when reviewing issues, bugs, feature requests, backlog items, labels, priorities, duplicate candidates, blockers, release candidates, stale issues, or sprint planning inputs without requiring GitHub API access."
---

## Purpose

Help a Delivery Lead turn a pasted/exported GitHub issue list into a practical triage summary and action plan without live GitHub integration.

## When to use this skill

Use this skill when the user asks for:

- GitHub issue triage
- issue list review
- bug backlog triage
- feature request triage
- label review
- stale issue review
- release candidate issue review

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- pasted/exported GitHub issue list with title, number, labels, status, age, assignee, milestone, and body where available
- project goals, release targets, and prioritization criteria
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`

## Process

1. Clarify triage objective: sprint planning, release readiness, stale cleanup, severity review, or backlog grooming.
2. Group issues by type, priority, status, milestone, component, and blocker/dependency signals.
3. Flag duplicates, unclear issues, stale items, missing owners, and release blockers.
4. Suggest labels, priority changes, next actions, or stakeholder questions as recommendations only.
5. Do not claim issues were updated unless the user performs the updates externally.
6. Keep live GitHub API or repository automation optional/deferred.

## Output format

```markdown
# GitHub Issue Triage — <Repo / Project>

## Triage objective

## Summary

## Priority groups

| Priority | Issues | Rationale | Recommended action |
|---|---|---|---|
| P0 / P1 / P2 / P3 / Unknown |  |  |  |

## Release blockers

## Duplicate / related candidates

## Stale or unclear issues

## Label / milestone recommendations

## Questions for owners
```

## Quality checklist

- Recommendations are based on pasted/exported issue data.
- No live GitHub updates are implied.
- Priority rationale is explicit.
- Missing issue details are called out.
- Release blockers are separated from ordinary backlog items.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
