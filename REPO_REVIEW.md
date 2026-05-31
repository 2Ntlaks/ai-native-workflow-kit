# Repo Review

Review date: 2026-05-31

Reviewer stance: strict senior AI-native software engineer. Goal was to make the kit smaller, clearer, and more usable without adding broad new content.

## What is strong

- The repo has the right operating-system shape: research, docs, workflows, templates, checklists, examples, adapters, evals, decisions, and failures are separated cleanly.
- The autonomy model is useful and concrete. A0-A5 gives the human a simple way to control agent behavior before discussing tool permissions.
- The workflow set covers the common task lifecycle: context, research, plan, implement, test, review, and retrospective.
- Source tracking exists in `research/source-index.md`, `research/claims-index.md`, and `research/source-cards/`.
- Tool adapters are concise and do not duplicate the full manual.
- The kit explicitly treats verification, review packets, source conflicts, and stop conditions as first-class parts of agent work.

## What is weak

- Several templates were too empty to copy into a real task without extra thinking.
- The checklists repeated a generic intro and did not always say what decision the human was making.
- The examples named the owner's real domains but initially read like placeholders instead of real agent briefs.
- Some source claims were recorded but did not make verification status obvious enough.
- The workflow index did not help a human choose a workflow quickly.
- Some phrasing was aspirational, such as "useful" or "practical", without saying what to inspect or block.

## What was removed or simplified

- Removed the repeated checklist opener and replaced it with checklist-specific decision guidance.
- Replaced vague README framing with a clearer statement that the kit exists for task preparation, review gates, and retrospectives.
- Replaced "where practical" style wording with explicit alternatives: add a test, or document the manual check and why automation was not added.
- Simplified AGENTS.md into mission, rules, and done criteria so it stays a lightweight instruction file rather than a duplicate manual.

## What was improved

- Made core templates copy-paste ready: `agent-task-brief.md`, `project-context.md`, `research-brief.md`, `feature-spec.md`, `bug-investigation.md`, `implementation-plan.md`, `test-plan.md`, `review-packet.md`, `pull-request-description.md`, `architecture-decision-record.md`, `after-action-report.md`, `decision-journal-entry.md`, `failure-report.md`, and `source-card.md`.
- Made checklists faster to use by tying each to a review decision: readiness, context, plan approval, implementation, tests, security, docs, overengineering, merge readiness, and research quality.
- Made examples more realistic for C assignment testing, Java desktop apps, WebGL visualizers, database schema changes, embedded systems, tutoring systems, and local-first desktop apps.
- Added verification status to `research/claims-index.md` and listed environment-specific claims that must be checked in the target tool.
- Added a workflow selection table to `workflows/README.md`.
- Tightened anti-overengineering guidance into removal rules instead of general advice.

## Remaining risks

- Source cards are source-backed but not deeply quoted; future maintainers should re-check live docs before relying on exact product behavior.
- Example folders now have stronger task briefs, but their `agent-plan.md` and `expected-review-packet.md` files are still intentionally generic. They may need one more pass after the owner runs real tasks.
- The kit is documentation-only. Its effectiveness depends on the human actually using review packets, checklists, and failure records.
- The repo is not currently a Git repository, so there is no commit history for future agents to inspect.
- Some workflows remain necessarily general because they must apply across C, Java, WebGL, databases, embedded systems, and desktop apps.

## Recommended next actions

1. Use `templates/agent-task-brief.md` on the next real bug fix or feature task.
2. Save the agent's final response using `templates/review-packet.md`.
3. Review the result with `checklists/implementation-review.md` and `checklists/test-review.md`.
4. If the agent makes a repeated mistake, record it in `failures/failure-template.md` and update one checklist or template.
5. After three real tasks, revisit the example folders and replace any remaining generic plans with real review packets.
