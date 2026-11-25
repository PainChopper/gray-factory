# Gray Factory

Gray Factory is a role-based workflow for AI-assisted project work. It keeps task coordination, implementation, testing, and review in separate roles and records each handoff in Markdown.

| Role | Responsibility |
| --- | --- |
| [LEAD](rules/lead.md) | Define tasks, route work, and accept role reports. |
| [ANALYST](rules/analyst.md) | Investigate unknowns and compare options. |
| [CODER](rules/coder.md) | Implement an agreed change and run its checks. |
| [TESTER](rules/tester.md) | Verify a specific behavior and report evidence. |
| [REVIEWER](rules/reviewer.md) | Review changes independently. |
| [WATCHDOG](rules/watchdog.md) | Audit the overall result and workflow for the owner. |
| [TEACHER](rules/teacher.md) | Help the owner learn and work through the next step. |

## Connect a project

1. Clone Gray Factory with `git clone https://github.com/PainChopper/gray-factory.git`. You can use the same checkout for multiple projects.
2. Copy [templates/AGENTS.md](templates/AGENTS.md) from that checkout to your project root as `AGENTS.md` and customize it for your project. To keep your settings local, add `/AGENTS.md` to your repository’s `.git/info/exclude`.
3. In your copy, fill in the path to [router.md](router.md) in your Gray Factory checkout. Use an absolute path or a path relative to your project’s `AGENTS.md`.
4. Set `RUNTIME_ROOT` to a directory outside the product checkout. Use an absolute path or a path relative to the directory containing the project’s `AGENTS.md`.
5. Set `DOCUMENT_LANGUAGE` to the language agents should use for tickets, reports, plans, and notes.
6. Add your project-specific instructions to your local `AGENTS.md` below the line that tells agents to read `router.md`. Include test commands, cache locations, publication rules, or mentorship settings as needed. List each role’s profiles using paths relative to the directory containing `router.md`. For Go, CODER reads `rules/go-coding.md` for Go changes. REVIEWER and WATCHDOG read `rules/review-go.md` when reviewing Go code.

Invoke a role by adding its marker to a request, for example `@LEAD`. Ticket inputs, reports, and lifecycle state live under `RUNTIME_ROOT`.
