# Workflows

Pick one workflow per task. If a task needs more than one, run them in sequence with a review gate between them.

| Task shape | Start with |
|---|---|
| Unsure what to ask the agent to do | `choose-a-workflow.md` |
| Agent lacks enough repo context | `context-packet.md` |
| Need a source-backed answer | `research-spike.md` |
| Requirement is rough or risky | `spec-to-plan.md` |
| Build a bounded feature | `feature-implementation.md` |
| Fix wrong behavior | `bug-fix.md` |
| Preserve behavior while cleaning structure | `refactor.md` |
| Add or improve tests | `test-generation.md` |
| Inspect a diff | `code-review.md` |
| Update docs after behavior changed | `documentation-update.md` |
| Compare options without editing | `parallel-exploration.md` |
| Improve a repeated workflow | `evaluator-optimizer.md` |
| Use several agents cautiously | `multi-agent-cautious-use.md` |
| Learn from a finished task | `after-action-retrospective.md` |

Default path: `context-packet.md` -> `spec-to-plan.md` -> implementation workflow -> `code-review.md` -> `after-action-retrospective.md`.

Multi-agent workflows are not the default.
