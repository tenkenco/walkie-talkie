# Walkie Bug-Recall Validation

This validation kit is for one product wedge:

`What did we already try for this bug/problem area, what files are involved, and what should we do next?`

The loop is intentionally narrow:

1. Sync or import real sessions.
2. Attach a fresh repo snapshot to a private agent.
3. Reindex the agent.
4. Ask bug-history questions.
5. Compare the answer against plain session search and plain repo/docs search.
6. Record whether the answer changed the next debugging step.

## Target Users

- You
- 3-5 close engineers working on real Walkie issues

## Success Criteria

- Trusted engineers use the flow repeatedly over 2 weeks, not as a one-off demo.
- Walkie is clearly better than plain repo/docs search on multiple real bug-history questions.
- Answers cite real prior attempts, plausible files, and a usable next step.
- Weak evidence produces `insufficient evidence` instead of confident filler.

## Guardrails

- Treat Hub, publish, and marketplace work as maintenance-only during validation.
- Do not expand into generic memory CRUD.
- Do not treat planning, prompt-writing, evaluation, or product-strategy sessions as bug-history evidence.
- Treat repo snapshot support as "fresh enough for validation", not dynamic live repo access.

## Core Answer Contract

Every answer should preserve these headings:

- `summary`
- `prior_attempts`
- `relevant_sessions`
- `relevant_files`
- `current_hypothesis`
- `recommended_next_steps`
- `uncertainties`

## Evidence Rules

- Prefer implementation/debugging sessions over planning or strategy sessions.
- Distinguish `session-backed` from `repo-backed` claims.
- Call out stale-advice risk when the repo snapshot may have drifted.
- If retrieved material is meta or evaluative rather than actual prior work, label it as such and do not count it as a prior attempt.
