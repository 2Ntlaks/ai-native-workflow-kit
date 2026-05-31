# Expected Review Packet: Database Schema Change

## Summary

- Added an additive `archived_at` column to lessons.
- Updated default lesson queries to exclude archived lessons.
- Added an explicit query path for archived lesson history.

## Files Changed

- `migrations/XXXX_add_lesson_archived_at.sql`: adds nullable `archived_at` without deleting or rewriting rows.
- `src/data/lessons.*`: filters active lesson lists with `archived_at IS NULL`.
- `tests/lessons.*`: covers active-only and include-archived query behavior.

## Key Decisions

- Decision: use a nullable timestamp instead of a boolean.
- Reason: timestamp preserves when the archive action happened and keeps active rows simple with `NULL`.
- Alternative not chosen: deleting old lessons, because tutoring history may be needed for audit and reporting.

## Tests Run

```bash
npm test
sqlite3 dev.db ".schema lessons"
```

## Evidence Of Correctness

- Existing lessons remain active because `archived_at` defaults to `NULL`.
- Default list tests exclude archived lessons.
- Explicit archive/history tests include archived lessons.

## Risks And Uncertainties

- Production migration execution is out of scope.
- Any report query not covered by tests may still need archive filtering.

## Follow-Up Work

- Required before production: dry-run migration on representative backup data.
- Optional later: add UI affordance for viewing archived lessons.

## Human Review Focus

- Inspect migration safety.
- Inspect every changed query for correct archive semantics.
