# Retrospective: Java Desktop App

## What Worked

- A2 was the right autonomy level: the bug was bounded and easy to verify.
- The task brief prevented a UI redesign by naming the exact behavior and non-goals.
- The review packet made the human check the risky part first: no-selection behavior plus preservation of valid delete.

## What Failed Or Slowed Review

- If the project lacks UI tests, the agent must provide a precise manual check instead of saying "tested manually."
- The agent plan needs to name likely files or UI layers so the human can spot unrelated edits quickly.

## Lesson Learned

For desktop UI bugs, the brief should name both the invalid action and the valid action that must keep working.

## Kit Update Needed

No immediate template change. Revisit if multiple desktop examples need a shared UI-manual-check pattern.
