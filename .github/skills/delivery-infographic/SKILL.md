---
name: delivery-infographic
description: "Creates infographic-ready delivery briefs. Use when turning project status, roadmap, risks, milestones, release plans, dependency maps, or executive updates into a clear infographic spec, one-page visual brief, layout narrative, or designer-ready content plan."
---

## Purpose

Help a Delivery Lead produce a tool-neutral infographic brief that a human, designer, or approved design tool can turn into a visual artifact.

## When to use this skill

Use this skill when the user asks for:

- delivery infographic
- one-page visual summary
- executive visual brief
- roadmap visual
- risk or dependency visual
- designer-ready infographic spec

## Inputs to gather

Look for available context in:

- `context/role-profile.md`
- status, roadmap, milestone, risk, dependency, or release context
- `projects/<project-name>/context/status.md`
- `projects/<project-name>/context/work-plan.md`
- `projects/<project-name>/context/raid-log.md`
- `projects/<project-name>/connections/dependencies.md`
- audience, medium, and desired level of detail

## Process

1. Clarify audience, purpose, and key message.
2. Select a simple structure such as status snapshot, timeline, roadmap, RAID heatmap, dependency map, or before/after view.
3. Reduce content to the few most important facts and actions.
4. Specify layout, sections, hierarchy, labels, and callouts.
5. Flag data gaps and avoid visualizing unsupported claims.
6. Provide copy that is ready for a designer or tool-neutral implementation.

## Output format

```markdown
# Delivery Infographic Brief — <Topic>

## Audience and purpose

## Key message

## Recommended layout

- Format: one-page / slide / poster / dashboard panel
- Layout pattern: status snapshot / timeline / roadmap / RAID heatmap / dependency map / before-after

## Visual sections

| Section | Message | Data / content | Visual treatment |
|---|---|---|---|
|  |  |  |  |

## Copy blocks

## Data gaps / assumptions

## Review checklist
```

## Quality checklist

- Visual brief has a single main message.
- Every metric or claim is supported.
- Layout is tool-neutral.
- Sensitive details are excluded.
- A designer can implement from the spec.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent dates, owners, approvals, stakeholder positions, scope commitments, test results, or release decisions.
- If evidence is missing or stale, label the gap and ask for the smallest missing input.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
