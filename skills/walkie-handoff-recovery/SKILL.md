---
name: walkie-handoff-recovery
description: Optional companion skill for getting up to speed on prior work in a repo area, especially after a pause or handoff.
---

# Walkie Handoff Recovery

Use this skill when someone needs to recover context quickly rather than rediscover the whole area from scratch.

Do not use this skill for Walkie's public agent/storefront flow. Use it only when prior-work recovery is the actual task.

## Core job

Answer:

- what prior work matters most
- what should be read first
- what not to retry blindly
- where the current repo may have drifted from old advice

## Workflow

1. Search for sessions tied to the feature, bug, or module.
2. Prefer sessions with implementation or debugging content.
3. Summarize only the highest-signal attempts.
4. Cross-check the likely code areas against the attached repo snapshot.
5. End with the best entry point for the next person.

## Output shape

- `summary`
- `relevant_sessions`
- `relevant_files`
- `what_to_read_first`
- `stale_or_risky_advice`
- `recommended_next_steps`

## Guardrails

- Do not dump every related session.
- Avoid generic architecture summaries unless they clearly help the handoff.
- If the corpus is thin, say so directly.

## Walkie integration

- Use the same private repo-backed agent surface as bug recall.
- Keep prompts explicit: ask for handoff recovery, not generic explanation.
- Score success by whether the next reader can act without backreading all prior sessions.
