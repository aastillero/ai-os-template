---
name: scope-change-review
description: "Reviews delivery scope changes. Use when evaluating change requests, new requirements, scope creep, trade-offs, timeline impact, priority shifts, capacity impact, stakeholder implications, or decision options for scope changes."
---

## Purpose

Help a Delivery Lead evaluate proposed scope changes in terms of value, impact, trade-offs, risks, dependencies, and decision path.

## When to use this skill

Use this skill when the user asks for:

- scope change review
- change request
- scope creep analysis
- impact assessment
- trade-off review
- priority shift
- timeline or capacity impact

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- proposed change and rationale
- current scope and plan
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`
- `projects/<project-name>/connections/stakeholders.md`

## Process

1. Restate the proposed change and desired outcome.
2. Compare it to current scope, priorities, and constraints.
3. Assess impact on timeline, capacity, dependencies, quality, risk, stakeholders, and release readiness.
4. Identify options: accept, defer, trade, split, reject, or investigate.
5. Define decision owner, evidence needed, and communication needs.
6. Avoid making the decision unless the user asks for a recommendation.

## Output format

```markdown
# Scope Change Review — <Change>

## Proposed change

## Current baseline

## Impact assessment

| Area | Impact | Evidence / assumption | Concern |
|---|---|---|---|
| Scope |  |  |  |
| Timeline |  |  |  |
| Capacity |  |  |  |
| Dependencies |  |  |  |
| Quality / QA |  |  |  |
| Stakeholders |  |  |  |

## Options

| Option | Pros | Cons / risks | Decision needed |
|---|---|---|---|
| Accept / Defer / Trade / Split / Reject / Investigate |  |  |  |

## Recommendation, if requested

## Questions before decision
```

## Quality checklist

- Change is compared to a baseline.
- Impacts are not guessed without labeling assumptions.
- Trade-offs are explicit.
- Decision owner/path is clear.
- Stakeholder communication needs are identified.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
