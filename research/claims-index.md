# Claims Index

Use this index for claims that shape workflows, templates, checklists, or adapters. Product-specific behavior must be marked `verify before use` unless the current target environment was confirmed during the task.

| ID | Claim | Support | Verification status | Used In |
|---|---|---|---|---|
| C001 | Good agent briefs include goal, context, constraints, and done-when criteria. | [OpenAI Codex best practices](source-cards/openai-codex-best-practices.md) | Source-backed | Task brief, operating model |
| C002 | Complex tasks should separate exploration and planning from implementation. | [OpenAI Codex best practices](source-cards/openai-codex-best-practices.md), [Claude Code best practices](source-cards/anthropic-claude-code-best-practices.md) | Source-backed | Workflows, autonomy |
| C003 | Agents need runnable verification signals. | [Claude Code best practices](source-cards/anthropic-claude-code-best-practices.md) | Source-backed | Review packet, test checklist |
| C004 | Simple, composable workflows should come before complex multi-agent systems. | [Anthropic Building Effective Agents](source-cards/anthropic-building-effective-agents.md) | Source-backed | Anti-overengineering |
| C005 | Tool-specific instruction support and precedence vary. | [AGENTS.md open format](source-cards/agents-md-open-format.md), [GitHub Copilot custom instructions](source-cards/github-copilot-custom-instructions.md), [Cursor rules](source-cards/cursor-rules.md) | Verify before use in target tool | Adapters |
| C006 | Sandbox mode and approval policy are separate controls. | [OpenAI Codex security](source-cards/openai-codex-security.md) | Source-backed; local defaults vary | Security and permissions |
| C007 | Parallel sessions should not edit the same files. | [OpenAI Codex prompting](source-cards/openai-codex-prompting.md) | Source-backed | Parallel exploration |
| C008 | External benchmarks are useful but limited by task quality and environment issues. | [SWE-bench](source-cards/swe-bench.md), [SWE-bench Verified](source-cards/openai-swe-bench-verified.md) | Source-backed | Evals |

## Unverified Or Environment-Specific Claims

- Exact Codex instruction precedence, goal mode behavior, plan mode behavior, MCP availability, and approval defaults: verify in the current Codex environment.
- Exact Claude Code hooks, subagent, memory, and permission behavior: verify in current Claude Code docs and local configuration.
- Exact GitHub Copilot instruction support: verify for GitHub.com, VS Code, JetBrains, Visual Studio, Xcode, or the surface being used.
- Exact Cursor project rule behavior and AGENTS.md support: verify in current Cursor docs and the project settings.
