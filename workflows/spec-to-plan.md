# Spec To Plan

## Purpose

Turn a rough requirement into a reviewable implementation plan.

## When to Use

When scope is not yet safe to code.

## When Not to Use

When the task is a one-line obvious fix.

## Inputs Needed

- Feature or bug spec
- Repo context
- Acceptance criteria

## Step-by-Step Process

1. Inspect relevant files.
2. Ask clarifying questions only if needed.
3. Define in-scope and out-of-scope work.
4. List files likely to change.
5. Propose verification commands.
6. Wait for approval.

## Expected Outputs

- Implementation plan
- Risks
- Verification plan

## Acceptance Criteria

- Plan is reviewable before edits.
- No broad refactor is hidden in the plan.
- Verification is realistic.

## Example Prompt

```text
Read the relevant code and propose a plan for [task]. Do not edit files yet.
```

## Common Failure Modes

- Planning without inspecting code.
- Plan omits tests.
- Scope grows quietly.

## Review Checklist

- [ ] Does the plan match the repo?
- [ ] Are decisions explicit?
- [ ] Does the plan preserve boundaries?

## Sources or Related Notes

See `checklists/plan-review.md`.
