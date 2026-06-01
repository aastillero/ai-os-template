---
name: powerpoint-deck-draft
description: "Drafts PowerPoint-ready deck content. Use when creating slide decks, presentation drafts, executive decks, steering committee decks, kickoff decks, release readiness decks, stakeholder presentations, speaker notes, or slide-by-slide storyboards without requiring pptx tooling by default."
---

## Purpose

Help a Delivery Lead create a PowerPoint-ready deck storyboard with slide titles, message hierarchy, content bullets, speaker notes, and visual direction while keeping the default workflow Markdown-first and tool-neutral.

## When to use this skill

Use this skill when the user asks for:

- PowerPoint deck draft
- presentation draft
- executive deck or steering committee deck
- kickoff or release readiness presentation
- slide-by-slide storyboard
- speaker notes or talk track
- deck content that may later become a `.pptx` file

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- presentation objective, audience, and desired decision or response
- target length or number of slides, if known
- available project context or source notes
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/stakeholders.md`
- brand, tone, visual, accessibility, or template constraints if provided

## Process

1. Clarify audience, purpose, decision/ask, desired length, and presentation setting.
2. Build a storyline with a clear arc: context, current state, key message, risks/trade-offs, decisions or asks, and next steps.
3. Create slide-by-slide content with one primary message per slide.
4. Include speaker notes or talk track for slides that need executive framing.
5. Add visual direction such as chart, timeline, process flow, status cards, dependency map, or callout without requiring a design tool.
6. Flag missing facts, data, approvals, or branding inputs instead of inventing them.
7. Keep actual `.pptx` generation optional and outside the default skill path.

## Output format

```markdown
# PowerPoint Deck Draft — <Deck Title>

## Audience and objective

- Audience:
- Purpose:
- Desired decision / response:
- Target length:

## Storyline

1. Context
2. Current state
3. Key update / options
4. Risks, trade-offs, or decisions
5. Ask and next steps

## Slide-by-slide draft

| Slide | Title | Primary message | Content bullets | Visual direction | Speaker notes |
|---:|---|---|---|---|---|
| 1 |  |  |  |  |  |

## Optional appendix slides

| Slide | Purpose | Content |
|---:|---|---|
|  |  |  |

## Data, design, or approval gaps

## Review checklist

- [ ] One main message per slide
- [ ] Audience and ask are clear
- [ ] Claims are evidence-backed
- [ ] Missing inputs are flagged
- [ ] Content is ready to paste into PowerPoint or an approved deck template
```

## Quality checklist

- The deck has a clear audience, purpose, and ask.
- Each slide has one primary message.
- Slide content is concise enough for a deck, not a long report.
- Visual direction is tool-neutral and implementable.
- Speaker notes help explain trade-offs where needed.
- Actual `.pptx` creation is not assumed by default.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, release decisions, deck content, or design approvals.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, generate binary `.pptx` files, or depend on external tools by default.
