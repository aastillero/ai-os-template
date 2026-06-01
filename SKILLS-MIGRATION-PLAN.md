# Standalone Copilot Skills Plan

Last updated: 2026-06-01T07:50:44+00:00

Status: Wave 1 through Wave 7 skill migration is implemented locally; pending human review, commit, and push.

## Purpose

This file defines the standalone GitHub Copilot skill roadmap for the Delivery Lead AI OS starter workspace.

The Delivery Lead AI OS starter must work when someone clones this repository and opens it directly in GitHub Copilot. Skills must not depend on any private agent workspace, agent memory, internal session history, cron jobs, MCP tools, local CLIs, private credentials, or hidden automations.

The only acceptable default dependencies are:

1. Files already in this repository.
2. Markdown instructions.
3. Templates in this repository.
4. User-provided project context.
5. GitHub Copilot's normal ability to read and edit the workspace.

Target root skill location:

```text
.github/skills/<skill-name>/SKILL.md
```

Future project-specific skills may live in:

```text
projects/<project-name>/.github/skills/<skill-name>/SKILL.md
```

## Current constraints and guardrails

1. This repository is GitHub Copilot-native only.
2. Do not create `.claude/`, `.codex/`, or `.agents/` folders.
3. Keep root skills role-level and reusable across projects.
4. Project folders must remain usable as standalone mini AI OS workspaces.
5. Prefer Markdown-first skills: `SKILL.md`, optional `references/`, and optional `templates/`.
6. Do not add `allowed-tools: shell`, `allowed-tools: bash`, background jobs, browser automation, API clients, or live integrations by default.
7. Do not store secrets, credentials, private customer data, or sensitive employee data in skills, templates, examples, or references.
8. Skill descriptions must be trigger-rich because Copilot uses the description to decide when to activate a skill.
9. Integration-heavy capabilities should be split into two layers:
   - a skill that works from pasted/exported/user-provided content; and
   - a separate integration guide only if the user later wants live SaaS connectivity.
10. Document, PDF, and PowerPoint skills remain source-first by default. Actual `.docx`, `.pptx`, and PDF generation/editing/rendering belong in optional setup guidance unless the repository intentionally opts into those tools later.

## Standalone rule

A candidate skill can stay only if it can produce useful output from repository files and user-provided context.

Keep a skill when it can answer yes to all of these:

1. Can it work with normal Markdown files in this repository?
2. Can it work without private agent memory, internal tools, or session context?
3. Can it produce a useful Markdown/checklist/draft output without running code?
4. Is it a Delivery Lead capability, not internal agent operations?
5. If it mentions a tool or integration, can the skill still work from manually pasted/exported content?

Defer implementation details that require:

- live SaaS credentials or API permissions;
- OCR engines or document-processing pipelines;
- Microsoft Graph/Teams integration;
- visual/image generation engines;
- repository automation or issue API calls;
- direct binary `.docx`, `.pptx`, or PDF editing/generation.

Those can become optional integration guides later, not default skill requirements.

## Approved candidate list

These are the current standalone Copilot skills migrated into `.github/skills/`.

| # | Candidate skill | Status | Dependency stance |
|---:|---|---|---|
| 1 | `delivery-status-report` | Wave 1 implemented locally | Standalone Markdown/repo context. |
| 2 | `raid-review` | Wave 1 implemented locally | Standalone Markdown/repo context. |
| 3 | `delivery-plan` | Wave 1 implemented locally | Standalone Markdown/repo context. |
| 4 | `stakeholder-update` | Wave 1 implemented locally | Standalone Markdown/repo context. |
| 5 | `meeting-prep-and-follow-up` | Wave 1 implemented locally | Standalone Markdown/repo context. |
| 6 | `decision-record` | Wave 1 implemented locally | Standalone Markdown/repo context. |
| 7 | `document-intake` | Wave 2 implemented locally | Skill works from pasted/extracted content; OCR setup is optional integration guidance. |
| 8 | `teams-meeting-synthesis` | Wave 2 implemented locally | Skill works from pasted/exported transcript; Teams/Graph setup is optional integration guidance. |
| 9 | `dependency-map` | Wave 2 implemented locally | Standalone Markdown/repo context. |
| 10 | `weekly-delivery-review` | Wave 2 implemented locally | Standalone Markdown/repo context and cadence files. |
| 11 | `requirements-to-plan` | Wave 2 implemented locally | Standalone from user-provided requirements and project context. |
| 12 | `release-readiness-review` | Wave 2 implemented locally | Standalone from project/release evidence. |
| 13 | `delivery-infographic` | Wave 3 implemented locally | Skill outputs an infographic brief/spec; design tooling is optional guidance. |
| 14 | `executive-briefing` | Wave 3 implemented locally | Standalone Markdown/executive narrative. |
| 15 | `roadmap-communication` | Wave 3 implemented locally | Standalone Markdown/stakeholder narrative. |
| 16 | `presentation-outline` | Wave 3 implemented locally | Standalone slide/story outline; no deck generator required. |
| 17 | `word-document-draft` | Wave 3 implemented locally | Standalone Word-ready Markdown/content draft; `.docx` generation tooling is optional guidance. |
| 18 | `word-document-edit` | Wave 3 implemented locally | Standalone edit plan/rewrite from pasted or extracted Word content; actual `.docx` editing tooling is optional guidance. |
| 19 | `pdf-export` | Wave 3 implemented locally | Standalone PDF-ready source/spec output; PDF rendering tools are optional guidance. |
| 20 | `qa-and-acceptance-review` | Wave 4 implemented locally | Standalone from QA/acceptance evidence. |
| 21 | `scope-change-review` | Wave 4 implemented locally | Standalone from project context and proposed change. |
| 22 | `evidence-review` | Wave 4 implemented locally | Standalone evidence check against available files and user-provided evidence. |
| 23 | `project-kickoff` | Wave 4 implemented locally | Standalone using `projects/_template/`. |
| 24 | `github-issue-triage` | Wave 5 implemented locally | Works from pasted/exported issue lists; live GitHub API is optional/deferred. |
| 25 | `pdf-review-and-edit` | Wave 6 implemented locally | Works from pasted/extracted PDF text; direct PDF editing tooling is optional/deferred. |
| 26 | `linear-board-review` | Wave 6 implemented locally | Works from pasted/exported board data; live Linear API is optional/deferred. |
| 27 | `powerpoint-deck-draft` | Wave 7 implemented locally | Standalone PowerPoint-ready Markdown/storyboard content; `.pptx` generation tooling is optional guidance. |
| 28 | `powerpoint-deck-edit` | Wave 7 implemented locally | Standalone edit plan/rewrite from pasted or extracted deck content; actual `.pptx` editing tooling is optional guidance. |

## Optional integration guides, not default skill requirements

These can be added as `references/` docs or repo setup guides later. They should not block the core skills.

```text
teams-integration-guide
ocr-document-processing-guide
design-infographic-system
docx-generation-guide
docx-editing-guide
pdf-export-guide
pdf-review-and-edit-guide
github-api-triage-guide
linear-api-board-guide
pptx-generation-guide
pptx-editing-guide
```

## Wave model

### Wave 0 — Governance and filtering

Status: complete.

Outcome:

- Confirmed GitHub Copilot-native skill location.
- Removed private-agent and internal-workspace dependencies.
- Split standalone skills from optional integrations.
- Confirmed the standalone candidate list.

### Wave 1 — Starter Delivery Lead skills

Status: implemented locally; pending review/commit.

Skills:

```text
delivery-status-report
raid-review
delivery-plan
stakeholder-update
meeting-prep-and-follow-up
decision-record
```

Goal: make the AI OS immediately useful for normal Delivery Lead operating work: status, risk, planning, stakeholder communication, meetings, and decisions.

### Wave 2 — High-value expansions

Status: implemented locally; pending review/commit.

```text
document-intake
teams-meeting-synthesis
dependency-map
weekly-delivery-review
requirements-to-plan
release-readiness-review
```

Notes:

- `document-intake` works from pasted/extracted text first. OCR tooling belongs in optional setup guidance.
- `teams-meeting-synthesis` works from pasted/exported transcript text first. Microsoft Graph integration belongs in optional setup guidance.

### Wave 3 — Document, visual, and executive communication

Status: implemented locally; pending review/commit.

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

- `delivery-infographic` defaults to an infographic brief/spec that a user or design tool can implement.
- Design guidance remains repo-local and tool-neutral.
- `word-document-draft` defaults to Word-ready Markdown/content structure before any `.docx` binary generation.
- `word-document-edit` works from pasted or extracted document text first; direct `.docx` editing belongs in optional setup guidance.
- `pdf-export` defaults to a PDF-ready source document or export spec; actual rendering via Pandoc, LibreOffice, WeasyPrint, Playwright, ReportLab, or similar tools is optional guidance.

### Wave 4 — Optional deeper delivery control

Status: implemented locally; pending review/commit.

```text
qa-and-acceptance-review
scope-change-review
evidence-review
project-kickoff
```

### Wave 5 — Tool-specific delivery workflows

Status: implemented locally; pending review/commit.

```text
github-issue-triage
```

Notes:

- `github-issue-triage` works from pasted/exported issue data first.
- Live GitHub API access or issue updates belong in optional setup guidance, not the default skill.

### Wave 6 — Source-first deferred adapters

Status: implemented locally; pending review/commit.

This wave was added when the user asked to migrate waves 2 through 6. The prior plan had only five waves, so the previously deferred/source-first candidates were promoted into a sixth standalone wave without adding live integrations.

```text
pdf-review-and-edit
linear-board-review
```

Notes:

- `pdf-review-and-edit` works from pasted or extracted PDF text first. Direct PDF binary editing is optional/deferred guidance.
- `linear-board-review` works from pasted/exported Linear-style board data first. Live Linear API access is optional/deferred guidance.

### Wave 7 — PowerPoint / deck production adapters

Status: implemented locally; pending review/commit.

This wave adds source-first PowerPoint support without making binary `.pptx` generation or editing a default requirement.

```text
powerpoint-deck-draft
powerpoint-deck-edit
```

Notes:

- `powerpoint-deck-draft` creates PowerPoint-ready Markdown/storyboard content, slide-by-slide copy, speaker notes, and visual direction. Actual `.pptx` generation belongs in optional guidance.
- `powerpoint-deck-edit` works from pasted or extracted deck text first. Direct `.pptx` binary editing belongs in optional guidance.

## Scrapped or not currently planned as skills

| Candidate | Decision | Reason |
|---|---|---|
| `project-handoff` | Not planned | Too close to internal session handoff. If needed later, create `delivery-transition-note` as a normal project transition workflow. |
| `incident-or-blocker-triage` | Not planned | Overlaps with `raid-review`, `release-readiness-review`, and `qa-and-acceptance-review`. |
| `google-workspace-draft-pack` | Not planned | Drafting is covered by communication skills; live Google integration is outside the starter scope. |
| `project-automation-candidate-review` | Not planned | Automation planning is AI OS improvement work, not Delivery Lead starter work. |
| `role-specific-variants` | Not a skill | Template governance, not a user workflow. |
| `project-specific-variants` | Not a skill | Template governance, not a user workflow. |
| `skill-consolidation` | Not a skill | Repository maintenance, not Delivery Lead workflow. |

## Standard Copilot skill shape

Each approved skill follows this basic shape:

```text
.github/skills/<skill-name>/
├── SKILL.md
├── references/
│   └── <optional-reference>.md
└── templates/
    └── <optional-template>.md
```

Minimal `SKILL.md` frontmatter example:

```markdown
---
name: delivery-status-report
description: "Drafts clear delivery status updates. Use when preparing weekly stakeholder updates, delivery reports, sprint summaries, project health summaries, or RAG status notes from project context."
---
```

Recommended body sections:

```markdown
## Purpose
## When to use this skill
## Inputs to gather
## Process
## Output format
## Quality checklist
## Boundaries
```

Boundaries for every skill:

1. Use only available repository context and user-provided information.
2. Do not invent dates, owners, commitments, blockers, approvals, or stakeholder positions.
3. If evidence is missing, list assumptions and questions.
4. Do not request or store secrets.
5. Do not run commands, call APIs, or depend on external tools by default.

## Validation before commit

Run from the repository root:

```bash
python3 - <<'PY'
from pathlib import Path
root = Path('.')
skills = sorted(p for p in (root / '.github' / 'skills').glob('*/SKILL.md'))
print('SKILL_MD_COUNT=' + str(len(list(root.rglob('SKILL.md')))))
print('ROOT_SKILL_MD_COUNT=' + str(len(skills)))
print('ROOT_SKILLS=' + ','.join(p.parent.name for p in skills))
print('HAS_CLAUDE_DIR=' + str((root / '.claude').exists()))
print('HAS_CODEX_DIR=' + str((root / '.codex').exists()))
print('HAS_AGENTS_DIR=' + str((root / '.agents').exists()))
print('PLAN_EXISTS=' + str((root / 'SKILLS-MIGRATION-PLAN.md').exists()))
PY
```

Expected current skill count after Wave 1 through Wave 7 migration:

```text
SKILL_MD_COUNT=28
ROOT_SKILL_MD_COUNT=28
```
