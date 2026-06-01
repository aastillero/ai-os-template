---
name: powerpoint-deck-edit
description: "Edits PowerPoint deck content from pasted or extracted slide text. Use when reviewing or improving existing decks, slide order, executive readability, speaker notes, stakeholder tone, visual consistency, missing slides, title/action clarity, or `.pptx`-originated content without directly editing pptx binaries by default."
---

## Purpose

Help a Delivery Lead review and improve PowerPoint-originated content using pasted or extracted slide text, while keeping direct binary `.pptx` editing optional and outside the default workflow.

## When to use this skill

Use this skill when the user asks for:

- PowerPoint deck edit
- existing deck review
- slide content rewrite
- executive readability pass
- speaker notes edit
- deck structure and slide order review
- stakeholder presentation polish
- PowerPoint or `.pptx` content pasted as text

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- pasted or extracted slide text
- deck purpose, audience, and desired response
- current slide order and slide titles if available
- known template, brand, tone, or format constraints
- review focus: structure, tone, clarity, completeness, executive polish, visuals, or speaker notes
- project context files if the deck is tied to a project

## Process

1. Identify the deck purpose, audience, review objective, and current slide structure.
2. Assess storyline, slide order, clarity of ask, executive readability, and whether each slide has one main message.
3. Flag missing slides, duplicated slides, over-dense slides, unsupported claims, unclear decisions, and weak transitions.
4. Rewrite titles, content bullets, and speaker notes while preserving confirmed facts and commitments.
5. Separate content edits from visual/layout recommendations.
6. Provide a slide-by-slide edit plan or revised slide content depending on the request.
7. Keep direct `.pptx` manipulation optional and do not imply the binary file was edited unless the user explicitly uses an approved editing workflow.

## Output format

```markdown
# PowerPoint Deck Edit — <Deck Title>

## Edit objective

## Deck-level findings

- Storyline:
- Audience fit:
- Ask / decision clarity:
- Evidence gaps:

## Slide-by-slide review

| Slide | Current issue | Recommended edit | Revised title / message | Notes |
|---:|---|---|---|---|
| 1 |  |  |  |  |

## Revised slide content

### Slide <N>: <Title>

Primary message:

Bullets:

Speaker notes:

Visual/layout recommendation:

## Suggested slide order changes

## Missing slides or appendices

## Fact checks / unresolved questions

## Change notes for reviewer
```

## Quality checklist

- Deck purpose and audience are explicit.
- Storyline and ask are clearer after edits.
- Slide edits preserve confirmed facts and commitments.
- Unsupported claims are flagged.
- Content and layout recommendations are separated.
- Direct binary `.pptx` editing is not assumed by default.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, release decisions, deck content, or design approvals.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, generate binary `.pptx` files, or depend on external tools by default.
