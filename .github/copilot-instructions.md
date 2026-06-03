# GitHub Copilot Instructions

This repository is a Role AI OS starter workspace. It is currently configured as the Delivery Lead edition.

Copilot should treat this as a structured operating workspace for a role holder, not as a normal application codebase.

## Role source of truth

Before giving role-specific advice, use:

```text
context/role-profile.md
```

That file defines the active role, outcomes, responsibilities, work products, and AI boundaries. If this template is adapted for another role, follow the updated role profile instead of assuming Delivery Lead behavior.

## 4C model

Use the 4 C's at both workspace levels:

- Context: role/project facts, current state, plans, decisions, risks, boundaries.
- Connections: stakeholders, teams, systems, dependencies, links, meetings, channels.
- Capabilities: workflows, templates, prompts, and Copilot skills.
- Cadence: daily, weekly, monthly, milestone, or cycle-based rhythms.

## Project focus mode

Active projects or workstreams live in:

```text
projects/<project-name>/
```

Each project copied from `projects/_template/` is also a standalone mini-workspace with its own:

- `README.md`
- `AGENTS.md`
- `.github/copilot-instructions.md`
- `.github/skills/`
- `context/`
- `connections/`
- `capabilities/`
- `cadence/`

When a user asks about a specific project, read that project's local files before making recommendations. Project-local files are the source of truth for project facts.

If the user opens `projects/<project-name>/` directly, work from the local project instructions and do not require parent files.

## How to respond

- Be direct, concise, and role-focused.
- Use the repository files as context before making recommendations.
- Prefer actionable outputs: next steps, risks, decisions needed, owners, dates, and follow-ups.
- If information is missing, identify the smallest missing input needed.
- Never fabricate project details, dates, commitments, risks, or stakeholder positions.
- When drafting external or stakeholder-facing messages, produce a reviewable draft, not a final sent message.

## Current Delivery Lead lens

For the current role edition, consider:

- Scope and outcomes
- Timeline and milestones
- Dependencies
- Risks, assumptions, issues, and decisions
- Stakeholders and communication needs
- Team capacity and blockers
- Release readiness
- Evidence needed for status claims

For future role editions, replace this lens by updating `context/role-profile.md` and any role-specific examples.

## Workspace conventions

- Active role context lives in `context/role-profile.md`.
- Personal operating context lives in `context/personalization-intake.md` and `context/ways-of-working.md`.
- Active project or workstream context lives in `projects/<project-name>/`.
- Repeatable operating rhythms live in `cadence/` and project-local `cadence/` folders.
- Reusable document patterns live in `templates/`.
- Reusable role packs live in `roles/<role-name>/`.
- Role-level Copilot skills live in root `.github/skills/`.
- Future project-specific Copilot skills will live in project-local `.github/skills/`.

## Security boundaries

Do not request, store, or expose:

- passwords
- API keys
- personal access tokens
- private keys
- unnecessary customer data
- sensitive employee data
- production credentials

If a task requires sensitive information, ask the user to use the approved company system instead of pasting it into this workspace.
