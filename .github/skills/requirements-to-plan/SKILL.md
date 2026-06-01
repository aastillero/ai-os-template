---
name: requirements-to-plan
description: "Turns requirements into delivery plans. Use when converting requirements, epics, scope notes, user stories, acceptance criteria, discovery outputs, or stakeholder asks into milestones, workstreams, assumptions, risks, dependencies, and planning questions."
---

## Purpose

Help a Delivery Lead translate requirements into a practical delivery plan without pretending unknown scope, capacity, or technical feasibility is already resolved.

## When to use this skill

Use this skill when the user asks for:

- requirements to plan
- epics to milestones
- scope notes to work breakdown
- user stories to delivery phases
- planning from discovery notes
- acceptance criteria review

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- user-provided requirements or scope notes
- `projects/<project-name>/context/project-brief.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/connections/dependencies.md`
- `projects/<project-name>/context/raid-log.md`
- `templates/status-update.md` if communication output is needed

## Process

1. Restate the target outcome and user/business value.
2. Group requirements into coherent workstreams or milestones.
3. Identify dependencies, assumptions, risks, unknowns, and sequencing constraints.
4. Define acceptance criteria or exit criteria at milestone level.
5. Separate confirmed scope from optional, ambiguous, or out-of-scope items.
6. End with a planning-ready set of next actions and questions.

## Output format

```markdown
# Requirements-to-Plan — <Project or Workstream>

## Outcome

## Requirement groups

| Group | Requirements included | Delivery notes | Acceptance / exit criteria |
|---|---|---|---|
|  |  |  |  |

## Proposed milestones

| Milestone | Objective | Key work | Dependencies | Risks | Exit criteria |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## Assumptions and unknowns

## Scope questions

## Immediate planning actions

1.
2.
3.
```

## Quality checklist

- Requirements are grouped logically.
- Acceptance/exit criteria are not vague.
- Unknowns are not hidden.
- Dependencies and sequencing are explicit.
- Next planning actions are clear.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
