---
name: release-readiness-review
description: "Reviews release readiness. Use when checking go/no-go readiness, launch preparation, release risks, acceptance evidence, QA status, stakeholder signoff, rollout plans, rollback plans, operational readiness, or release decision inputs."
---

## Purpose

Help a Delivery Lead assess whether a release is ready, what evidence supports that view, and what remains before a go/no-go decision.

## When to use this skill

Use this skill when the user asks for:

- release readiness review
- go/no-go prep
- launch readiness
- release risk assessment
- acceptance evidence check
- stakeholder signoff review
- rollback and rollout planning

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`
- `projects/<project-name>/connections/stakeholders.md`
- QA, UAT, acceptance, rollout, rollback, support, or comms evidence provided by the user

## Process

1. Define release scope and intended release date/window if known.
2. Review readiness across scope, QA/acceptance, defects, rollout, rollback, support, documentation, stakeholders, and communications.
3. Classify each area as Ready, At risk, Blocked, or Unknown based on evidence.
4. List blockers and go/no-go decisions without manufacturing approvals.
5. Identify residual risks and contingency actions.
6. Create a concise release decision brief.

## Output format

```markdown
# Release Readiness Review — <Release / Project>

## Release scope

## Readiness summary

Overall: Ready / At risk / Blocked / Unknown

| Area | Status | Evidence | Gap / concern | Owner | Next action |
|---|---|---|---|---|---|
| Scope |  |  |  |  |  |
| QA / acceptance |  |  |  |  |  |
| Defects |  |  |  |  |  |
| Rollout |  |  |  |  |  |
| Rollback |  |  |  |  |  |
| Support / ops |  |  |  |  |  |
| Stakeholder comms |  |  |  |  |  |

## Go/no-go decision inputs

## Residual risks

## Required actions before release

## Missing evidence
```

## Quality checklist

- Readiness labels are evidence-backed.
- Go/no-go decision is not invented.
- Rollback and support are considered.
- Open blockers are explicit.
- Stakeholder signoff is evidenced or marked missing.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
