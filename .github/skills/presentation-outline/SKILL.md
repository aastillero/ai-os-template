---
name: presentation-outline
description: "Builds presentation outlines. Use when creating slide narratives, executive deck outlines, steering committee presentations, project updates, release readiness decks, kickoff decks, or communication storylines without requiring deck-generation tools."
---

## Purpose

Help a Delivery Lead produce a clear slide-by-slide story outline that can be copied into any presentation tool.

## When to use this skill

Use this skill when the user asks for:

- presentation outline
- deck storyline
- slide narrative
- executive deck
- steering committee presentation
- kickoff presentation
- release readiness deck

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- presentation objective and audience
- available project context or source notes
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/stakeholders.md`

## Process

1. Clarify presentation goal, audience, length, and desired decision/response.
2. Define a narrative arc: context, current state, key points, risks/decisions, ask, next steps.
3. Create a slide-by-slide outline with message, content, and speaker notes.
4. Keep each slide focused on one main idea.
5. Identify where data, diagrams, or approvals are needed.
6. Provide optional title alternatives if useful.

## Output format

```markdown
# Presentation Outline — <Topic>

## Audience and objective

## Recommended storyline

1. Context
2. Current state
3. Key updates / options
4. Risks / decisions
5. Ask / next steps

## Slide outline

| Slide | Title | Main message | Content bullets | Visual idea | Speaker notes |
|---:|---|---|---|---|---|
| 1 |  |  |  |  |  |

## Data or approvals needed

## Short talk track
```

## Quality checklist

- Each slide has one main message.
- The narrative leads to a clear ask or decision.
- Data gaps are flagged.
- No deck-generation tool is required.
- Speaker notes help the presenter explain trade-offs.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
