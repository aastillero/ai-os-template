# Workspace Operating Model

This workspace is organized as a role-specific AI operating system.

The current instance is for a Software Development Delivery Lead, but the model is reusable for other roles.

## Core model: the 4 C's

Every level of the workspace should be organized around the 4 C's.

| C | Purpose |
|---|---|
| Context | The facts, goals, current state, plans, decisions, risks, and boundaries the AI needs to understand. |
| Connections | Stakeholders, teams, systems, dependencies, communication paths, meetings, and links. |
| Capabilities | Reusable workflows, templates, prompts, and future Copilot skills. |
| Cadence | Daily, weekly, monthly, milestone, or cycle-based rituals that keep work moving. |

The root workspace applies the 4 C's to the role. Each project workspace applies the 4 C's to a specific project or workstream.

## Root workspace layers

### 1. Role context

Where Copilot learns what role this workspace is serving.

Folder/file:

```text
context/role-profile.md
roles/<role-name>/profile.md
```

`context/role-profile.md` is the active role. `roles/` stores reusable role packs that can be copied into the active profile.

### 2. Personal and operating context

Where Copilot learns who you are, how you work, and how work runs in your environment.

Folder:

```text
context/
```

### 3. Projects or workstreams

Where active work-specific context lives.

Folder:

```text
projects/<project-name>/
```

Each project/workstream is also a standalone 4C mini-workspace.

### 4. Cadence

Where daily, weekly, and monthly operating rhythms live.

Folder:

```text
cadence/
```

These are not automations. They are repeatable work rituals that help the role holder use AI consistently.

### 5. Templates

Reusable document shapes for common role outputs.

Folder:

```text
templates/
```

### 6. Skills

Future role-level Copilot skills will live here:

```text
.github/skills/
```

This base project intentionally leaves the skills folder empty until the skill set is designed.

## Project workspace model

Every project copied from `projects/_template/` should have this shape:

```text
projects/<project-name>/
├── README.md
├── AGENTS.md
├── .github/
│   ├── copilot-instructions.md
│   └── skills/
│       └── .gitkeep
├── context/
│   ├── project-brief.md
│   ├── current-state.md
│   ├── work-plan.md
│   ├── status.md
│   ├── raid-log.md
│   ├── decisions.md
│   └── notes/.gitkeep
├── connections/
│   ├── stakeholders.md
│   ├── dependencies.md
│   ├── systems-and-links.md
│   ├── communication-map.md
│   └── meetings.md
├── capabilities/
│   ├── README.md
│   ├── workflows.md
│   ├── prompts.md
│   └── skill-backlog.md
└── cadence/
    ├── daily-focus.md
    ├── weekly-project-review.md
    └── milestone-checkpoint.md
```

This means the user can open either:

```text
delivery-lead-ai-os-starter/
```

for role-level work, or:

```text
projects/<project-name>/
```

for focused project work.

When a project folder is opened directly, project-local `README.md`, `AGENTS.md`, and `.github/copilot-instructions.md` should be enough to guide Copilot without relying on the parent folder.

## How to add a project or workstream

1. Copy `projects/_template/`.
2. Rename the copy to the project/workstream name.
3. Fill in the project's `README.md` and `context/project-brief.md` first.
4. Fill in enough 4C context for Copilot to answer:
   - Context: What are we trying to accomplish? Why? What is true now?
   - Connections: Who cares? What systems, teams, dependencies, or channels matter?
   - Capabilities: What repeatable workflows or prompts help this project?
   - Cadence: What daily, weekly, or milestone rhythm keeps it moving?

## How to adapt this workspace to another role

1. Create `roles/<new-role>/profile.md` from `roles/_template/profile.md`.
2. Replace `context/role-profile.md` with that role profile.
3. Review cadence prompts and templates for role-specific language.
4. Keep the 4C project workspace pattern unless the new role has a genuinely different work object than projects/workstreams.
5. Add skills later under `.github/skills/` or project-local `.github/skills/` only after repeatable workflows are proven.

## Good workspace hygiene

- Prefer short, current summaries over long pasted histories.
- Record decisions and reasons, not just outcomes.
- Keep risks explicit.
- Archive stale projects instead of deleting useful history.
- Keep confidential data out unless your organization explicitly permits it.
- Keep project-local facts in the project folder so project focus mode stays useful.
