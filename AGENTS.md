# AGENTS.md

Instructions for agents editing this repository.

## Mission

Keep this kit usable for delegating real software work. A change belongs here only if it helps a human prepare a task, choose autonomy, review agent output, record sources, or prevent a repeated failure.

## Rules

- Prefer specific steps, templates, checklists, examples, and review gates over advice.
- Keep tool-specific behavior in `adapters/`; keep general workflow rules in `docs/`, `workflows/`, `templates/`, and `checklists/`.
- Record important external claims in `research/claims-index.md` and `research/source-cards/`.
- Mark live product behavior, uncertain support, and unverified capabilities as `verify before use`.
- If repo files, tests, docs, task briefs, or sources conflict, report the conflict instead of guessing.
- Remove duplicated or vague text when you touch nearby content.

## Done Criteria

- The changed file can be used on a real agent task without extra explanation.
- The diff is scoped to the task.
- Important claims are sourced or explicitly marked unverified.
- Implementation work ends with the review packet sections in `templates/review-packet.md`.
