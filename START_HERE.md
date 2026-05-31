# Start Here

Use this process whenever you want an agent to help with software work.

1. Define the task.
2. Choose a workflow.
3. Choose autonomy level.
4. Prepare context packet.
5. Fill task brief.
6. Ask agent for research or plan.
7. Approve or adjust.
8. Let agent implement.
9. Review using checklists.
10. Save review packet and retrospective.
11. Update the kit if a repeated failure appears.

## Default Path

Use [spec-to-plan.md](workflows/spec-to-plan.md), then [feature-implementation.md](workflows/feature-implementation.md) or [bug-fix.md](workflows/bug-fix.md). Default to A1 for unclear work and A2 for bounded implementation.

## Stop Immediately If

- The agent needs secrets, credentials, private student data, or production access.
- The task touches authentication, authorization, payment, migrations, destructive file operations, or deployment settings without explicit permission.
- The agent's plan conflicts with current code, tests, or official documentation.
- The agent cannot explain verification evidence.
