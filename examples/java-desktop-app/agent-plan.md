# Agent Plan: Java Desktop App

## Task

Fix a Swing desktop app crash when the user clicks Delete with no row selected in the students table.

## Plan

1. Inspect the delete action handler, table selection model, and any controller method called by the Delete button.
2. Reproduce the likely failure path: no selected row produces `-1`, then code indexes the table model or student list with that value.
3. Make the smallest fix in the UI/controller layer:
   - disable Delete when no row is selected, or
   - guard the action and show a short non-blocking message.
4. Preserve existing behavior when a valid row is selected.
5. Add or update a focused controller/action test if the project already has UI-adjacent tests.
6. Run `./gradlew test`.
7. Manually verify the no-selection path if UI automation is not available.
8. Prepare the review packet with the exact file(s), evidence, and review focus.

## Expected Files

- `src/main/java/.../StudentsPanel.java` or equivalent table view: selection and button state.
- `src/main/java/.../StudentController.java` or equivalent action handler: delete guard if controller owns the action.
- `src/test/java/...`: focused regression test if the project has a test seam.

## Stop Conditions

- The fix requires changing persistence or the student data model.
- The UI has no clear owner for delete behavior.
- Tests cannot run and no manual UI check can be performed.
