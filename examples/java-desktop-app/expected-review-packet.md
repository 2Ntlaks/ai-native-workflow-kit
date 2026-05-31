# Expected Review Packet: Java Desktop App

## Summary

- Fixed the Delete action so clicking it with no selected student row no longer crashes.
- Preserved existing delete behavior when a valid row is selected.
- Added selection-state handling in the table UI instead of catching a broad exception.

## Files Changed

- `src/main/java/app/ui/StudentsPanel.java`: disabled the Delete button when no row is selected and re-enabled it when a row is selected.
- `src/test/java/app/ui/StudentsPanelTest.java`: added a regression test for the no-selection delete path, if the project has this test seam.

## Key Decisions

- Decision: guard the UI action at the selection boundary.
- Reason: the bug is caused by the UI allowing an invalid action, not by persistence or domain logic.
- Alternative not chosen: catching `IndexOutOfBoundsException`, because that hides the invalid state and could mask other bugs.

## Tests Run

```bash
./gradlew test
```

Expected result:

```text
BUILD SUCCESSFUL
```

Manual check if UI automation is unavailable:

```text
1. Launch app.
2. Open Students table.
3. Ensure no row is selected.
4. Click Delete or confirm Delete is disabled.
5. Select a row and confirm normal delete confirmation still appears.
```

## Evidence Of Correctness

- Acceptance criterion: Delete with no selection does not throw.
- Evidence: regression test passes or manual no-selection check completed.
- Acceptance criterion: valid delete still works.
- Evidence: existing delete test passes or manual selected-row delete check completed.

## Risks And Uncertainties

- Swing UI automation may not exist in the project; manual evidence may be required.
- If multiple tables share delete behavior, this fix may need the same guard in another panel.

## Follow-Up Work

- Required before merge: human confirms no broad UI redesign was introduced.
- Optional later: add shared helper for selection-aware buttons if the pattern repeats in multiple panels.

## Human Review Focus

- Inspect whether the fix is at the action/selection boundary.
- Confirm no persistence or model behavior changed.
- Re-run `./gradlew test` if local UI dependencies are available.
