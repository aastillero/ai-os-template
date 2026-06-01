# Project Workspace: <Project / Workstream Name>

This folder is a standalone project-specific AI OS workspace.

It can be used in two ways:

1. From the parent Role AI OS workspace, where role-level context is also available.
2. Directly, by opening this project folder in VS Code or another GitHub Copilot-enabled environment.

When opened directly, this folder should still work as a normal project workspace because it has its own instructions, agent guidance, context, connections, capabilities, cadence, and future skill location.

## The 4 C's

Every project should be organized around these four layers.

| Layer | Purpose | Folder |
|---|---|---|
| Context | What this project is, why it matters, current state, plans, decisions, risks | `context/` |
| Connections | Who and what this project depends on: stakeholders, systems, teams, channels, meetings | `connections/` |
| Capabilities | Repeatable ways this project gets work done: workflows, prompts, future skills | `capabilities/` and `.github/skills/` |
| Cadence | How this project is reviewed and advanced over time | `cadence/` |

## Start here

Fill in these files first:

1. `context/project-brief.md`
2. `context/current-state.md`
3. `connections/stakeholders.md`
4. `context/work-plan.md`
5. `context/status.md`
6. `context/raid-log.md`
7. `capabilities/workflows.md`
8. `cadence/daily-focus.md`

## Project focus mode

When this project folder is opened directly, Copilot or an AI agent should:

1. Read this `README.md`.
2. Read `AGENTS.md`.
3. Read `.github/copilot-instructions.md`.
4. Use the 4C folders as the project source of truth.
5. Treat parent workspace files as optional background, not a dependency.

## Skills

Project-specific Copilot skills belong under:

```text
.github/skills/<skill-name>/SKILL.md
```

Do not add skills until the workflow is proven and the user explicitly wants it encoded as a skill.

For now, use:

```text
capabilities/skill-backlog.md
```

to capture candidate skills.
