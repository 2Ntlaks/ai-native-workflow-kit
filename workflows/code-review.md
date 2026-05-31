# Code Review

## Purpose

Review a diff for correctness, risk, and missing tests.

## When to Use

When an agent or human has produced changes.

## When Not to Use

When there is no diff or artifact to inspect.

## Inputs Needed

- Diff
- Task brief
- Relevant tests

## Step-by-Step Process

1. Read the task brief.
2. Inspect changed files.
3. Prioritize bugs, regressions, security, and missing tests.
4. Reference file paths and lines where possible.
5. Separate findings from style suggestions.
6. State residual risk.

## Expected Outputs

- Findings
- Open questions
- Test gaps

## Acceptance Criteria

- Findings are actionable.
- Severity is clear.
- Style preferences are not presented as defects.

## Example Prompt

```text
Review this diff against [brief]. Lead with bugs, regressions, and missing tests.
```

## Common Failure Modes

- Summarizing instead of reviewing.
- Nitpicking while missing behavior risk.
- No file references.

## Review Checklist

- [ ] Are findings severe and specific?
- [ ] Are test gaps noted?
- [ ] Is the review grounded in the diff?

## Sources or Related Notes

See `checklists/implementation-review.md`.
