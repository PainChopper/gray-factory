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
2. In that file, set the link to [the shared router](router.md) relative to the product root. This one link locates Gray Factory. The router resolves role links from its own directory.
3. Set `PRODUCT_ROOT` to the directory containing the product’s `AGENTS.md`. Choose a local `RUNTIME_ROOT` outside the product checkout, relative to `PRODUCT_ROOT`. Use the linked router’s directory as `RULES_ROOT`.
4. In the same file, record the document language (`DOCUMENT_LANGUAGE`), test commands, caches, publication rules, and any mentorship settings. List the profiles each role should read for the project’s stack. For Go, use `RULES_ROOT/rules/go-coding.md` for CODER and `RULES_ROOT/rules/review-go.md` for REVIEWER and WATCHDOG when reviewing Go. The agent substitutes the router’s directory for `RULES_ROOT` in these paths.

Invoke a role by adding its marker to a request, for example `@LEAD`. Ticket inputs, reports, and lifecycle state live under `RUNTIME_ROOT`.
