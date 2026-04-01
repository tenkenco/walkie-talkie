# Walkie Prompt Pack

Use these prompts during the 2-week validation so results are comparable.

## Strong-Match Prompts

- `What prior work explored this repository to understand its architecture, what files are involved, and what should I inspect first?`
- `What prior work touched GitHub Actions or CI cleanup in Walkie, and what files are likely involved?`
- `What prior work involved auth implementation or auth integration, what files are likely involved, and what should be checked first?`

## Bug-Recall Prompts

- `What did we already try for this bug/problem area, what files are involved, and what should we do next?`
- `What prior work touched billing usage resets and what should be checked first?`
- `Why might agent publish or reindex flows be brittle based on prior sessions?`
- `What have we already tried around OAuth token exchange failures?`

## Handoff Recovery Prompts

- `I am new to this issue. What prior attempts matter most, what files should I read first, and what is the likely next step?`
- `Summarize the implementation history for this area and tell me what not to retry blindly.`

## Stale-Attempt Synthesis Prompts

- `What prior advice here may be stale relative to the attached repo snapshot?`
- `Which previous implementation attempts still look relevant, and which ones may have drifted from current code?`

## Comparison Procedure

For each prompt:

1. Run the private agent.
2. Run plain `walkie sessions search`.
3. Run plain repo/docs search.
4. Compare on:
   - prior-attempt recall
   - file/module grounding
   - clarity of next step
   - uncertainty discipline

## Notes

- Keep at least 2 weak-match prompts in the mix.
- If the agent cites only planning or test material, mark the answer as a miss.
