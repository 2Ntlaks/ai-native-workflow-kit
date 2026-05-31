# Feature Implementation

## Purpose

Build a scoped feature with verification and a review packet.

## When to Use

When acceptance criteria are clear and scope is bounded.

## When Not to Use

When product behavior is still undecided.

## Inputs Needed

- Approved brief
- Acceptance criteria
- Verification commands

## Step-by-Step Process

1. Inspect existing patterns.
2. Implement the smallest useful change.
3. Add or update tests where risk justifies it.
4. Run verification.
5. Update docs if behavior changed.
6. Produce review packet.

## Expected Outputs

- Working feature
- Tests or evidence
- Review packet

## Acceptance Criteria

- Acceptance criteria are met.
- No unrelated refactor is included.
- Review packet is complete.

## Example Prompt

```text
Implement [feature] within [scope]. Run [commands] and end with the review packet format.
```

## Common Failure Modes

- Expanding scope.
- Skipping docs for changed behavior.
- Adding dependencies without approval.

## Review Checklist

- [ ] Does diff match feature?
- [ ] Did verification cover acceptance criteria?
- [ ] Are risks stated?

## Sources or Related Notes

See `templates/review-packet.md`.
