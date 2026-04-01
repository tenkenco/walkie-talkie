---
name: walkie-bug-recall
description: Optional companion skill for answering bug-history questions with Walkie's prior-work recall: what was already tried, what files are involved, what still looks unresolved, and what should be done next.
---

# Walkie Bug Recall

Use this skill when the user wants a concise implementation brief for a bug or brittle area.

Walkie's primary workflow is still agent creation, deployment, and storefront publishing. Use this only when prior-work recall is the actual need.

## Core job

Answer:

- what we already tried
- what seems unresolved
- what files or modules matter
- what the next debugging step should be

## Workflow

1. Search Walkie sessions first.
2. Prefer implementation/debugging sessions over planning or strategy sessions.
3. Cross-check likely files against the attached repo snapshot if one exists.
4. Separate factual prior attempts from current hypothesis.
5. If evidence is weak or only meta/planning material matches, say `insufficient evidence`.

## Output contract

Return these headings in order:

- `summary`
- `prior_attempts`
- `relevant_sessions`
- `relevant_files`
- `current_hypothesis`
- `recommended_next_steps`
- `uncertainties`

## Evidence rules

- Do not present planning, evaluation, or prompt-writing sessions as actual bug history.
- Prefer sessions with logs, commands, diffs, code review, failure analysis, or concrete file references.
- Distinguish `session-backed` from `repo-backed` claims.
- Call out stale-advice risk when repo freshness is uncertain.

## Walkie integration

- Use `searchWalkieSessions` for recall.
- Use repo bootstrap context from `walkie agent deploy --repo-path ...` for file grounding.
- Run `walkie agent reindex <id>` before serious evaluation cycles.
- Use `walkie agent preview --debug` to inspect citations and bad matches.
