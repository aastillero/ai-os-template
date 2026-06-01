# Projects and Workstreams

Active projects, workstreams, initiatives, or major responsibilities live here.

For the current Delivery Lead edition, these will usually be software delivery projects. For another role edition, this folder can represent the role's main work objects.

## Project model: the 4 C's

Every project should be a small standalone AI OS workspace organized around:

- Context
- Connections
- Capabilities
- Cadence

That means a project folder should be useful from the parent workspace and also when opened directly for focused work.

## How to create a project or workstream

Copy:

```text
projects/_template/
```

To:

```text
projects/<project-name>/
```

Use lowercase folder names with hyphens, for example:

```text
projects/customer-portal-modernization/
projects/payment-platform-release/
projects/mobile-app-stability/
```

## Minimum useful context

At minimum, fill in:

- `README.md`
- `context/project-brief.md`
- `context/current-state.md`
- `connections/stakeholders.md`
- `context/work-plan.md`
- `context/status.md`
- `context/raid-log.md`
- `capabilities/workflows.md`
- `cadence/daily-focus.md`

## Project focus mode

If the user wants focused work on one project, open that project folder directly:

```text
projects/<project-name>/
```

The project folder has its own:

- `AGENTS.md`
- `.github/copilot-instructions.md`
- `.github/skills/`
- 4C folders

So it should behave like a normal project workspace.

## When a project or workstream ends

Move completed or stale work to an archive folder that your organization approves, or keep it here if you still need the context.
