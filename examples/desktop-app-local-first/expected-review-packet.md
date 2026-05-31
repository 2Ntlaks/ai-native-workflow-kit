# Expected Review Packet: Desktop App Local First

## Summary

- Added a local backup export command for app data.
- Backup files use a safe timestamped filename.
- Documented restore or inspection steps without claiming cloud sync or encryption.

## Files Changed

- `src/storage/backup.*`: serializes current local data to a user-chosen backup file.
- `src/ui/backup-action.*`: exposes export action and error feedback.
- `docs/backup.md`: explains backup location, inspection, and manual restore.
- `tests/backup.*`: covers filename creation and serialization where test seams exist.

## Key Decisions

- Decision: implement manual export only.
- Reason: local-first backup should stay understandable before adding scheduling or sync.
- Alternative not chosen: cloud backup, because that introduces accounts, privacy, and network failure modes.

## Tests Run

```bash
npm test
```

Manual check:

```text
Create a backup, inspect file presence and size, then follow the documented restore or inspection step.
```

## Evidence Of Correctness

- Export creates a file at the chosen location.
- Filename includes a safe timestamp.
- Missing or unwritable paths produce a visible error.

## Risks And Uncertainties

- Backup is not encrypted unless the app already encrypts the underlying data.
- Manual restore may be error-prone if not implemented as a first-class command.

## Follow-Up Work

- Optional later: add restore automation after manual export proves useful.

## Human Review Focus

- Check that the UI does not overpromise privacy, encryption, or cloud durability.
