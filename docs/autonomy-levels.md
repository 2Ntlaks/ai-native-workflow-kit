# Autonomy Levels

Autonomy is the amount of initiative the agent may take before stopping for human approval. It is separate from permissions. A task can be low-autonomy but still require read access, or high-autonomy but stay inside a narrow sandbox.

## A0: Research Only. No Edits.

Use when the human needs understanding, source notes, options, risk analysis, or codebase orientation.

Do not use when the desired output is a code change.

Allowed agent behavior: read files, inspect docs, search approved sources, summarize findings, compare options, identify risks, and recommend next steps.

Stop conditions: missing source, conflicting evidence, need for credentials, need for code edits, or a decision that affects scope.

Human review requirement: verify sources and decide whether to move to A1 or A2.

Example tasks:

- C: inspect a linked-list assignment and explain likely edge cases.
- Java: compare persistence options for a Swing desktop app.
- WebGL: research how the current render loop handles resizing.
- Databases: inspect schema and explain migration risks.
- Embedded systems: review Arduino pin usage before hardware changes.
- Tutoring systems: summarize how student progress is currently stored.

## A1: Propose Plan. Wait For Approval.

Use when work is multi-step, ambiguous, risky, or likely to touch several files.

Do not use for tiny obvious edits where A2 is already safe.

Allowed agent behavior: inspect code, ask clarifying questions, propose a plan, list files, define verification, and wait.

Stop conditions: plan uncertainty, missing context, broad refactor temptation, dependency changes, migrations, or permission escalation.

Human review requirement: approve, edit, or reject the plan before implementation.

Example tasks:

- C: plan a test harness for pointer-heavy exercises.
- Java: plan a settings dialog without changing UI code yet.
- WebGL: plan a camera-control refactor.
- Databases: plan a migration with rollback steps.
- Embedded systems: plan sensor calibration changes.
- Tutoring systems: plan a lesson scheduling feature.

## A2: Implement Bounded Change. Run Verification.

Use when the task has clear scope, relevant files, acceptance criteria, and verification commands.

Do not use when the agent must make product decisions or touch sensitive systems without approval.

Allowed agent behavior: edit scoped files, run agreed checks, fix failures within scope, and produce a review packet.

Stop conditions: tests require external services, implementation exceeds scope, dependency changes are needed, behavior conflicts with docs, or a sensitive area is touched.

Human review requirement: inspect diff, tests, and review packet before accepting.

Example tasks:

- C: add unit tests for a sorting assignment helper.
- Java: fix a null selection crash in a desktop form.
- WebGL: correct projection aspect ratio handling.
- Databases: add an approved non-destructive index migration.
- Embedded systems: adjust debounce logic with serial-test evidence.
- Tutoring systems: fix invoice total formatting.

## A3: Implement, Test, Document, And Prepare Review Packet.

Use when the agent can own a coherent small task end-to-end and tests are available.

Do not use when review must happen after every file or when acceptance criteria are unclear.

Allowed agent behavior: implement scoped feature, add or update tests, update docs, run verification, and prepare PR-style notes.

Stop conditions: product ambiguity, public API change, security-sensitive code, hidden dependency on production data, or failing checks outside scope.

Human review requirement: review packet plus focused diff review. The human may request a second review pass.

Example tasks:

- C: create a worked example and tests for a recursion lesson.
- Java: implement local CSV export for a desktop table.
- WebGL: add a grid toggle with UI state and verification.
- Databases: implement a small read-only report query and docs.
- Embedded systems: add a simulated test for a finite-state controller.
- Tutoring systems: add a student attendance summary screen.

## A4: Own A Small Subsystem Under Strict Rules.

Use only when the subsystem has clear boundaries, mature tests, stable patterns, and explicit permissions.

Do not use for new architecture, auth, billing, production migrations, or student/private data handling.

Allowed agent behavior: maintain a bounded subsystem, triage issues, implement small changes, update tests/docs, and escalate on boundary crossings.

Stop conditions: boundary ambiguity, test coverage gap, architecture decision, dependency change, security risk, or repeated failures.

Human review requirement: scheduled review, diff review for every merge, and periodic retrospective.

Example tasks:

- C: maintain a small exercise test runner.
- Java: own a preferences module in a desktop app.
- WebGL: maintain shader examples under a teaching visualizer.
- Databases: maintain analytics views without schema ownership.
- Embedded systems: maintain simulation-only firmware helpers.
- Tutoring systems: maintain non-sensitive notification templates.

## A5: Broad Autonomous Development. Dangerous For Now.

Use only when project rules, tests, permissions, monitoring, and rollback are mature. This kit assumes A5 should usually be avoided.

Do not use for student projects, final-year deliverables, production data, security, migrations, or unfamiliar codebases.

Allowed agent behavior: broad work only under explicit written rules and strong isolation.

Stop conditions: almost any uncertainty, failing checks, permission escalation, unclear ownership, or missing rollback.

Human review requirement: mandatory design review, implementation review, security review, and merge readiness review.

Example tasks:

- C: not recommended beyond isolated practice repos.
- Java: not recommended beyond disposable prototypes.
- WebGL: not recommended beyond experimental branches.
- Databases: avoid.
- Embedded systems: avoid where hardware or safety is involved.
- Tutoring systems: avoid where real student or payment data exists.
