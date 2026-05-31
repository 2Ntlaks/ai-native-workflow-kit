# Multi-Agent Cautious Use

## Purpose

Use multiple agents only for bounded independent work.

## When to Use

When separate research, test, or review tracks can run independently.

## When Not to Use

When one agent can do the work clearly.

## Inputs Needed

- Independent subproblems
- File boundaries
- Synthesis owner

## Step-by-Step Process

1. Define roles and boundaries.
2. Prevent overlapping edits.
3. Run agents in isolated threads or worktrees.
4. Require each agent to produce evidence.
5. Have one owner synthesize.
6. Review final work normally.

## Expected Outputs

- Role briefs
- Evidence from each agent
- Synthesis

## Acceptance Criteria

- No shared-file collisions.
- Synthesis resolves conflicts.
- Coordination cost is justified.

## Example Prompt

```text
Use separate agents only to investigate [A], [B], and [C]. No shared edits. Synthesize before implementation.
```

## Common Failure Modes

- Coordination overhead.
- Conflicting changes.
- Assuming more agents means better quality.

## Review Checklist

- [ ] Was multi-agent necessary?
- [ ] Are boundaries explicit?
- [ ] Did synthesis choose a single path?

## Sources or Related Notes

See `research/source-cards/anthropic-building-effective-agents.md`.
