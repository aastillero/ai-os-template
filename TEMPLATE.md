# Template Adaptation Guide

This repository should remain easy to translate into other role-specific AI OS workspaces.

The Delivery Lead setup is the first concrete role instance. Future roles should reuse the same core structure wherever possible.

## Design principle

Keep the reusable core stable and isolate role-specific assumptions.

The reusable model is based on the 4 C's:

- Context
- Connections
- Capabilities
- Cadence

Apply the 4 C's at two levels:

1. Root role-level workspace
2. Project/workstream-level workspaces under `projects/`

## Reusable core

- `.github/copilot-instructions.md`
- `AGENTS.md`
- `WORKSPACE.md`
- `context/personalization-intake.md`
- `context/operating-principles.md`
- `cadence/`
- `projects/_template/`
- `templates/`
- `references/ai-safety-and-boundaries.md`
- `.github/skills/` as the future role-level skill location

## Role-specific layer

- `context/role-profile.md`
- `roles/<role-name>/profile.md`
- role-specific language in cadence prompts
- role-specific project/workstream examples
- future role-specific skills in `.github/skills/`

## Project-specific layer

Each project copied from `projects/_template/` can also be opened directly as a standalone project workspace.

Project-specific files include:

- `projects/<project-name>/README.md`
- `projects/<project-name>/AGENTS.md`
- `projects/<project-name>/.github/copilot-instructions.md`
- `projects/<project-name>/.github/skills/`
- `projects/<project-name>/context/`
- `projects/<project-name>/connections/`
- `projects/<project-name>/capabilities/`
- `projects/<project-name>/cadence/`

## How to create another role edition

1. Create a role pack:

   ```text
   roles/<role-name>/profile.md
   ```

2. Use `roles/_template/profile.md` as the starting point.

3. Replace the active profile:

   ```text
   context/role-profile.md
   ```

4. Review the project/workstream template:

   ```text
   projects/_template/
   ```

   Keep the 4C project workspace pattern if the role manages projects, workstreams, accounts, programs, initiatives, or focus areas.

5. Review cadence prompts:

   ```text
   cadence/daily-startup.md
   cadence/weekly-review.md
   cadence/monthly-retro.md
   ```

   Replace Delivery Lead examples with the new role's daily, weekly, and monthly rhythms.

6. Review reusable templates:

   ```text
   templates/
   ```

   Keep generic templates. Add role-specific templates only when the role repeatedly produces that output.

7. Add Copilot skills later, not immediately.

   Skills should encode proven repeatable workflows. Do not create a skill until the manual workflow is useful and stable.

## Role profile fields

Every role profile should define:

- Role name
- Role family
- Purpose
- Outcomes the role is accountable for
- Common responsibilities
- Common work products
- Cadence/rhythm
- Stakeholders or collaborators
- Decision boundaries
- AI should help with
- AI should not do

## Project template checklist

Every project template should support:

- Context: project brief, current state, work plan, status, RAID, decisions, notes
- Connections: stakeholders, dependencies, systems/links, communication map, meetings
- Capabilities: workflows, prompts, skill backlog, future project-local skills
- Cadence: daily focus, weekly review, milestone checkpoint
- Direct-open mode: project-local `README.md`, `AGENTS.md`, and `.github/copilot-instructions.md`

## Portability checklist

Before copying this for another role, check:

- Does `README.md` explain this as a role edition, not a one-off?
- Does Copilot read the active role from `context/role-profile.md`?
- Are role-specific terms localized to role profile, cadence examples, and templates?
- Are project/workstream files named generically enough for the new role?
- Does `projects/_template/` still follow the 4C project workspace model?
- Can a copied project folder be opened directly as its own workspace?
- Are no `.claude/`, `.codex/`, or non-Copilot-specific structures introduced?
- Are there still zero `SKILL.md` files unless skills are intentionally being added?
