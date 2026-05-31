# Choose A Workflow

## Purpose

Select the smallest workflow that fits the task risk.

## When to Use

At the start of any agent task when the task type is not already obvious.

## When Not to Use

When an approved brief already names the workflow and autonomy level.

## Inputs Needed

- Task objective
- Known risk areas
- Whether code changes are expected
- Available verification

## Step-by-Step Process

1. Classify the task as research, planning, implementation, review, documentation, eval, or retrospective.
2. Check for sensitive areas such as auth, data, migrations, hardware, deployment, and dependencies.
3. Choose the smallest matching workflow.
4. Choose autonomy level.
5. Record the choice in the task brief.

## Expected Outputs

- Selected workflow
- Autonomy recommendation
- Review checklist recommendation

## Acceptance Criteria

- Workflow matches the task type.
- Risky tasks are not pushed directly to implementation.
- The human can explain why the workflow was chosen.

## Example Prompt

```text
Choose a workflow for this task: [objective]. Recommend autonomy level and review checklist.
```

## Common Failure Modes

- Picking feature implementation for a research question.
- Using multi-agent work as the default.
- Ignoring permission risk.

## Review Checklist

- [ ] Is the workflow small enough?
- [ ] Are stop conditions clear?
- [ ] Does the workflow match the task type?

## Sources or Related Notes

See `docs/autonomy-levels.md` and `docs/anti-overengineering.md`.
