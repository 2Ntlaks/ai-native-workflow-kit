# Task Brief: Embedded Systems Task

## Objective

Debounce a pushbutton input for an Arduino lab so one physical press produces one logical event without changing pin assignments.

## Background

Students are learning digital input and state machines. The fix should make the behavior stable while keeping the code understandable for teaching.

## Scope

In scope:

- Preserve existing pin constants.
- Add a simple debounce state using `millis()`.
- Keep serial output useful for manual verification.
- Add a simulation/unit test if the project already supports PlatformIO tests.

Out of scope:

- Changing wiring assumptions.
- Adding interrupts unless the assignment already uses them.
- Changing actuator behavior beyond button event timing.

## Autonomy Level

A2, with hardware-facing changes kept minimal.

## Acceptance Criteria

- [ ] One press triggers one event.
- [ ] Holding the button does not repeatedly trigger unless the assignment explicitly allows repeat.
- [ ] Release and second press are detected.
- [ ] Pin assignments are unchanged.
- [ ] Manual serial-monitor check is documented if automated tests are unavailable.

## Verification

```bash
pio test
```

Fallback manual check: upload sketch, open serial monitor, press/release button ten times, and record observed event count.

## Human Review Focus

Confirm the logic remains teachable and does not introduce timing behavior the hardware setup cannot support.
