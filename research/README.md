# Research Synthesis

Access date for this research pass: 2026-05-31.

## 1. What Makes AI Coding Agent Workflows Successful?

Successful workflows give the agent a clear goal, relevant context, constraints, and an explicit definition of done. They also give the agent a verification signal: tests, builds, lint, screenshots, logs, fixtures, or manual checks.

## 2. What Causes AI Coding Agent Workflows To Fail?

Common failure causes are vague briefs, missing reproduction steps, weak tests, excessive autonomy, poor context management, parallel sessions touching the same files, stale instructions, and unsupported assumptions about tool behavior.

## 3. What Workflow Patterns Appear Across High-Quality Sources?

The repeated pattern is: explore, plan, implement, verify, review, and learn. For simple tasks, steps can be compressed. For risky tasks, split them into separate review gates.

## 4. What Should Be Agent-Agnostic?

Task brief structure, autonomy levels, context packets, source-of-truth hierarchy, permission policy, review packet format, diff inspection, test evidence, retrospectives, and failure tracking.

## 5. What Should Be Tool-Specific?

Instruction filenames, loading behavior, sandbox controls, approval controls, hooks, skills, subagents, MCP, automations, IDE behavior, and cloud review bot behavior.

## 6. What Context Do Agents Need Before Editing Code?

Agents need the objective, relevant files, current behavior, expected behavior, reproduction steps, constraints, commands, acceptance criteria, and stop conditions.

## 7. How Should A Human Choose The Agent's Autonomy Level?

Choose by risk, reversibility, test strength, and clarity. Use A0 for research, A1 for plans needing approval, A2 for bounded changes, A3 for implementation plus review packet, A4 only for small mature subsystems, and avoid A5 for now.

## 8. How Should Agent Work Be Reviewed?

Review the diff against the task, inspect verification evidence, check for unrelated refactors, look for invented APIs, review security-sensitive areas, and require a review packet.

## 9. How Should Sources Be Recorded?

Important claims go in [claims-index.md](claims-index.md) and point to source cards. Each card records title, author, URL, date, accessed date, type, reliability, claims, caveats, implications, and usage.

## 10. How Should This Workflow Kit Avoid Becoming Bloated?

Add documents only when they support a real decision or repeated workflow. Move tool-specific material into adapters. Delete vague, duplicated, or unsupported material during maintenance reviews.
