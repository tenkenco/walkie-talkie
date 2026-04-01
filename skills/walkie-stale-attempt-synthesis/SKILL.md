---
name: walkie-stale-attempt-synthesis
description: Optional companion skill for identifying which old advice still applies, which parts drifted, and what should not be retried blindly.
---

# Walkie Stale-Attempt Synthesis

Use this skill when the important question is not just "what happened before?" but "which of that still matters now?"

Use it only when stale prior work is the issue. Do not use it for public agent onboarding, storefront discovery, or TOML deployment guidance.

## Core job

Answer:

- which prior attempts still look relevant
- which prior attempts may be stale
- why they may be stale
- what current repo areas should be checked before retrying an old fix

## Workflow

1. Retrieve prior sessions about the issue or module.
2. Extract explicit prior attempts and assumptions.
3. Cross-check likely files/modules against the attached repo snapshot.
4. Flag mismatches, drift, or uncertainty.
5. Recommend the smallest verification step before retrying anything.

## Output shape

- `summary`
- `prior_attempts`
- `possibly_stale_attempts`
- `relevant_files`
- `current_hypothesis`
- `recommended_next_steps`
- `uncertainties`

## Guardrails

- Never claim current-code mismatch unless there is real evidence.
- Prefer "may be stale because..." over confident unsupported claims.
- If no repo snapshot is attached, explicitly say stale-attempt detection is limited.

## Walkie integration

- This skill depends most heavily on repo bootstrap + reindex.
- Use debug preview mode to verify whether answers rely on repo-backed evidence or only session recall.
