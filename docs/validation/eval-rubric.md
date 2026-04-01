# Walkie Eval Rubric

Use one row per prompt/answer pair.

## Ratings

- `useful`
- `partially useful`
- `not useful`

## Required Checks

### Evidence quality

- Did it cite a real implementation/debugging session?
- Did it avoid treating planning or evaluation chatter as prior work?
- Did it distinguish session-backed and repo-backed claims?

### Relevance

- Did it identify the right file or module area?
- Did it capture what was actually tried before?
- Did it identify what remained unresolved?

### Decision support

- Did it give a next step an engineer would actually take?
- Did it separate fact from hypothesis?
- Did it return `insufficient evidence` when evidence was weak?

## Suggested Table

| Prompt | Agent rating | Plain search rating | Won? | Why |
| --- | --- | --- | --- | --- |
| prompt text | useful / partially useful / not useful | useful / partially useful / not useful | yes / no | short note |

## Common Failure Modes

- Cites product planning as bug history
- Overconfident file guesses
- Generic next-step advice with no historical value
- No stale-advice warning despite repo drift risk
- Correct retrieval but poor synthesis
