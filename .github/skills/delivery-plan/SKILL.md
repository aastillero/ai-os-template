---
name: delivery-plan
description: Creates phased delivery plans. Use when turning goals, scope, requirements, project briefs, roadmap items, or ambiguous delivery asks into milestones, phases, tasks, dependencies, risks, acceptance criteria, and next actions.
---

## Purpose

Help a Delivery Lead turn a goal or rough scope into a practical delivery plan that can be reviewed with teams and stakeholders.

## When to use this skill

Use this skill when the user asks for:

- delivery plan
- project plan
- workstream plan
- milestone plan
- implementation sequence
- delivery roadmap
- plan from requirements or scope

## Inputs to gather

Look for available context in:

- `projects/<project-name>/context/project-brief.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/dependencies.md`
- `projects/<project-name>/connections/stakeholders.md`
- user-provided goals, requirements, or constraints

## Process

1. Restate the delivery outcome in plain language.
2. Identify scope, non-scope, assumptions, constraints, and open questions.
3. Break work into phases or milestones.
4. For each phase, define objective, key activities, dependencies, risks, outputs, and acceptance criteria.
5. Identify decisions needed before or during execution.
6. Call out sequencing constraints and parallelizable work.
7. End with immediate next actions.

## Output format

```markdown
# Delivery Plan — <Project or Workstream>

## Outcome

## Scope

## Out of scope / not yet confirmed

## Assumptions

## Milestones / phases

| Phase | Objective | Key work | Dependencies | Exit criteria |
|---|---|---|---|---|
|  |  |  |  |  |

## Risks and mitigations

| Risk | Impact | Mitigation | Owner |
|---|---|---|---|
|  |  |  |  |

## Decisions needed

-

## Immediate next actions

1.
2.
3.

## Missing inputs

-
```

## Quality checklist

- The plan is sequenced, not just a task dump.
- Each phase has an exit criterion.
- Dependencies and decisions are visible.
- Unknowns are labeled as assumptions or missing inputs.
- The first next action is clear.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent team capacity, deadlines, technical feasibility, stakeholder approval, owners, commitments, or test results.
- If the plan depends on missing facts, mark them as assumptions or questions.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
