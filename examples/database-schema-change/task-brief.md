# Task Brief: Database Schema Change

## Objective

Add a nullable `archived_at` column to lessons and update lesson queries so archived lessons are hidden by default but still retrievable for audit/history screens.

## Background

Tutoring data should not be deleted when a lesson is no longer active. Archiving keeps history while reducing clutter in normal views.

## Scope

In scope:

- Add an additive migration for `archived_at`.
- Update read queries to exclude archived rows by default.
- Add an explicit query path for archived lessons.
- Add tests for active-only and include-archived behavior.

Out of scope:

- Deleting existing lesson rows.
- Backfilling archive dates.
- Changing payment or attendance logic.
- Production migration execution.

## Autonomy Level

A1 for migration plan, then A2 after approval.

## Acceptance Criteria

- [ ] Migration is additive and non-destructive.
- [ ] Existing lessons remain active with `archived_at = NULL`.
- [ ] Default lesson list excludes archived rows.
- [ ] Explicit archived query includes archived rows.
- [ ] Tests or dry-run evidence are included.

## Verification

```bash
npm test
sqlite3 dev.db ".schema lessons"
```

## Human Review Focus

Inspect migration safety and every query that should or should not include archived lessons.
