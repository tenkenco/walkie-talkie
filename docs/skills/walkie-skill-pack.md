# Walkie Skill Pack

This package turns the current product wedge into four reusable skills:

- `walkie-bug-recall`
- `walkie-handoff-recovery`
- `walkie-stale-attempt-synthesis`
- `walkie-next-step-brief`

These are not four separate products. They are four views over the same private engineering-memory loop.

## Why this split

- `walkie-bug-recall` is the lead wedge and primary evaluation surface.
- `walkie-handoff-recovery` reframes the same retrieval for fast context recovery.
- `walkie-stale-attempt-synthesis` emphasizes repo drift and stale advice.
- `walkie-next-step-brief` compresses the output into the shortest actionable form.

## Best integration with current Walkie infrastructure

Use existing infrastructure rather than building a new skills subsystem first.

### 1. Keep skills as prompt profiles first

Map each skill to a prompt profile layered on top of the same private repo-backed Walkie agent:

- shared primitives:
  - synced/imported sessions
  - repo bootstrap snapshot
  - reindex
  - preview / private invoke
- varying layer:
  - instructions
  - answer shape
  - prompt template

This is the lowest-friction way to test value quickly.

### 2. Use one shared base agent plus skill-specific prompts

The best current fit is:

- one private base memory agent
- one repo-backed deployment
- skill-specific prompt variants for the four use cases

Do not split into four independent agents unless behavior diverges enough that shared retrieval quality becomes a problem.

### 3. Add script tools only if a deterministic gap appears

Current built-ins are already enough for the wedge:

- `searchWalkieSessions`
- repo bootstrap via `walkie agent deploy --repo-path`
- `walkie agent reindex`
- `walkie agent preview --debug`

Only introduce custom script tools if you need deterministic behavior such as:

- filtering known bad session IDs
- labeling snapshot freshness
- producing a fixed evaluation table

### 4. Keep Hub and publish out of the critical path

These skills are for private use first. Treat publish/hub as optional later distribution, not as the implementation surface for the wedge.

## Recommended rollout order

1. `walkie-bug-recall`
2. `walkie-stale-attempt-synthesis`
3. `walkie-next-step-brief`
4. `walkie-handoff-recovery`

## Evaluation guidance

- Use the same validation prompts and rubric under `/Users/rickyyoung/GitHub/wk-2/docs/validation`.
- Score whether the skill changes the next debugging step.
- Treat any answer that cites planning/test material as real prior work as a failure.
