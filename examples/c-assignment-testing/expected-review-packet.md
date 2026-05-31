# Expected Review Packet: C Assignment Testing

## Summary

- Added a small C test harness for the linked-list assignment.
- Covered insert, delete, search, empty-list, and single-node edge cases.
- Preserved the student's implementation and public function names.

## Files Changed

- `tests/list_tests.c`: added focused linked-list behavior tests with clear failure messages.
- `build/` or test command docs: documented how to compile the harness if the repo does not already have a test runner.

## Key Decisions

- Decision: use a lightweight C harness instead of adding a full test framework.
- Reason: student assignments should stay easy to compile and inspect.
- Alternative not chosen: rewriting the linked-list implementation, because the tutor needs to evaluate the student's code.

## Tests Run

```bash
gcc -Wall -Wextra -std=c11 src/list.c tests/list_tests.c -o build/list_tests
./build/list_tests
```

## Evidence Of Correctness

- Harness builds with warnings enabled.
- Each tested behavior prints a targeted failure message.
- At least one intentionally bad submission or known edge case fails as expected.

## Risks And Uncertainties

- The harness only tests visible behavior; it does not prove memory safety without tools such as Valgrind or sanitizers.
- If the assignment spec uses different function names, the harness must be adapted.

## Follow-Up Work

- Optional later: add sanitizer or Valgrind instructions for deeper pointer debugging.

## Human Review Focus

- Confirm the tests match the assignment spec.
- Confirm the harness does not reveal a complete solution.
