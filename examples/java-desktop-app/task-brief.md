# Task Brief: Java Desktop App

## Objective

Fix a Swing desktop app crash when the user clicks Delete with no row selected in the students table.

## Background

The app is used during tutoring admin work. A small UI mistake should not crash the session or risk losing unsaved edits.

## Scope

In scope:

- Inspect the table selection handler and delete action.
- Disable Delete when no row is selected or show a clear non-blocking message.
- Preserve existing delete behavior when a valid row is selected.
- Add a focused test if the project has UI/controller tests.

Out of scope:

- Redesigning the table UI.
- Changing persistence format.
- Introducing a new UI framework.

## Autonomy Level

A2 after a short plan.

## Acceptance Criteria

- [ ] Clicking Delete with no selection no longer throws.
- [ ] Valid delete behavior still works.
- [ ] The user gets clear feedback or the action is disabled.
- [ ] Verification evidence includes a test result or manual UI check.

## Verification

```bash
./gradlew test
```

Manual check: launch the app, open the students table, clear selection, click Delete, and confirm no crash.

## Human Review Focus

Inspect whether the fix belongs in the action/controller layer rather than hiding the exception globally.
