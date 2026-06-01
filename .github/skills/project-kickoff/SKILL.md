---
name: project-kickoff
description: "Prepares project kickoff materials. Use when starting a new project or workstream from projects/_template, defining kickoff agendas, project briefs, stakeholder maps, working agreements, initial risks, decision logs, cadence, and first-week actions."
---

## Purpose

Help a Delivery Lead start a project with enough context, connections, capabilities, and cadence to make the project folder useful from day one.

## When to use this skill

Use this skill when the user asks for:

- project kickoff
- new workstream setup
- project brief creation
- kickoff agenda
- first-week project plan
- stakeholder map setup
- copy projects/_template

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- new project name and purpose
- `projects/_template/README.md`
- `projects/_template/context/project-brief.md`
- `projects/_template/connections/stakeholders.md`
- `projects/_template/context/work-plan.md`
- `projects/_template/context/raid-log.md`
- known stakeholders, dates, constraints, and desired cadence

## Process

1. Clarify project purpose, outcome, stakeholders, and kickoff objective.
2. Use the 4C model: Context, Connections, Capabilities, Cadence.
3. Draft initial project brief, kickoff agenda, stakeholder map, RAID seeds, and first-week actions.
4. Identify missing facts needed to complete the project folder.
5. If asked to create files, preserve the project template structure and avoid introducing vendor-specific folders.
6. Keep the project usable when opened directly as its own workspace.

## Output format

```markdown
# Project Kickoff Pack — <Project Name>

## Kickoff objective

## Context

- Outcome:
- Scope:
- Non-scope:
- Constraints:

## Connections

| Stakeholder / team | Role | Interest | Engagement need |
|---|---|---|---|
|  |  |  |  |

## Capabilities / working approach

## Cadence

## Initial RAID items

## Kickoff agenda

## First-week actions

1.
2.
3.

## Missing inputs
```

## Quality checklist

- 4C model is used explicitly.
- Project folder structure remains standalone.
- Kickoff output identifies scope and non-scope.
- Stakeholders and cadence are visible.
- First-week actions are clear.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
