# Context Engineering

Context engineering is giving the agent enough relevant information to act well without burying the important parts.

## Context Packet Contents

- Objective
- Background
- Current behavior
- Expected behavior
- Relevant files, logs, screenshots, docs, or issue links
- Constraints and non-goals
- Autonomy level
- Verification commands
- Acceptance criteria
- Stop conditions

## Progressive Disclosure

Start with the smallest useful context. Let the agent inspect files, then add more only when it asks for a specific reason.
