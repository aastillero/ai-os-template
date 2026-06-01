# Quickstart

Use this when setting up the workspace for the first time.

## 1. Open the workspace

Open the root folder in VS Code or another GitHub Copilot-enabled environment when you want role-level context across projects.

For focused project work later, you can open a specific project folder directly:

```text
projects/<project-name>/
```

## 2. Confirm the active role

Review:

- `context/role-profile.md`

This starter is currently configured for a Delivery Lead. If you are adapting it for another role, follow `TEMPLATE.md` before personalizing the workspace.

## 3. Personalize your operator context

Fill in:

- `context/personalization-intake.md`
- `context/ways-of-working.md`

Keep it practical. Copilot does not need your life story. It needs enough context to help you work.

## 4. Create your first project or workstream folder

Copy the project template:

```text
projects/_template/ -> projects/<project-name>/
```

Each project uses the 4 C's:

- Context
- Connections
- Capabilities
- Cadence

Complete the key files in this order:

1. `projects/<project-name>/README.md`
2. `projects/<project-name>/context/project-brief.md`
3. `projects/<project-name>/context/current-state.md`
4. `projects/<project-name>/connections/stakeholders.md`
5. `projects/<project-name>/context/work-plan.md`
6. `projects/<project-name>/context/status.md`
7. `projects/<project-name>/context/raid-log.md`
8. `projects/<project-name>/capabilities/workflows.md`
9. `projects/<project-name>/cadence/daily-focus.md`

## 5. Use project focus mode when helpful

If you want Copilot to focus only on one project, open:

```text
projects/<project-name>/
```

That folder has its own:

- `README.md`
- `AGENTS.md`
- `.github/copilot-instructions.md`
- `.github/skills/`
- `context/`
- `connections/`
- `capabilities/`
- `cadence/`

So it should behave like a normal standalone project workspace.

## 6. Start the day from the workspace

For role-level daily planning, open `cadence/daily-startup.md`.

Suggested root prompt:

```text
Using this Role AI OS workspace and the active role in context/role-profile.md, help me plan today. Review my active project/workstream status, RAID items, recent decisions, and work plan. Give me the top 3 things that need attention today, the reason each matters, and the next action I should take.
```

For project-specific daily planning, open the project folder and use `cadence/daily-focus.md`.

## 7. Keep the workspace current

The workspace only becomes useful if it reflects reality.

Update it after:

- scope changes
- stakeholder decisions
- role-relevant risks
- release or milestone changes
- sprint/release/review cycles
- major meetings
- escalations
- dependency changes

## Important habit

Do not paste sensitive credentials, private tokens, passwords, or unnecessary customer data into this workspace.
