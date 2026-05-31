# Test Generation

## Purpose

Add useful tests for existing behavior or a change.

## When to Use

When behavior is clear but test coverage is weak.

## When Not to Use

When expected behavior is not agreed.

## Inputs Needed

- Behavior spec
- Test framework
- Relevant files

## Step-by-Step Process

1. Inspect existing test style.
2. List behaviors and edge cases.
3. Add focused tests.
4. Run targeted tests.
5. Avoid brittle implementation-only assertions.
6. Report coverage gaps.

## Expected Outputs

- Tests
- Command output
- Coverage gaps

## Acceptance Criteria

- Tests match local style.
- Tests fail for real regressions.
- Known gaps are stated.

## Example Prompt

```text
Add tests for [behavior]. Follow existing test patterns and run the targeted suite.
```

## Common Failure Modes

- Testing implementation details.
- Adding tests that never fail.
- Ignoring existing fixtures.

## Review Checklist

- [ ] Are tests readable?
- [ ] Do they cover edge cases?
- [ ] Do they prove the right behavior?

## Sources or Related Notes

See `checklists/test-review.md`.
