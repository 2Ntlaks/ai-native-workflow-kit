# Context Packet

## Purpose

Prepare the minimum useful context for an agent task.

## When to Use

Before research, planning, implementation, review, or debugging.

## When Not to Use

When the agent already has a complete current brief and no code changes are needed.

## Inputs Needed

- Objective
- Relevant files
- Current behavior
- Expected behavior
- Commands
- Constraints

## Step-by-Step Process

1. State the outcome.
2. List relevant files and why they matter.
3. Add reproduction steps or examples.
4. List allowed commands.
5. Name non-goals and stop conditions.
6. Trim unrelated context.

## Expected Outputs

- Context packet ready for the agent

## Acceptance Criteria

- A new agent could start without guessing.
- No obvious sensitive data is included.
- Verification path is named.

## Example Prompt

```text
Create a context packet for [task] using these files: [paths].
```

## Common Failure Modes

- Pasting too much.
- Leaving out verification commands.
- Mixing old assumptions with current repo facts.

## Review Checklist

- [ ] Does it include done conditions?
- [ ] Are assumptions labeled?
- [ ] Is the context narrow enough?

## Sources or Related Notes

See `docs/context-engineering.md` and `docs/context-budget.md`.
