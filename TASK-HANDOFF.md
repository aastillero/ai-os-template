# Task Handoff

Last updated: 2026-06-01T03:50:35+00:00

Use this file to transfer the current project state into a new session. In a new session, ask the agent to read this file first, then continue from the latest user instruction.

## Project location

```text
/mnt/hermes-workspace/delivery-lead-ai-os-starter
```

## Current project purpose

This repository is a GitHub Copilot-native Role AI OS starter workspace.

The current role edition is Delivery Lead, but the project must remain easy to translate to other roles later, such as Product Owner, Engineering Manager, QA Lead, Business Analyst, or other software-delivery-adjacent roles.

The workspace now uses Nate Herk's 4 C's as the organizing model at two levels:

1. Root workspace = role-level AI OS.
2. `projects/<project-name>/` = project-specific mini AI OS that can also be opened directly as its own workspace.

The 4 C's are:

- Context
- Connections
- Capabilities
- Cadence

## Current task state

Status: base project scaffold created, generalized into a reusable role template, and refined so every project created inside the workspace follows the 4C model and can function as a standalone project workspace.

### Completed

- Reviewed Nate Herk AI OS context from the YouTube URL supplied by the user.
- Reviewed the reference GitHub repository:

  ```text
  https://github.com/nateherkai/AIS-OS
  ```

- Confirmed this project is not Otto.
- Confirmed target users will use GitHub Copilot only.
- Created the starter workspace at:

  ```text
  /mnt/hermes-workspace/delivery-lead-ai-os-starter
  ```

- Initialized a local git repository.
- Created the root Copilot-native role workspace with:

  ```text
  .github/copilot-instructions.md
  .github/skills/.gitkeep
  AGENTS.md
  README.md
  QUICKSTART.md
  WORKSPACE.md
  TEMPLATE.md
  context/
  cadence/
  projects/
  templates/
  references/
  roles/
  decisions/
  ```

- Generalized the original Delivery Lead-specific scaffold into a reusable Role AI OS template.
- Added role packs:

  ```text
  roles/_template/profile.md
  roles/delivery-lead/profile.md
  ```

- Made the active role profile live here:

  ```text
  context/role-profile.md
  ```

- Renamed role-specific files to template-friendly names:

  ```text
  context/delivery-lead-role.md -> context/role-profile.md
  references/delivery-lead-ai-os-framework.md -> references/role-ai-os-framework.md
  projects/_template/delivery-plan.md -> project work plan concept
  ```

- Refined the root documentation around the 4 C's:

  ```text
  README.md
  QUICKSTART.md
  WORKSPACE.md
  TEMPLATE.md
  AGENTS.md
  .github/copilot-instructions.md
  projects/README.md
  references/role-ai-os-framework.md
  cadence/daily-startup.md
  cadence/weekly-review.md
  cadence/monthly-retro.md
  ```

- Rebuilt `projects/_template/` as a standalone 4C project workspace:

  ```text
  projects/_template/
  ├── README.md
  ├── AGENTS.md
  ├── .github/
  │   ├── copilot-instructions.md
  │   └── skills/.gitkeep
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

- Removed the old flat project-template files that were replaced by the 4C folders:

  ```text
  projects/_template/PROJECT.md
  projects/_template/stakeholders.md
  projects/_template/work-plan.md
  projects/_template/status.md
  projects/_template/raid-log.md
  projects/_template/decisions.md
  projects/_template/meetings.md
  projects/_template/notes/
  ```

- Preserved the no-skills-yet guardrail. Skill folders contain `.gitkeep` placeholders only.

## Current design decisions

1. This is a role-template project, not a one-off Delivery Lead workspace.
2. Delivery Lead is the first concrete role edition.
3. The active role source of truth is:

   ```text
   context/role-profile.md
   ```

4. Reusable role packs live under:

   ```text
   roles/<role-name>/profile.md
   ```

5. The whole workspace follows the 4 C's:

   ```text
   Context
   Connections
   Capabilities
   Cadence
   ```

6. The root workspace is the role-level AI OS.
7. Each copied project folder under `projects/<project-name>/` is a project-level AI OS and should work when opened directly.
8. Root-level future Copilot skills belong under:

   ```text
   .github/skills/<skill-name>/SKILL.md
   ```

9. Project-specific future Copilot skills belong under:

   ```text
   projects/<project-name>/.github/skills/<skill-name>/SKILL.md
   ```

10. No skills have been added yet. All `.github/skills/` folders are intentionally placeholders only.
11. Do not introduce Claude/Codex-specific structure, including:

   ```text
   .claude/
   .codex/
   .agents/
   ```

12. Keep the reusable core stable and isolate role-specific assumptions into role profile, role packs, cadence examples, templates, and future role-specific skills.
13. Keep project-specific facts inside the relevant project folder so project focus mode remains useful.

## Important guardrails

- GitHub Copilot only.
- Do not add `SKILL.md` files until the user explicitly says to start adding skills.
- Do not use Claude Code, Codex, `.claude/`, `.codex/`, or `.agents/` conventions.
- Treat this as a reusable Role AI OS template.
- Treat every copied project folder as a standalone 4C project workspace.
- Keep Delivery Lead language only where it is intentionally the current role edition or example.
- Keep secrets, credentials, tokens, and unnecessary confidential data out of all files.
- If adapting to another role, start from `TEMPLATE.md` and `roles/_template/profile.md`.
- If creating a new project, start from `projects/_template/`.

## Recommended files to read first in a new session

Read these in order:

1. `TASK-HANDOFF.md`
2. `README.md`
3. `WORKSPACE.md`
4. `TEMPLATE.md`
5. `QUICKSTART.md`
6. `.github/copilot-instructions.md`
7. `AGENTS.md`
8. `references/role-ai-os-framework.md`
9. `projects/README.md`
10. `projects/_template/README.md`
11. `projects/_template/AGENTS.md`
12. `projects/_template/.github/copilot-instructions.md`
13. `projects/_template/context/project-brief.md`
14. `projects/_template/connections/stakeholders.md`
15. `projects/_template/capabilities/README.md`
16. `projects/_template/cadence/daily-focus.md`
17. `context/role-profile.md`
18. `roles/README.md`

## Suggested new-session prompt

```text
Please load the project handoff from:
/mnt/hermes-workspace/delivery-lead-ai-os-starter/TASK-HANDOFF.md

Then inspect the project state and continue from my latest instruction. Do not add skills yet unless I explicitly ask for skills.
```

## Current git state

A local git repository exists, but no initial commit has been made yet.

Expected current status: starter files are untracked and ready for review/commit.

Live verification on 2026-06-01T03:50:35+00:00:

```text
--- git status --short ---
?? .github/
?? .gitignore
?? AGENTS.md
?? QUICKSTART.md
?? README.md
?? TASK-HANDOFF.md
?? TEMPLATE.md
?? WORKSPACE.md
?? cadence/
?? context/
?? decisions/
?? projects/
?? references/
?? roles/
?? templates/
--- git branch/log ---
master
fatal: your current branch 'master' does not have any commits yet
```

## Verification commands for the next session

From the project root:

```bash
python3 - <<'PY'
from pathlib import Path
print('SKILL_MD_COUNT=' + str(len(list(Path('.').rglob('SKILL.md')))))
PY
test ! -d .claude && echo NO_CLAUDE
test ! -d .codex && echo NO_CODEX
test ! -d .agents && echo NO_AGENTS
test -f .github/skills/.gitkeep && echo ROOT_SKILLS_PLACEHOLDER_OK
test -f projects/_template/.github/skills/.gitkeep && echo PROJECT_SKILLS_PLACEHOLDER_OK
test -f projects/_template/README.md && echo PROJECT_TEMPLATE_README_OK
test -f projects/_template/AGENTS.md && echo PROJECT_TEMPLATE_AGENTS_OK
test -f projects/_template/.github/copilot-instructions.md && echo PROJECT_TEMPLATE_COPILOT_OK
test -d projects/_template/context && echo PROJECT_CONTEXT_OK
test -d projects/_template/connections && echo PROJECT_CONNECTIONS_OK
test -d projects/_template/capabilities && echo PROJECT_CAPABILITIES_OK
test -d projects/_template/cadence && echo PROJECT_CADENCE_OK
```

Expected output:

```text
SKILL_MD_COUNT=0
NO_CLAUDE
NO_CODEX
NO_AGENTS
ROOT_SKILLS_PLACEHOLDER_OK
PROJECT_SKILLS_PLACEHOLDER_OK
PROJECT_TEMPLATE_README_OK
PROJECT_TEMPLATE_AGENTS_OK
PROJECT_TEMPLATE_COPILOT_OK
PROJECT_CONTEXT_OK
PROJECT_CONNECTIONS_OK
PROJECT_CAPABILITIES_OK
PROJECT_CADENCE_OK
```

Latest verification output:

```text
SKILL_MD_COUNT=0
NO_CLAUDE
NO_CODEX
NO_AGENTS
ROOT_SKILLS_PLACEHOLDER_OK
PROJECT_SKILLS_PLACEHOLDER_OK
OK projects/_template/README.md
OK projects/_template/AGENTS.md
OK projects/_template/.github/copilot-instructions.md
OK projects/_template/context/project-brief.md
OK projects/_template/context/current-state.md
OK projects/_template/context/work-plan.md
OK projects/_template/context/status.md
OK projects/_template/context/raid-log.md
OK projects/_template/context/decisions.md
OK projects/_template/context/notes/.gitkeep
OK projects/_template/connections/stakeholders.md
OK projects/_template/connections/dependencies.md
OK projects/_template/connections/systems-and-links.md
OK projects/_template/connections/communication-map.md
OK projects/_template/connections/meetings.md
OK projects/_template/capabilities/README.md
OK projects/_template/capabilities/workflows.md
OK projects/_template/capabilities/prompts.md
OK projects/_template/capabilities/skill-backlog.md
OK projects/_template/cadence/daily-focus.md
OK projects/_template/cadence/weekly-project-review.md
OK projects/_template/cadence/milestone-checkpoint.md
REMOVED projects/_template/PROJECT.md
REMOVED projects/_template/stakeholders.md
REMOVED projects/_template/work-plan.md
REMOVED projects/_template/status.md
REMOVED projects/_template/raid-log.md
REMOVED projects/_template/decisions.md
REMOVED projects/_template/meetings.md
REMOVED projects/_template/notes
secret_scan_matches=0
```

## Remaining work / likely next steps

Do not assume these are approved. Ask or follow the user's latest instruction.

1. User review of the refined 4C structure.
2. Decide whether to make the first git commit.
3. Optionally test the template by copying `projects/_template/` to a sample project and opening it as a direct project workspace.
4. Decide which Delivery Lead workflows should become the first Copilot skills.
5. Only after explicit approval, create `.github/skills/<skill-name>/SKILL.md` files or project-local `projects/<project-name>/.github/skills/<skill-name>/SKILL.md` files.
6. Later, test adaptation by creating another role pack, for example Product Owner or QA Lead.

## Blockers

None currently.

## Pitfalls to avoid

- Do not rebuild the project from scratch; the scaffold already exists.
- Do not accidentally convert this into a Claude/Codex project.
- Do not add skills prematurely.
- Do not overfit all documents to Delivery Lead; this must remain portable to other roles.
- Do not rely on memory alone; read the project files before editing.
- Do not reintroduce the old flat project template unless the user explicitly prefers it.
- Do not put project-specific facts only in the root workspace; project focus mode depends on project-local context.

## Handoff update rule

When meaningful project decisions or structural changes are made, update this file before ending the session so the next session can resume without rework.
