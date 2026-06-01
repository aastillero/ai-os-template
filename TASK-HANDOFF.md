# Task Handoff

Last updated: 2026-06-01T12:39:02+00:00

Use this file to transfer the current project state into a new session. In a new session, ask the agent to read this file first, then continue from the latest user instruction.

Repository note: `TASK-HANDOFF.md` and `SKILLS-MIGRATION-PLAN.md` are intentionally versioned with this starter repository again. The previous local-only/gitignore cleanup was a misunderstanding and has been reversed.

## Project location

```text
/mnt/hermes-workspace/delivery-lead-ai-os-starter
```

## Current project purpose

This repository is a GitHub Copilot-native Role AI OS starter workspace.

The current role edition is Delivery Lead, but the project must remain easy to translate to other roles later, such as Product Owner, Engineering Manager, QA Lead, Business Analyst, or other software-delivery-adjacent roles.

The workspace uses Nate Herk's 4 C's as the organizing model at two levels:

1. Root workspace = role-level AI OS.
2. `projects/<project-name>/` = project-specific mini AI OS that can also be opened directly as its own workspace.

The 4 C's are:

- Context
- Connections
- Capabilities
- Cadence

## Current task state

Status: base project scaffold created, generalized into a reusable role template, refined so every project created inside the workspace follows the 4C model, published to GitHub as `aastillero/ai-os-template` on branch `main`, and Copilot skill migration is implemented through Wave 7 and published to `origin/main`.

Current repository hygiene: `TASK-HANDOFF.md` and `SKILLS-MIGRATION-PLAN.md` are tracked repository files again. `.gitignore` no longer contains root-anchored rules for either file.

Important detail: the prior roadmap only had five waves and 24 serious candidate skills. The latest user instruction was to migrate waves 2 through 6. To satisfy that without adding live integrations, the previously deferred/source-first candidates were promoted into Wave 6:

```text
pdf-review-and-edit
linear-board-review
```

Both Wave 6 skills are standalone-first and work from pasted/extracted/exported content. Direct PDF editing and live Linear API access remain optional/deferred guidance, not default requirements. Wave 7 adds standalone-first PowerPoint deck drafting and editing support without requiring binary `.pptx` generation or editing by default.

## Completed

### Base workspace and publish

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

- Rebuilt `projects/_template/` as a standalone 4C project workspace with local `README.md`, `AGENTS.md`, `.github/copilot-instructions.md`, `.github/skills/.gitkeep`, and 4C folders:

  ```text
  context/
  connections/
  capabilities/
  cadence/
  ```

- Removed the old flat project-template files that were replaced by the 4C folders.
- Preserved the no-skills-yet guardrail during the base scaffold. Real skills were only added after later user approval.
- Renamed the local branch from `master` to `main`.
- Created and pushed the initial local commit:

  ```text
  5bd5adf feat: initialize role AI OS template
  Full SHA: 5bd5adffc086e6432728cedd9293761e67ccc8c2
  ```

- Added the GitHub remote:

  ```text
  origin https://github.com/aastillero/ai-os-template.git
  ```

- Pushed `main` to GitHub and set local `main` to track `origin/main`.
- Verified the remote repository is reachable at:

  ```text
  https://github.com/aastillero/ai-os-template
  ```

### Skills roadmap and migration

- Created the standalone Copilot skills roadmap:

  ```text
  SKILLS-MIGRATION-PLAN.md
  ```

- Refocused the roadmap for a standalone GitHub Copilot project with no Hermes workspace dependency.
- Repository update: this roadmap is tracked again. The earlier local-only/gitignore cleanup was reversed after user clarification.
- Kept skills standalone-first:
  - Markdown-only by default.
  - Repository files and user-provided context only.
  - No scripts.
  - No `allowed-tools` frontmatter.
  - No live SaaS/API integration requirements.
  - No `.claude/`, `.codex/`, or `.agents/` folders.
- Added document/PDF output candidates as source-first skills.
- Added PowerPoint/deck output and editing candidates as source-first skills.
- Migrated Wave 1 through Wave 7 locally under:

  ```text
  .github/skills/<skill-name>/SKILL.md
  ```

## Current Copilot skills

Current root skill count: 28.

### Wave 1 — Starter Delivery Lead skills

```text
delivery-status-report
raid-review
delivery-plan
stakeholder-update
meeting-prep-and-follow-up
decision-record
```

### Wave 2 — High-value expansions

```text
document-intake
teams-meeting-synthesis
dependency-map
weekly-delivery-review
requirements-to-plan
release-readiness-review
```

Notes:

- `document-intake` works from pasted/extracted text first. OCR tooling is optional guidance only.
- `teams-meeting-synthesis` works from pasted/exported transcript text first. Microsoft Graph/Teams integration is optional guidance only.

### Wave 3 — Document, visual, and executive communication

```text
delivery-infographic
executive-briefing
roadmap-communication
presentation-outline
word-document-draft
word-document-edit
pdf-export
```

Notes:

- `delivery-infographic` outputs an infographic brief/spec, not generated media.
- `word-document-draft` and `word-document-edit` are source-first. Actual `.docx` tooling is optional guidance only.
- `pdf-export` outputs PDF-ready source/spec. Actual rendering tools are optional guidance only.

### Wave 4 — Optional deeper delivery control

```text
qa-and-acceptance-review
scope-change-review
evidence-review
project-kickoff
```

### Wave 5 — Tool-specific delivery workflows

```text
github-issue-triage
```

Note: works from pasted/exported issue lists. Live GitHub API access is optional/deferred.

### Wave 6 — Source-first deferred adapters

```text
pdf-review-and-edit
linear-board-review
```

Notes:

- `pdf-review-and-edit` works from pasted/extracted PDF text. Direct PDF binary editing is optional/deferred.
- `linear-board-review` works from pasted/exported Linear-style board data. Live Linear API access is optional/deferred.

### Wave 7 — PowerPoint / deck production adapters

```text
powerpoint-deck-draft
powerpoint-deck-edit
```

Notes:

- `powerpoint-deck-draft` creates PowerPoint-ready Markdown/storyboard content, slide-by-slide copy, speaker notes, and visual direction. Actual `.pptx` generation is optional guidance only.
- `powerpoint-deck-edit` works from pasted or extracted deck text first. Direct `.pptx` binary editing is optional guidance only.

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
8. Root-level Copilot skills live under:

   ```text
   .github/skills/<skill-name>/SKILL.md
   ```

9. Project-specific future Copilot skills belong under:

   ```text
   projects/<project-name>/.github/skills/<skill-name>/SKILL.md
   ```

10. Do not introduce Claude/Codex-specific structure, including:

   ```text
   .claude/
   .codex/
   .agents/
   ```

11. Keep the reusable core stable and isolate role-specific assumptions into role profile, role packs, cadence examples, templates, and role-specific skills.
12. Keep project-specific facts inside the relevant project folder so project focus mode remains useful.
13. Integration-heavy skills must work from pasted/exported/user-provided content first. Live tool/API setup belongs in optional references or future guides only.

## Important guardrails

- GitHub Copilot only.
- Do not use Claude Code, Codex, `.claude/`, `.codex/`, or `.agents/` conventions.
- Treat this as a reusable Role AI OS template.
- Treat every copied project folder as a standalone 4C project workspace.
- Keep Delivery Lead language only where it is intentionally the current role edition or example.
- Keep secrets, credentials, tokens, and unnecessary confidential data out of all files.
- If adapting to another role, start from `TEMPLATE.md` and `roles/_template/profile.md`.
- If creating a new project, start from `projects/_template/`.
- Do not add `allowed-tools`, scripts, browser automation, API clients, shell execution, or live integrations to skills by default.
- For Word/PDF/PowerPoint skills, keep the default output source-first: Markdown/content, storyboards, speaker notes, edit plans, export specs, and QA checklists.

## Recommended files to read first in a new session

Read these in order from the repository workspace:

1. `TASK-HANDOFF.md`
2. `SKILLS-MIGRATION-PLAN.md`
3. `README.md`
4. `WORKSPACE.md`
5. `TEMPLATE.md`
6. `QUICKSTART.md`
7. `.github/copilot-instructions.md`
8. `AGENTS.md`
9. `references/role-ai-os-framework.md`
10. `projects/README.md`
11. `projects/_template/README.md`
12. `projects/_template/AGENTS.md`
13. `projects/_template/.github/copilot-instructions.md`
14. `projects/_template/context/project-brief.md`
15. `projects/_template/connections/stakeholders.md`
16. `projects/_template/capabilities/README.md`
17. `projects/_template/cadence/daily-focus.md`
18. `context/role-profile.md`
19. `roles/README.md`

## Suggested new-session prompt

```text
Please load the project handoff from:
/mnt/hermes-workspace/delivery-lead-ai-os-starter/TASK-HANDOFF.md

Then inspect the project state and continue from my latest instruction. Wave 1 through Wave 7 Copilot skills should be present on `main`; verify the latest git status and remote history before making new changes.
```

## Current git state

The reusable template, Wave 1 through Wave 7 Copilot skill library, and restoration of the handoff/planning files have been committed and pushed to GitHub.

Repository:

```text
https://github.com/aastillero/ai-os-template
```

Branch and remote:

```text
Local branch: main
Remote branch: origin/main
Remote URL: https://github.com/aastillero/ai-os-template.git
```

Current published commits:

```text
RESTORE_COMMIT_PENDING chore: restore handoff and migration plan files
Full SHA: RESTORE_COMMIT_PENDING

2c82121 chore: ignore local skill migration plan
Full SHA: 2c8212111430e2e303c70629f2f7c9afd9692e6b

3c78663 chore: ignore local task handoff
Full SHA: 3c78663944fbd820155221637666159ddab99dc1

bffcd59 [verified] feat: add Copilot skill library
Full SHA: bffcd59dad11f15893015ece3062521ef7145f0d

5bd5adf feat: initialize role AI OS template
Full SHA: 5bd5adffc086e6432728cedd9293761e67ccc8c2
```

Current repository hygiene:

```text
TASK-HANDOFF.md is tracked and present in HEAD/origin/main.
SKILLS-MIGRATION-PLAN.md is tracked and present in HEAD/origin/main.
.gitignore has no rules for either file.
```

When resuming, verify the actual latest state instead of relying on this file alone:

```bash
git fetch origin main
git status --short --branch
git log --oneline -5 --decorate origin/main
git check-ignore -v TASK-HANDOFF.md SKILLS-MIGRATION-PLAN.md || true
git ls-files -- TASK-HANDOFF.md SKILLS-MIGRATION-PLAN.md
git ls-tree -r --name-only origin/main | grep -E '^(TASK-HANDOFF|SKILLS-MIGRATION-PLAN)\.md$'
```

Expected current output summary:

```text
## main...origin/main
RESTORE_COMMIT_PENDING (origin/main, main) chore: restore handoff and migration plan files
TASK-HANDOFF.md
SKILLS-MIGRATION-PLAN.md
# no check-ignore output for either file
```

## Verification commands for the next session

From the project root:

```bash
python3 - <<'PY'
from pathlib import Path
import re
root = Path('.')
skills_dir = root / '.github' / 'skills'
skills = sorted(skills_dir.glob('*/SKILL.md'))
all_text = '\n'.join(p.read_text(encoding='utf-8') for p in skills)
print('SKILL_MD_COUNT=' + str(len(list(root.rglob('SKILL.md')))))
print('ROOT_SKILL_MD_COUNT=' + str(len(skills)))
print('TEMPLATE_COUNT=' + str(len(list(skills_dir.glob('*/templates/*.md')))))
print('REFERENCE_COUNT=' + str(len(list(skills_dir.glob('*/references/*.md')))))
print('ROOT_SKILLS=' + ','.join(p.parent.name for p in skills))
print('PLAN_EXISTS_LOCAL=' + str((root / 'SKILLS-MIGRATION-PLAN.md').exists()))
print('HANDOFF_EXISTS_LOCAL=' + str((root / 'TASK-HANDOFF.md').exists()))
import subprocess
tracked = subprocess.check_output(['git', 'ls-files', '--', 'TASK-HANDOFF.md', 'SKILLS-MIGRATION-PLAN.md'], text=True).strip().splitlines()
print('HANDOFF_AND_PLAN_TRACKED=' + str(set(tracked) == {'TASK-HANDOFF.md', 'SKILLS-MIGRATION-PLAN.md'}))
ignored = [subprocess.run(['git', 'check-ignore', '-q', p], stdout=subprocess.DEVNULL, stderr=subprocess.DEVNULL).returncode == 0 for p in ['TASK-HANDOFF.md', 'SKILLS-MIGRATION-PLAN.md']]
print('HANDOFF_AND_PLAN_IGNORED=' + str(any(ignored)))
print('NO_ALLOWED_TOOLS=' + str('allowed-tools' not in all_text and 'allowed_tools' not in all_text))
print('HAS_CLAUDE_DIR=' + str((root / '.claude').exists()))
print('HAS_CODEX_DIR=' + str((root / '.codex').exists()))
print('HAS_AGENTS_DIR=' + str((root / '.agents').exists()))
PY
```

Expected current output summary:

```text
SKILL_MD_COUNT=28
ROOT_SKILL_MD_COUNT=28
TEMPLATE_COUNT=28
REFERENCE_COUNT=12
PLAN_EXISTS_LOCAL=True
HANDOFF_EXISTS_LOCAL=True
HANDOFF_AND_PLAN_TRACKED=True
HANDOFF_AND_PLAN_IGNORED=False
NO_ALLOWED_TOOLS=True
HAS_CLAUDE_DIR=False
HAS_CODEX_DIR=False
HAS_AGENTS_DIR=False
```

Latest verification output after Wave 1 through Wave 7 migration:

```text
VALIDATION_RESULT=PASS
ROOT_SKILL_MD_COUNT=28
ALL_SKILL_MD_COUNT=28
TEMPLATE_COUNT=28
REFERENCE_COUNT=12
ROOT_SKILLS=decision-record,delivery-infographic,delivery-plan,delivery-status-report,dependency-map,document-intake,evidence-review,executive-briefing,github-issue-triage,linear-board-review,meeting-prep-and-follow-up,pdf-export,pdf-review-and-edit,powerpoint-deck-draft,powerpoint-deck-edit,presentation-outline,project-kickoff,qa-and-acceptance-review,raid-review,release-readiness-review,requirements-to-plan,roadmap-communication,scope-change-review,stakeholder-update,teams-meeting-synthesis,weekly-delivery-review,word-document-draft,word-document-edit
ROOT_SKILLS_MATCH_EXPECTED=True
FRONTMATTER_OK=True
NO_ALLOWED_TOOLS=True
NO_FORBIDDEN_DIRS=True
PLAN_HAS_WAVE7=True
```

## Remaining work / likely next steps

Follow the user's latest instruction and verify current git state first.

1. Repository restore is complete as of `RESTORE_COMMIT_PENDING`; verify live state before any new edits.
2. Optionally test the template by copying `projects/_template/` to a sample project and opening it as a direct project workspace.
3. Later, test adaptation by creating another role pack, for example Product Owner or QA Lead.
4. Keep `TASK-HANDOFF.md` and `SKILLS-MIGRATION-PLAN.md` tracked unless the user explicitly asks to remove/version them differently.

## Final review notes

Final review before commit/push found and resolved two publication blockers:

1. Root docs still described `.github/skills/` as future-only or empty. Updated `README.md`, `WORKSPACE.md`, `.github/copilot-instructions.md`, and `AGENTS.md` to reflect the approved role-level skill library.
2. Six Wave 1 skills had less explicit standalone guardrails. Standardized their boundaries to require repository/user-provided context only, no invented facts, no secrets, and no commands/APIs/live integrations by default.

Post-publish repository hygiene clarification:

1. `TASK-HANDOFF.md` was briefly removed from tracking and added to `.gitignore` in `3c78663944fbd820155221637666159ddab99dc1`.
2. `SKILLS-MIGRATION-PLAN.md` was briefly removed from tracking and added to `.gitignore` in `2c8212111430e2e303c70629f2f7c9afd9692e6b`.
3. User clarified that both files should be added back to the repository; the restoration commit removes those ignore rules and tracks both files again.

## Blockers

None currently.

## Pitfalls to avoid

- Do not rebuild the project from scratch; the scaffold already exists.
- Do not accidentally convert this into a Claude/Codex project.
- Do not add `allowed-tools`, scripts, or live integrations by default.
- Do not overfit all documents to Delivery Lead; this must remain portable to other roles.
- Do not rely on memory alone; read the project files before editing.
- Do not reintroduce the old flat project template unless the user explicitly prefers it.
- Do not put project-specific facts only in the root workspace; project focus mode depends on project-local context.
- Do not treat direct PDF editing, `.docx` or `.pptx` binary editing/generation, GitHub API access, Teams/Graph access, or Linear API access as default skill requirements.
- Do not re-remove `TASK-HANDOFF.md` or `SKILLS-MIGRATION-PLAN.md` from Git tracking unless the user explicitly asks for that again.

## Handoff update rule

When meaningful project decisions or structural changes are made, update this file before ending the session so the next session can resume without rework.
