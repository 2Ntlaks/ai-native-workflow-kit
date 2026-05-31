# AI-Native Workflow Kit

A practical Markdown operating manual for giving AI coding agents enough context and room to do strong work while keeping the human responsible for product judgment, permissions, review, and final acceptance.

This kit is for builders working across C, Java, WebGL, databases, embedded systems, desktop apps, tutoring systems, portfolio projects, and other real codebases.

The goal is simple:

> Stop being the bottleneck by giving the agent room to work without giving up judgment.

## Why I Built This

I built this because I noticed I was the bottleneck in my own projects. The models behind coding agents are genuinely powerful: they often know more than I do, and when they do not, they can research, compare options, and come back with a better result than I would produce manually. The answer was not to hand over the keys; it was to give the agent enough context and clear boundaries, let it explore ways to solve the problem, and keep myself responsible for judgment, review, and the final decision.

## What This Is

This repo helps you give coding agents better work, let them use their capability, and review the output faster. It provides:

- task briefs that give the agent context, scope, acceptance criteria, verification, and stop conditions
- autonomy levels so the agent knows how much room it has to research, plan, edit, or stop
- workflows for bug fixes, features, refactors, tests, research spikes, and code review
- checklists for inspecting diffs, tests, security risks, docs, and merge readiness
- review packet templates so every agent task ends with evidence, risks, and review focus
- source tracking so important claims are not treated as magic advice

This is not a prompt dump, productivity hack list, or software app.

## Context Is The Leverage

The quality of agent output is mostly a function of context quality plus clear boundaries. If the agent gets the right files, constraints, examples, acceptance criteria, and permission limits, it can explore solution paths instead of guessing what you meant. The value is not just asking better prompts; it is giving the model enough situational awareness to use its capability while you keep the final judgment.

## Try This In 10 Minutes

For your next real task, use only these three files first:

1. [templates/agent-task-brief.md](templates/agent-task-brief.md)
2. [docs/autonomy-levels.md](docs/autonomy-levels.md)
3. [templates/review-packet.md](templates/review-packet.md)

Minimum safe path for a small bug:

```text
brief -> A2 bounded fix -> tests/manual check -> review packet -> human diff review
```

## 60-Second Example

Bad request:

```text
Fix my app.
```

Better agent task:

```text
Use autonomy level A2 and the bug-fix workflow.

Bug: the Java desktop app crashes when Delete is clicked with no table row selected.

Scope:
- inspect the table selection and delete action
- make the smallest fix
- preserve valid delete behavior
- do not redesign the UI

Verification:
- run ./gradlew test
- manually check that Delete with no selection does not crash

Final response:
End with the review packet format, including files changed, tests run,
evidence, risks, and human review focus.
```

Human review:

```text
Use checklists/implementation-review.md and checklists/test-review.md.
Accept only if the diff matches the task and the evidence covers the crash.
```

## Start Here

For day-to-day use, open [START_HERE.md](START_HERE.md).

Default path for most tasks:

1. Fill [templates/agent-task-brief.md](templates/agent-task-brief.md).
2. Choose an autonomy level from [docs/autonomy-levels.md](docs/autonomy-levels.md).
3. Pick a workflow from [workflows/README.md](workflows/README.md).
4. Give the brief and context packet to the agent, then let it explore within the boundary.
5. Review the result with the relevant checklist.
6. Save the review packet and record repeated failures.

## The Core Loop

```text
Define task -> choose workflow -> choose autonomy -> prepare context
-> agent explores/researches/plans/implements -> agent verifies -> human reviews
-> record lessons
```

The agent should do more of the work. The human still owns the decision.

## Who This Is For

- Solo builders using coding agents on real projects.
- Builders who suspect they are the bottleneck and want to delegate more without losing understanding.
- Students who want agent help without losing understanding or review control.
- Tutors and project builders working across assignments, tools, visualizers, databases, and desktop apps.
- Developers who want repeatable review packets instead of vague agent summaries.

## Who This Is Not For

- People looking for a list of clever prompts.
- Teams that already have mature internal agent governance.
- Workflows where agents may change production systems without human review.
- Anyone trying to avoid understanding the code they submit or ship.

## Autonomy Levels

| Level | Use When | Human Gate |
|---|---|---|
| A0 | Research only, no edits | Review sources and decide next step |
| A1 | Plan first | Approve plan before edits |
| A2 | Bounded implementation | Review diff, tests, and review packet |
| A3 | Implement, test, document | Review full packet and risky decisions |
| A4 | Small subsystem ownership | Strict boundaries and scheduled review |
| A5 | Broad autonomous development | Avoid for now unless rules are mature |

See [docs/autonomy-levels.md](docs/autonomy-levels.md) for examples across C, Java, WebGL, databases, embedded systems, and tutoring systems.

## What To Use First

| Need | File |
|---|---|
| Give an agent a task | [templates/agent-task-brief.md](templates/agent-task-brief.md) |
| Pick the right workflow | [workflows/README.md](workflows/README.md) |
| Decide how much freedom to give | [docs/autonomy-levels.md](docs/autonomy-levels.md) |
| Prepare repo context | [workflows/context-packet.md](workflows/context-packet.md) |
| Review a diff | [checklists/implementation-review.md](checklists/implementation-review.md) |
| Check test evidence | [checklists/test-review.md](checklists/test-review.md) |
| Handle security-sensitive work | [checklists/security-review.md](checklists/security-review.md) |
| Capture lessons after a task | [templates/after-action-report.md](templates/after-action-report.md) |

## Worked Examples

Start with these if you want to see the kit grounded in real tasks:

- [Java desktop crash fix](examples/java-desktop-app/) - complete mini case study with task brief, agent plan, review packet, human review notes, and retrospective.
- [C assignment testing](examples/c-assignment-testing/) - testing student linked-list submissions without rewriting the solution.
- [Embedded systems debounce task](examples/embedded-systems-task/) - bounded Arduino change with manual hardware verification.
- [Local-first desktop backup](examples/desktop-app-local-first/) - backup export without overclaiming cloud sync or encryption.

## Use It In Another Project

Do not copy this whole repo into every project. Keep this repo as the source of truth, then add a short `AGENTS.md` to each project:

```md
# AGENTS.md

Use the AI-Native Workflow Kit:
https://github.com/2Ntlaks/ai-native-workflow-kit

Default autonomy:
- A1 for unclear or risky work.
- A2 for bounded implementation.

For implementation tasks:
1. Read the task brief.
2. Follow the selected workflow.
3. Run verification.
4. End with a review packet.

Stop before dependencies, migrations, auth/security changes, destructive actions,
private data, deployment settings, or broad refactors unless explicitly approved.
```

## Repository Map

| Path | Purpose |
|---|---|
| [docs/](docs/) | Operating model, autonomy, context, permissions, maintenance |
| [workflows/](workflows/) | Step-by-step processes for common agent tasks |
| [templates/](templates/) | Copy-paste briefs, plans, review packets, decisions, and failure reports |
| [checklists/](checklists/) | Fast human review gates |
| [examples/](examples/) | Realistic task examples from the owner's domains |
| [adapters/](adapters/) | Short templates for Codex, Claude Code, GitHub Copilot, and Cursor |
| [research/](research/) | Source cards, [claims index](research/claims-index.md), verification status, and caveats |
| [evals/](evals/) | Local golden tasks and workflow scorecards |
| [decisions/](decisions/) | Decision journal |
| [failures/](failures/) | Repeated agent mistakes and prevention notes |

## Contribution Standard

Contributions should make agent work easier to delegate or review. Prefer practical workflows, source-backed claims, realistic examples, and small changes that reduce ambiguity.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT. See [LICENSE](LICENSE).
