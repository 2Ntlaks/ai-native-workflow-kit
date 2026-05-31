# Task Brief: C Assignment Testing

## Objective

Create a small C test harness for a student's linked-list assignment that checks insert, delete, search, empty-list, and single-node edge cases without rewriting the student's solution.

## Background

The tutor needs fast feedback on student submissions. The goal is to catch common pointer mistakes while preserving the student's code for review.

## Scope

In scope:

- Add tests under `tests/`.
- Compile the submitted `list.c` and `list.h` with warnings enabled.
- Include cases for head deletion, tail deletion, missing value, duplicate insert, and empty list.

Out of scope:

- Rewriting student implementation.
- Changing public function names.
- Adding a full unit test framework unless already present.

## Autonomy Level

A2 after the agent inspects the existing assignment structure.

## Acceptance Criteria

- [ ] Harness builds with the existing submission files.
- [ ] At least five linked-list behaviors are tested.
- [ ] A failing student implementation produces a clear failure message.
- [ ] No unrelated formatting or solution rewrites are included.

## Verification

```bash
gcc -Wall -Wextra -std=c11 src/list.c tests/list_tests.c -o build/list_tests
./build/list_tests
```

## Human Review Focus

Confirm the tests match the assignment spec and do not give away a complete solution.
