---
name: stakeholder-update
description: Drafts stakeholder-facing delivery communications. Use when preparing stakeholder updates, escalation notes, decision requests, expectation-setting messages, timeline change notes, project emails, or communication drafts from project context.
---

## Purpose

Help a Delivery Lead produce clear, reviewable stakeholder communication that is factual, calm, and action-oriented.

## When to use this skill

Use this skill when the user asks for:

- stakeholder update
- escalation note
- decision request
- project email draft
- expectation-setting message
- change/timeline communication
- concise update for leadership or cross-functional partners

## Inputs to gather

Look for available context in:

- `projects/<project-name>/connections/stakeholders.md`
- `projects/<project-name>/connections/communication-map.md`
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/context/decisions.md`
- user-provided audience, tone, and message goal

## Process

1. Identify the audience, desired outcome, and communication channel.
2. Separate what happened, why it matters, what is needed, and by when.
3. Make the ask or decision explicit.
4. Keep the tone calm, accountable, and concise.
5. Avoid blame, vague urgency, or unsupported certainty.
6. Offer a short version first when the audience is executive or time-constrained.

## Output format

```markdown
# Stakeholder Update Draft

## Audience

## Goal of message

## Short version

## Draft

Subject: <subject>

Hi <name/team>,

<context>

<current status / impact>

<decision, ask, or next step>

Thanks,
<sender>

## Notes for reviewer

- Assumptions:
- Missing inputs:
- Suggested follow-up:
```

## Quality checklist

- The audience and desired outcome are clear.
- The message states the ask or decision needed.
- The draft does not overpromise or hide risk.
- Dates, owners, and commitments are supported by context.
- The tone fits the stakeholder relationship.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not send messages or take external action.
- Do not invent approvals, commitments, dates, stakeholder positions, customer impact, or delivery outcomes.
- Produce reviewable drafts only.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
