---
name: decision-record
description: Creates and updates delivery decision records. Use when documenting project decisions, architecture/product/process trade-offs, stakeholder approvals, decision options, decision rationale, reversibility, follow-up actions, or decision logs from project context.
---

## Purpose

Help a Delivery Lead capture decisions clearly so future project work can understand what was decided, why, who owns it, and what would cause reconsideration.

## When to use this skill

Use this skill when the user asks for:

- decision record
- decision log entry
- ADR-style delivery decision
- options/trade-off summary
- stakeholder decision capture
- decision follow-up actions

## Inputs to gather

Look for available context in:

- `templates/decision-record.md`
- `decisions/log.md`
- `projects/<project-name>/context/decisions.md`
- `projects/<project-name>/context/current-state.md`
- `projects/<project-name>/connections/stakeholders.md`
- user-provided decision notes, options, rationale, and follow-ups

## Process

1. Identify the decision title and date if provided.
2. State the decision in one clear sentence.
3. Capture context and why the decision is needed now.
4. List options considered and trade-offs.
5. Identify owner, impacted stakeholders, and follow-up actions.
6. Note what would change or reopen the decision.
7. Flag missing rationale, owner, or approval evidence.

## Output format

```markdown
# Decision Record

## YYYY-MM-DD — <Decision title>

Decision:

Why:

Context:

Options considered:

Trade-offs:

Owner:

Impacted stakeholders:

What would change this decision:

Follow-up actions:

Assumptions / missing inputs:
```

## Quality checklist

- The decision is specific enough to be referenced later.
- Rationale and trade-offs are visible.
- Owner and impacted stakeholders are captured or flagged as missing.
- Follow-up actions are concrete.
- Missing approval/evidence is not hidden.

## Boundaries

- Use only repository context, pasted/exported content, and information the user provides.
- Do not invent approval, authority, consensus, dates, owners, commitments, or stakeholder positions.
- If a decision is only proposed, label it as proposed rather than decided.
- Do not request, store, or expose secrets, credentials, private keys, tokens, or unnecessary sensitive data.
- Do not run commands, call APIs, browse external systems, or depend on live integrations by default.
