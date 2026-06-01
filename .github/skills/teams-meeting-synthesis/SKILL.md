---
name: teams-meeting-synthesis
description: "Synthesizes pasted or exported meeting transcripts. Use when turning Teams, Zoom, Meet, or meeting notes into summaries, decisions, risks, blockers, action items, follow-ups, stakeholder messages, or project record updates."
---

## Purpose

Help a Delivery Lead turn meeting transcripts or notes into usable delivery outputs while staying independent of Microsoft Teams, Graph, or any live meeting integration.

## When to use this skill

Use this skill when the user asks for:

- meeting transcript synthesis
- meeting notes cleanup
- action item extraction
- decision and blocker capture
- follow-up email drafting
- project record update after a meeting

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- pasted/exported transcript or meeting notes
- meeting title, date, and attendees if known
- meeting objective or agenda
- `projects/<project-name>/connections/meetings.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`

## Process

1. Identify meeting purpose, participants, and timeframe.
2. Summarize outcomes in plain language, not a chronological transcript recap.
3. Extract decisions, action items, blockers, risks, dependencies, and questions.
4. Distinguish confirmed commitments from discussion ideas.
5. Assign owners and dates only when explicitly stated.
6. Suggest project-file updates without assuming permission to edit them unless asked.

## Output format

```markdown
# Meeting Synthesis — <Meeting Name> — <Date>

## Meeting purpose

## Short summary

## Decisions made

| Decision | Owner / approver | Evidence | Follow-up |
|---|---|---|---|
|  |  |  |  |

## Action items

| Action | Owner | Due / trigger | Notes |
|---|---|---|---|
|  |  |  |  |

## Risks / blockers / dependencies

| Type | Item | Impact | Next step |
|---|---|---|---|
| Risk / Issue / Dependency |  |  |  |

## Stakeholder follow-up draft

## Project record updates to consider

## Open questions / missing inputs
```

## Quality checklist

- Summary focuses on outcomes, not transcript noise.
- Actions and owners are evidenced.
- Decisions are not confused with proposals.
- Sensitive/personnel content is minimized.
- Follow-up draft is marked reviewable, not sent.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
