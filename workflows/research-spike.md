# Research Spike

## Purpose

Answer a bounded question with sources, caveats, and recommendation.

## When to Use

When the human needs understanding before a plan or implementation.

## When Not to Use

When current repository code or tests already answer the question.

## Inputs Needed

- Research question
- Allowed sources
- Decision this research supports

## Step-by-Step Process

1. Restate the question.
2. Gather current primary sources; if only secondary sources are available, state that limit.
3. Separate facts, interpretations, and assumptions.
4. Record source cards for important claims.
5. Summarize options, caveats, and recommendation.

## Expected Outputs

- Research note
- Source cards
- Recommendation

## Acceptance Criteria

- Sources are recorded.
- Recommendation supports a decision.
- Unverified items are named.

## Example Prompt

```text
Research the current best way to [question]. Use official docs first and record caveats.
```

## Common Failure Modes

- No sources.
- Confusing vendor claims with project requirements.
- Answering more than the decision needs.

## Review Checklist

- [ ] Are claims sourced?
- [ ] Are caveats visible?
- [ ] Can the human make a decision from this?

## Sources or Related Notes

See `research/source-index.md`.
