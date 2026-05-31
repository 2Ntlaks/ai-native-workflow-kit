# Prompting - Codex

## Title

Prompting - Codex

## Organization or Author

OpenAI

## URL

https://developers.openai.com/codex/prompting

## Date Published If Available

Undated live product documentation

## Date Accessed

2026-05-31

## Source Type

Official product documentation

## Reliability Rating

High

## Key Claims

- Codex works through model calls, file reads, file edits, and tool calls until completion or cancellation.
- Prompts improve when they include reproduction steps, validation steps, linting, and checks.
- Parallel threads should not modify the same files at the same time.

## Caveats

- Goal mode, plan mode, and thread behavior are Codex-specific.

## Workflow Implications

- The kit treats each agent session as a bounded unit of work.
- Parallel exploration is read-only by default or isolated by worktree.
- Verification instructions are included in task briefs and review packets.

## Where the Source Is Used in the Repo

- `docs/human-agent-contract.md`
- `workflows/parallel-exploration.md`
