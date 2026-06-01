---
name: delivery-status-report
description: Drafts clear delivery status updates. Use when preparing weekly stakeholder updates, delivery reports, sprint summaries, project health summaries, RAG status notes, milestone updates, or executive delivery updates from repository project context.
---

## Purpose

Help a Delivery Lead turn project context into a clear, evidence-grounded status update.

## When to use this skill

Use this skill when the user asks for:

- weekly status updates
- project or workstream health reports
- RAG status summaries
- sprint or milestone updates
- executive delivery updates
- stakeholder-facing progress summaries

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- `templates/status-update.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/stakeholders.md`
- user-provided notes or pasted context

If key facts are missing, list the missing inputs instead of inventing them.

## Process

1. Identify the audience and reporting period.
2. Summarize the current delivery health as Green, Amber, or Red only when evidence supports it.
3. Separate facts from interpretation.
4. Pull out progress, risks/blockers, decisions needed, next milestones, and asks.
5. Keep the tone calm, clear, and action-oriented.
6. Make ownership and decisions explicit where known.
7. If the user needs external-facing copy, produce a reviewable draft, not a sent message.

## Output format

Use this structure by default:

```markdown
# <Project or Workstream> — Status Update — <Date or Period>

## Summary

Overall status: Green / Amber / Red / Unknown

One-sentence summary:

## Progress

-

## Risks / blockers

-

## Decisions needed

-

## Next milestones

-

## Ask

-

## Assumptions / missing inputs

-
```

## Quality checklist

- Status label is supported by evidence.
- No invented dates, owners, commitments, approvals, or stakeholder positions.
- Risks and blockers are specific enough to act on.
- Decisions needed and asks are explicit.
- The update is concise enough for the intended audience.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not claim a project is on track, blocked, approved, accepted, released, or tested unless the available context supports it.
- If evidence is incomplete, say so directly and label the status as unknown where appropriate.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
