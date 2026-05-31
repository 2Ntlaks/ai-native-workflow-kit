# Documentation Update

## Purpose

Update docs to match current behavior or decisions.

## When to Use

When code, workflow, or policy changed.

## When Not to Use

When docs would describe future ideas as facts.

## Inputs Needed

- Current behavior
- Changed files
- Audience

## Step-by-Step Process

1. Inspect the source of truth.
2. Update only affected docs.
3. Link related docs.
4. Remove stale claims.
5. Record source updates if needed.
6. Review for bloat.

## Expected Outputs

- Updated docs
- Changed links
- Source notes if needed

## Acceptance Criteria

- Docs match current behavior.
- No duplicated manual sections.
- Reader can act on the doc.

## Example Prompt

```text
Update docs for [change]. Keep it practical and link related workflow files.
```

## Common Failure Modes

- Writing aspirational docs.
- Duplicating content everywhere.
- Forgetting source cards.

## Review Checklist

- [ ] Do docs help a decision?
- [ ] Are claims sourced?
- [ ] Is old guidance removed?

## Sources or Related Notes

See `docs/maintenance.md`.
