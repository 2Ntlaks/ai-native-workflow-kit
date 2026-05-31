# Evaluator Optimizer

## Purpose

Improve a workflow by scoring outputs and tightening prompts or templates.

## When to Use

When a repeated task has measurable quality issues.

## When Not to Use

When there is no stable task or scoring rubric yet.

## Inputs Needed

- Task examples
- Rubric
- Desired improvement

## Step-by-Step Process

1. Select a small golden task.
2. Run the current workflow.
3. Score using the rubric.
4. Identify the smallest template or checklist change.
5. Run again only if useful.
6. Record lesson learned.

## Expected Outputs

- Scorecard
- Template improvement
- Lesson

## Acceptance Criteria

- Score changes inform a real decision.
- Only one main variable changes.
- Template improvement is concrete.

## Example Prompt

```text
Evaluate this workflow on [golden task]. Score it and propose one template improvement.
```

## Common Failure Modes

- Optimizing for vanity metrics.
- Changing too many variables.
- Treating benchmark results as project readiness.

## Review Checklist

- [ ] Does the scorecard map to real review pain?
- [ ] Was only one thing changed?
- [ ] Is the lesson reusable?

## Sources or Related Notes

See `evals/workflow-scorecard.md`.
