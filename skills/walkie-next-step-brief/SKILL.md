---
name: walkie-next-step-brief
description: Optional companion skill for turning prior session history and current repo context into a short engineering brief with the best next debugging or implementation step.
---

# Walkie Next-Step Brief

Use this skill when the user needs a short, actionable brief rather than raw retrieval results.

Treat this as a secondary work-history workflow, not Walkie's primary storefront pitch.

## Core job

Produce a brief that says:

- what matters from history
- what code area is implicated
- what the best next action is
- what uncertainty remains

## Workflow

1. Start from the question and retrieve relevant sessions.
2. Keep only evidence that changes the next action.
3. Cross-check the likely code area with the attached repo snapshot.
4. Distill to one or two highest-value next steps.
5. Keep uncertainty visible.

## Output shape

- `summary`
- `prior_attempts`
- `relevant_files`
- `recommended_next_steps`
- `uncertainties`

## Guardrails

- Do not restate the full history if it does not change the next action.
- Avoid broad brainstorming.
- A short specific brief is better than a long vague one.

## Walkie integration

- Best used after bug recall or stale-attempt synthesis.
- Good fit for `walkie agent preview` or a later private invoke endpoint.
