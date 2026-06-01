# Role AI OS Starter Workspace — Delivery Lead Edition

A GitHub Copilot-native starter workspace for building a role-specific AI operating system.

This repository is currently configured for Software Development Delivery Leads, but the structure is intentionally reusable. The reusable core can support other roles later by swapping the role profile, role examples, project/workstream templates, cadence prompts, and future `.github/skills/`.

## Template stance

Treat this as a role template, not a one-off Delivery Lead folder.

The workspace has two levels:

1. Role-level AI OS
   - root Copilot instructions
   - root agent guidance
   - role context
   - cross-project cadence
   - reusable templates
   - future role-level skills

2. Project-level AI OS workspaces
   - one folder per project or workstream under `projects/`
   - each project has its own instructions, context, connections, capabilities, cadence, and future skill location
   - each project can be opened directly for focused work

When adapting this for another role, keep the reusable core and replace only the role-specific layer.

## The 4 C's

Both the root workspace and every project workspace should follow the 4 C's.

| C | Meaning | Root example | Project example |
|---|---|---|---|
| Context | What the AI needs to know | `context/role-profile.md` | `projects/<project>/context/` |
| Connections | People, systems, dependencies, channels | role collaborators and operating context | `projects/<project>/connections/` |
| Capabilities | Reusable workflows, prompts, and future skills | `templates/`, `.github/skills/` | `projects/<project>/capabilities/`, project `.github/skills/` |
| Cadence | Operating rhythms | `cadence/` | `projects/<project>/cadence/` |

## Current audience

Delivery Leads, Project Leads, Scrum Masters, Engineering Managers, and software delivery operators who coordinate people, scope, risk, releases, stakeholders, and delivery outcomes.

## What this is not

- Not a Claude Code project.
- Not a Codex project.
- Not a codebase for a product.
- Not a dumping ground for raw chats or confidential data.
- Not a replacement for Jira, Azure DevOps, GitHub Issues, Confluence, Teams, Slack, or email.

It is a structured workspace that gives GitHub Copilot enough context to help the role holder think and work more effectively.

## Core idea

Use this workspace as your daily command center.

When you come in to work:

1. Open the root workspace when you need cross-project role context.
2. Open a project folder under `projects/<project-name>/` when you need focused project work.
3. Review the relevant cadence prompt.
4. Update the project or workstream files so Copilot has current facts.
5. Ask Copilot to help with role-relevant thinking, drafting, summarizing, and planning using the files in this workspace.

## Current shape

```text
delivery-lead-ai-os-starter/          # role-level AI OS; template can be copied for other roles
├── README.md
├── QUICKSTART.md
├── TEMPLATE.md
├── TASK-HANDOFF.md
├── AGENTS.md
├── WORKSPACE.md
├── .github/
│   ├── copilot-instructions.md
│   └── skills/
│       └── .gitkeep
├── roles/
│   ├── README.md
│   ├── _template/
│   │   └── profile.md
│   └── delivery-lead/
│       └── profile.md
├── context/
│   ├── role-profile.md
│   ├── operating-principles.md
│   ├── personalization-intake.md
│   └── ways-of-working.md
├── cadence/
│   ├── daily-startup.md
│   ├── weekly-review.md
│   └── monthly-retro.md
├── projects/
│   ├── README.md
│   └── _template/
│       ├── README.md
│       ├── AGENTS.md
│       ├── .github/
│       │   ├── copilot-instructions.md
│       │   └── skills/.gitkeep
│       ├── context/
│       ├── connections/
│       ├── capabilities/
│       └── cadence/
├── templates/
│   ├── status-update.md
│   ├── meeting-prep.md
│   ├── decision-record.md
│   └── risk-entry.md
├── decisions/
│   └── log.md
└── references/
    ├── ai-safety-and-boundaries.md
    └── role-ai-os-framework.md
```

## Copilot-native conventions

- Repository-wide Copilot behavior lives in root `.github/copilot-instructions.md`.
- Root agent behavior lives in root `AGENTS.md`.
- Active role context lives in `context/role-profile.md`.
- Reusable role packs live in `roles/<role-name>/`.
- Future role-level skills will live in root `.github/skills/<skill-name>/SKILL.md`.
- Project-specific Copilot behavior lives in `projects/<project-name>/.github/copilot-instructions.md`.
- Project-specific agent behavior lives in `projects/<project-name>/AGENTS.md`.
- Future project-specific skills will live in `projects/<project-name>/.github/skills/<skill-name>/SKILL.md`.
- This base project intentionally does not include skills yet. Skill folders are only scaffolded with `.gitkeep` files.

## Suggested first use

1. Read `QUICKSTART.md`.
2. Review the active role in `context/role-profile.md`.
3. Fill in `context/personalization-intake.md`.
4. Copy `projects/_template/` to `projects/<your-project-name>/`.
5. Fill in that project's 4C files, starting with `README.md`, `context/project-brief.md`, `context/current-state.md`, and `connections/stakeholders.md`.
6. Ask Copilot: "Using this workspace context and the active role profile, help me identify the top risks, decisions, and next actions I should focus on today."

## Project focus mode

For focused project work, open the project folder directly:

```text
projects/<project-name>/
```

That folder has its own:

- `README.md`
- `AGENTS.md`
- `.github/copilot-instructions.md`
- `context/`
- `connections/`
- `capabilities/`
- `cadence/`
- `.github/skills/`

This lets the project behave like a normal standalone workspace while still fitting inside the broader role-level AI OS.

## Continuing work in a new session

For session-to-session continuity, read `TASK-HANDOFF.md` first. It captures current project state, decisions, guardrails, verification commands, and likely next steps.

Suggested prompt:

```text
Please load TASK-HANDOFF.md from this project, then continue from my latest instruction.
```

## Adapting to another role

Use `TEMPLATE.md` as the adaptation guide. In short:

1. Copy `roles/_template/profile.md` to `roles/<new-role>/profile.md`.
2. Replace `context/role-profile.md` with the new role profile.
3. Adjust examples in `cadence/`, `projects/_template/`, and `templates/` only where the role needs different work products.
4. Keep `.github/copilot-instructions.md` generic so it always reads the active role from `context/role-profile.md`.
5. Add role-specific or project-specific Copilot skills later only after the manual workflow is clear.
