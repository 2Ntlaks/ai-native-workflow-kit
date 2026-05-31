# Bug Fix

## Purpose

Reproduce, diagnose, fix minimally, and prevent regression.

## When to Use

When current behavior is wrong, failing, or inconsistent with requirements.

## When Not to Use

When the issue is a feature request disguised as a bug.

## Inputs Needed

- Bug report
- Reproduction steps
- Expected behavior
- Actual behavior
- Relevant logs

## Step-by-Step Process

1. Reproduce the bug or explain why reproduction is unavailable.
2. Identify root cause.
3. Make the minimal fix.
4. Add a regression test unless the project has no test harness; if no test is possible, document the manual check.
5. Run verification.
6. Produce review packet.

## Expected Outputs

- Fix
- Root cause note
- Regression evidence

## Acceptance Criteria

- Bug no longer reproduces.
- Existing behavior is preserved.
- Root cause is explained.

## Example Prompt

```text
Fix this bug: [report]. Reproduce it first, identify root cause, make the minimal fix, and add a regression test. If no automated test is possible, document the manual check.
```

## Common Failure Modes

- Treating symptoms.
- Suppressing errors.
- No reproduction.
- Changing behavior outside the bug.

## Review Checklist

- [ ] Is root cause explained?
- [ ] Is the fix minimal?
- [ ] Is there regression evidence?

## Sources or Related Notes

Inspired by issue-to-patch evaluation patterns from SWE-bench.
