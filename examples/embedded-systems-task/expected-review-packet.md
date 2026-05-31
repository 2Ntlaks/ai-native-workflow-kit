# Expected Review Packet: Embedded Systems Task

## Summary

- Added debounce logic for a pushbutton input using `millis()`.
- Preserved existing pin assignments and teaching-oriented structure.
- Documented serial-monitor verification for hardware behavior.

## Files Changed

- `src/main.cpp` or sketch file: added debounce state and press/release handling.
- `test/` files: added simulation test if the project already supports PlatformIO tests.
- `README.md` or lab notes: documented manual serial-monitor check if no automated test exists.

## Key Decisions

- Decision: use a simple polling debounce instead of interrupts.
- Reason: the lab is teaching digital input and state machines, and polling is easier to inspect.
- Alternative not chosen: changing wiring or pin constants, because that would invalidate the lab setup.

## Tests Run

```bash
pio test
```

Fallback manual check:

```text
Upload sketch, open serial monitor, press/release the button ten times, and record observed event count.
```

## Evidence Of Correctness

- One physical press produces one logical event.
- Holding the button does not repeatedly trigger unless repeat is part of the assignment.
- Release and second press are detected.

## Risks And Uncertainties

- Hardware bounce varies by button and wiring.
- Serial-monitor verification is weaker than a deterministic simulation test.

## Follow-Up Work

- Optional later: add a simulation seam for time-based button state transitions.

## Human Review Focus

- Confirm pin assignments are unchanged.
- Confirm debounce timing remains understandable for students.
