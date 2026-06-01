# Project Agent Instructions

This folder is a project-specific AI OS workspace.

## Operating mode

If this folder is opened directly, treat it as the active workspace root.

If this folder is opened from inside the parent Role AI OS workspace, combine:

1. Parent role context, especially `../../context/role-profile.md` when available.
2. This project's local 4C files.

Project-local files take priority for project facts.

## Project source of truth

Read these first for project work:

1. `README.md`
2. `context/project-brief.md`
3. `context/current-state.md`
4. `context/work-plan.md`
5. `context/status.md`
6. `context/raid-log.md`
7. `connections/stakeholders.md`
8. `capabilities/README.md`
9. `cadence/daily-focus.md`

## Working style

- Be concise and practical.
- Ground project claims in project files.
- Distinguish known facts from assumptions.
- Never invent stakeholders, dates, status, commitments, dependencies, risks, or decisions.
- Ask for the smallest missing input only when it materially changes the answer.
- Keep status updates evidence-based.
- Draft external stakeholder messages for human review; do not treat them as sent.

## 4C responsibilities

- Context: keep project truth current.
- Connections: keep people, systems, channels, and dependencies visible.
- Capabilities: turn repeated useful workflows into prompts first, then skills only after approval.
- Cadence: use repeatable check-ins to keep the project moving.

## Skills boundary

Future project-specific Copilot skills should live in:

```text
.github/skills/<skill-name>/SKILL.md
```

Do not create `SKILL.md` files unless the user explicitly approves adding skills.
