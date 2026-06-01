---
name: meeting-prep-and-follow-up
description: Prepares delivery meetings and follow-ups. Use when creating agendas, meeting prep notes, decision lists, action item summaries, follow-up emails, meeting notes, or delivery meeting outcomes from project context.
---

## Purpose

Help a Delivery Lead prepare useful meetings and convert meeting outcomes into actions, decisions, risks, and follow-up communication.

## When to use this skill

Use this skill when the user asks for:

- meeting agenda
- meeting prep
- delivery review prep
- stakeholder meeting prep
- follow-up summary
- action item list
- decision capture
- meeting notes cleanup

## Inputs to gather

Look for available context in:

- `templates/meeting-prep.md`
- `projects/<project-name>/connections/meetings.md`
- `projects/<project-name>/connections/stakeholders.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`
- user-provided notes, transcript excerpts, or meeting goals

## Process

Choose the mode based on the user request.

### Prep mode

1. Identify meeting name, audience, date, and desired outcome.
2. Summarize the context everyone needs.
3. Propose agenda topics in priority order.
4. List decisions needed, risks/blockers to raise, and materials to bring.
5. Define how outcomes should be captured.

### Follow-up mode

1. Extract decisions, actions, owners, due dates, risks, and open questions.
2. Separate confirmed outcomes from assumptions.
3. Draft a concise follow-up note.
4. Identify updates needed in project files such as status, RAID, decisions, or work plan.

## Output format

```markdown
# Meeting Prep / Follow-up — <Meeting name>

## Desired outcome

## Context

## Agenda / topics

1.
2.
3.

## Decisions needed or captured

| Decision | Owner | Required by / decided on | Notes |
|---|---|---|---|
|  |  |  |  |

## Actions

| Action | Owner | Due | Source / note |
|---|---|---|---|
|  |  |  |  |

## Risks / blockers

-

## Follow-up draft

## Missing inputs

-
```

## Quality checklist

- Every action has an owner or is flagged as missing one.
- Decisions are distinct from discussion points.
- Follow-up is concise and reviewable.
- Risks/blockers are visible.
- Missing dates, owners, or context are called out.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent attendance, decisions, owners, due dates, commitments, or stakeholder positions.
- Do not claim a meeting outcome occurred unless the user provided evidence.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
