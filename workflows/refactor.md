# Refactor

## Purpose

Improve structure while preserving behavior.

## When to Use

When code structure blocks safe future work.

## When Not to Use

When behavior changes are required but not explicitly specified.

## Inputs Needed

- Refactor goal
- Behavior to preserve
- Tests

## Step-by-Step Process

1. Identify current behavior and tests.
2. Define non-goals.
3. Make small mechanical changes.
4. Run tests frequently.
5. Document any behavior risk.
6. Produce review packet.

## Expected Outputs

- Behavior-preserving diff
- Verification evidence

## Acceptance Criteria

- Public behavior is unchanged.
- No opportunistic feature work is included.
- Tests support preservation claim.

## Example Prompt

```text
Refactor [area] to [goal] without changing behavior. Stop if behavior change seems required.
```

## Common Failure Modes

- Smuggling in feature changes.
- Renaming too broadly.
- Replacing working patterns without payoff.

## Review Checklist

- [ ] Can each change be justified?
- [ ] Did tests prove behavior preservation?
- [ ] Is the diff reviewable?

## Sources or Related Notes

See `docs/anti-overengineering.md`.
