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

1. Copy [templates/AGENTS.md](templates/AGENTS.md) to your project root as `AGENTS.md` and customize it for your project. To keep your settings local, add `/AGENTS.md` to your repository’s `.git/info/exclude`.
2. In your copy, replace `../router.md` with the path from your project root to Gray Factory’s [router.md](router.md). The router resolves role links from its own directory.
3. Set `RUNTIME_ROOT` to a directory outside the product checkout. Write its path relative to the directory containing the project’s `AGENTS.md`.
4. In the same file, record the document language (`DOCUMENT_LANGUAGE`), test commands, caches, publication rules, and any mentorship settings. List each role’s profiles using paths relative to the directory containing `router.md`. For Go, CODER reads `rules/go-coding.md` for Go changes. REVIEWER and WATCHDOG read `rules/review-go.md` when reviewing Go code.

Invoke a role by adding its marker to a request, for example `@LEAD`. Ticket inputs, reports, and lifecycle state live under `RUNTIME_ROOT`.
