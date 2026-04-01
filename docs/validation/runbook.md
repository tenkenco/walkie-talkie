# Walkie Validation Runbook

## Fresh Evaluation Cycle

1. Sync/import the latest relevant sessions.
2. Deploy or redeploy the private memory agent with a fresh repo snapshot.
3. Run `walkie agent reindex <agent-id>`.
4. Confirm reindex completion with `walkie agent status <agent-id>`.
5. Run prompts from [prompt-pack.md](/Users/rickyyoung/GitHub/wk-2/docs/validation/prompt-pack.md).
6. Score answers with [eval-rubric.md](/Users/rickyyoung/GitHub/wk-2/docs/validation/eval-rubric.md).

## Operator Checklist

- Confirm the repo snapshot source and commit.
- Note the reindex completion time.
- Record whether each answer was mostly `session-backed`, `repo-backed`, or mixed.
- Flag any answer that cites planning/test sessions as real prior work.

## Decision Rule

Keep investing in the wedge if:

- engineers return to it repeatedly for real issues
- it wins against plain search on several real prompts
- failures are mostly fixable via curation/ranking, not a missing use case

Pause or rethink if:

- answers are mostly generic even when evidence exists
- trusted users do not come back after the initial trial
- repo grounding adds little value over plain session search
