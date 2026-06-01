# Role AI OS Framework

This workspace uses Nate Herk's 4 C's as the organizing model:

1. Context
2. Connections
3. Capabilities
4. Cadence

The model applies twice:

- Root workspace: the role-level AI OS.
- Project workspace: each project/workstream under `projects/`.

## 1. Context

Context is what the AI needs to know to reason accurately.

At the root level, context includes:

```text
context/role-profile.md
context/personalization-intake.md
context/operating-principles.md
context/ways-of-working.md
```

At the project level, context includes:

```text
projects/<project-name>/context/project-brief.md
projects/<project-name>/context/current-state.md
projects/<project-name>/context/work-plan.md
projects/<project-name>/context/status.md
projects/<project-name>/context/raid-log.md
projects/<project-name>/context/decisions.md
projects/<project-name>/context/notes/
```

Context should be current, concise, and factual. Prefer a short accurate current-state note over a long stale history.

## 2. Connections

Connections are the people, systems, teams, dependencies, and communication paths that shape the work.

At the project level, connections include:

```text
projects/<project-name>/connections/stakeholders.md
projects/<project-name>/connections/dependencies.md
projects/<project-name>/connections/systems-and-links.md
projects/<project-name>/connections/communication-map.md
projects/<project-name>/connections/meetings.md
```

Connections help Copilot answer questions like:

- Who cares about this?
- Who approves?
- What systems or teams are involved?
- What dependencies could block progress?
- What communication path should be used?

## 3. Capabilities

Capabilities are reusable ways of doing work.

Start with templates and prompts. Add skills only after a workflow is proven and the user explicitly approves making it a skill.

Root-level capabilities include:

```text
templates/
.github/skills/
```

Project-level capabilities include:

```text
projects/<project-name>/capabilities/README.md
projects/<project-name>/capabilities/workflows.md
projects/<project-name>/capabilities/prompts.md
projects/<project-name>/capabilities/skill-backlog.md
projects/<project-name>/.github/skills/
```

Current Delivery Lead examples:

- weekly status update
- RAID review
- release readiness check
- stakeholder escalation draft
- meeting prep
- decision capture

Future role examples might include:

- Product Owner: backlog refinement, acceptance criteria review, roadmap trade-off analysis
- QA Lead: test strategy review, defect triage, release quality summary
- Engineering Manager: 1:1 prep, team health review, hiring scorecard synthesis
- Business Analyst: requirements clarification, process mapping, stakeholder question list

## 4. Cadence

Cadence is the rhythm that keeps the workspace useful.

At the root level:

```text
cadence/daily-startup.md
cadence/weekly-review.md
cadence/monthly-retro.md
```

At the project level:

```text
projects/<project-name>/cadence/daily-focus.md
projects/<project-name>/cadence/weekly-project-review.md
projects/<project-name>/cadence/milestone-checkpoint.md
```

Cadence files are not automations. They are repeatable rituals and prompt patterns.

## Project focus mode

Each project copied from `projects/_template/` should be usable as a standalone project workspace.

That means it has its own:

```text
README.md
AGENTS.md
.github/copilot-instructions.md
.github/skills/
context/
connections/
capabilities/
cadence/
```

If the user opens `projects/<project-name>/` directly, Copilot should be able to operate from the project-local files without needing the parent workspace.

## Skill boundary

This starter intentionally scaffolds skill folders but does not add actual skills yet.

Do not create `SKILL.md` files until the user explicitly approves adding skills.
