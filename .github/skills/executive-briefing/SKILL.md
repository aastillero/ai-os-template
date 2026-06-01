---
name: executive-briefing
description: "Drafts executive delivery briefings. Use when preparing sponsor updates, steering committee notes, executive summaries, decision briefs, escalation summaries, portfolio-level updates, or concise leadership narratives from delivery context."
---

## Purpose

Help a Delivery Lead convert project detail into an executive-ready narrative that emphasizes outcomes, risks, decisions, and asks.

## When to use this skill

Use this skill when the user asks for:

- executive briefing
- steering committee update
- sponsor update
- decision brief
- escalation summary
- leadership narrative
- portfolio-level delivery update

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`
- `projects/<project-name>/connections/stakeholders.md`
- audience and desired decision or ask

## Process

1. Identify the executive audience and what they need to decide or understand.
2. Lead with outcome, status, and material change since last update.
3. Surface only the few risks, trade-offs, and decisions that need leadership attention.
4. Translate delivery detail into business impact.
5. Make asks explicit and time-bound when evidence supports timing.
6. Keep tone calm, concise, and reviewable.

## Output format

```markdown
# Executive Briefing — <Project / Topic>

## Purpose

## Executive summary

## Current status

## Material changes since last update

## Key risks or trade-offs

## Decisions / asks

| Ask / decision | Why it matters | Needed by | Owner / approver |
|---|---|---|---|
|  |  |  |  |

## Recommended message

## Assumptions / missing inputs
```

## Quality checklist

- Brief is short enough for executives.
- Business impact is clear.
- Asks and decisions are explicit.
- No unverified commitments are presented as facts.
- Risks are framed with options or next actions.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
