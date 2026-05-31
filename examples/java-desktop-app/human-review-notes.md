# Human Review Notes: Java Desktop App

## Diff Review

- [ ] Delete action is guarded or disabled when no row is selected.
- [ ] Valid selected-row delete behavior still follows the old flow.
- [ ] No persistence, schema, or student model changes were introduced.
- [ ] No broad Swing redesign or unrelated formatting churn.

## Evidence Review

- [ ] `./gradlew test` passed, or the failure is unrelated and clearly explained.
- [ ] Manual no-selection check is recorded if no UI test exists.
- [ ] Review packet states what to inspect first.

## Decision

Accepted.

## Reason

The fix is scoped to the UI/action boundary, preserves existing valid delete behavior, and provides enough test or manual evidence for this risk level.

## Follow-Up

If two more table actions have similar no-selection bugs, add a small shared selection-action helper and document the UI convention.
