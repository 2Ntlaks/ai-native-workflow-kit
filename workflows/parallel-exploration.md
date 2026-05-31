# Parallel Exploration

## Purpose

Compare options without letting agents edit the same files.

## When to Use

When multiple approaches are plausible and cheap to investigate.

## When Not to Use

When the task is already clear enough to implement.

## Inputs Needed

- Question
- Options
- Boundaries

## Step-by-Step Process

1. Define independent exploration questions.
2. Keep work read-only or use isolated worktrees.
3. Ask each agent for evidence and recommendation.
4. Compare findings in one synthesis.
5. Choose one path before coding.

## Expected Outputs

- Comparison matrix
- Recommendation

## Acceptance Criteria

- No conflicting edits.
- Human chooses before implementation.
- Evidence is comparable.

## Example Prompt

```text
Explore these options in parallel: [options]. Do not edit shared files. Return evidence and recommendation.
```

## Common Failure Modes

- Parallel agents editing same files.
- Merging conflicting plans without review.
- Using parallel work to avoid a decision.

## Review Checklist

- [ ] Are options comparable?
- [ ] Did each result cite evidence?
- [ ] Was one path chosen before coding?

## Sources or Related Notes

See `research/source-cards/openai-codex-prompting.md`.
