# Task Brief: Desktop App Local First

## Objective

Add a local backup export for desktop-app data so the user can save a timestamped backup file and later restore it manually.

## Background

The app is local-first. Users need confidence that their data is portable without adding cloud sync or account infrastructure.

## Scope

In scope:

- Add an export command that writes a timestamped backup file.
- Validate that the backup contains the expected local data.
- Add a restore note or manual restore command if restore is not implemented.
- Add tests around backup path creation and serialization if the project supports it.

Out of scope:

- Cloud sync.
- Automatic scheduled backups.
- Encryption claims unless encryption is actually implemented.
- Changing the primary storage engine.

## Autonomy Level

A2 after inspecting storage code.

## Acceptance Criteria

- [ ] Export creates a backup file in the chosen location.
- [ ] Filename includes a safe timestamp.
- [ ] Backup content can be inspected or restored according to documented steps.
- [ ] Errors are shown clearly if the path is unavailable.
- [ ] No cloud or account behavior is introduced.

## Verification

```bash
npm test
```

Manual check: create a backup, inspect file presence and size, then run the documented restore or inspection step.

## Human Review Focus

Check that the feature does not imply stronger backup, privacy, or encryption guarantees than it actually provides.
