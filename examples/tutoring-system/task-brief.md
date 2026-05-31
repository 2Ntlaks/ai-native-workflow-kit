# Task Brief: Tutoring System

## Objective

Add a CSV export for tutoring session attendance with date, student name, duration, status, and notes.

## Background

The tutor needs a simple export for admin review and parent/client summaries without exposing more student data than necessary.

## Scope

In scope:

- Add export action for a selected date range.
- Include only attendance fields already stored in the app.
- Escape CSV fields correctly.
- Add tests for commas, quotes, blank notes, and no sessions.

Out of scope:

- Cloud sync.
- Payment data.
- New student profile fields.
- Email sending.

## Autonomy Level

A2 or A3 if tests and UI patterns are clear.

## Acceptance Criteria

- [ ] CSV opens cleanly in a spreadsheet.
- [ ] Empty result exports a header row or clear no-data response.
- [ ] Notes with commas and quotes are escaped correctly.
- [ ] Export does not include private fields outside the scope.
- [ ] Review packet includes privacy review focus.

## Verification

```bash
npm test
```

Manual check: export a sample date range and inspect the CSV in a spreadsheet.

## Human Review Focus

Check privacy scope and whether export fields match real tutoring admin needs.
