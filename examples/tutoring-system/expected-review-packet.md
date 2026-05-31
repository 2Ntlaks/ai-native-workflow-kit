# Expected Review Packet: Tutoring System

## Summary

- Added CSV export for tutoring session attendance.
- Included date, student name, duration, status, and notes.
- Escaped commas, quotes, blank notes, and empty result cases.

## Files Changed

- `src/export/attendance-csv.*`: builds CSV rows and escapes fields.
- `src/ui/attendance-export.*`: adds date-range export action.
- `tests/attendance-csv.*`: covers special characters and no-session export behavior.

## Key Decisions

- Decision: export only existing attendance fields.
- Reason: reduces privacy risk and keeps the feature aligned with admin reporting needs.
- Alternative not chosen: adding payment or profile fields, because they are out of scope and more sensitive.

## Tests Run

```bash
npm test
```

Manual check:

```text
Export a sample date range and open the CSV in a spreadsheet.
```

## Evidence Of Correctness

- CSV opens cleanly in a spreadsheet.
- Notes with commas and quotes are escaped.
- Empty range returns a header row or clear no-data response.

## Risks And Uncertainties

- Spreadsheet apps may interpret some values unexpectedly if formula injection is not handled.
- Export privacy depends on the selected fields staying limited.

## Follow-Up Work

- Required before sharing externally: confirm no sensitive fields are included.
- Optional later: add export presets for parent summaries.

## Human Review Focus

- Check privacy scope first.
- Inspect escaping tests for quotes, commas, and blank values.
