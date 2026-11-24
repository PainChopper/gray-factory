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

1. Put `AGENTS.md` in the product root. It can be a symbolic link to [the shared router](router.md) when its role links resolve from your product root. For another directory layout, copy [the router template](templates/AGENTS.md) and adjust its role links to point to the Gray Factory checkout. Resolve router links from the directory containing the product’s `AGENTS.md`.
2. Create `AGENTS.project-rules.md` beside `AGENTS.md`. Every role reads it before starting. Define `PRODUCT_ROOT` (usually `./`), `RULES_ROOT` (the Gray Factory checkout), and `RUNTIME_ROOT` (a local directory outside the product checkout). For local-only settings, add `/AGENTS.project-rules.md` to the product repository’s `.git/info/exclude`.
3. In the project rules, link the applicable coding and review profiles by role and technology. For a Go project, link CODER to the [Go coding profile](rules/go-coding.md) and REVIEWER to the [Go review profile](rules/review-go.md). Use the review profile for WATCHDOG when it reviews Go code. Resolve these links from the product root.
4. Set `DOCUMENT_LANGUAGE` for tickets, reports, plans, and notes. Keep template headings and identifiers as written. Record project-specific test commands, caches, Git publication rules, and mentorship context here. Keep personal communication preferences in the owner’s machine-wide agent instructions.

Invoke a role by adding its marker to a request, for example `@LEAD`. Ticket inputs, reports, and lifecycle state live under `RUNTIME_ROOT`.
