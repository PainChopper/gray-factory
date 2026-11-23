# Gray Factory

Gray Factory is a role-based workflow for AI-assisted project work. It keeps task coordination, implementation, testing, and review in separate roles and records each handoff in Markdown.

| Role | Responsibility |
| --- | --- |
| [LEAD](rules/LEAD.md) | Define tasks, route work, and accept role reports. |
| [ANALYST](rules/ANALYST.md) | Investigate unknowns and compare options. |
| [CODER](rules/CODER.md) | Implement an agreed change and run its checks. |
| [TESTER](rules/TESTER.md) | Verify a specific behavior and report evidence. |
| [REVIEWER](rules/REVIEWER.md) | Review changes independently. |
| [WATCHDOG](rules/WATCHDOG.md) | Audit the overall result and workflow for the owner. |
| [TEACHER](rules/TEACHER.md) | Help the owner learn and work through the next step. |

## Connect a project

1. Copy [the AGENTS.md template](templates/AGENTS.md) to the project root. Set `PRODUCT_ROOT` to `./`, `RULES_ROOT` to the root of the Gray Factory checkout, and `RUNTIME_ROOT` to a local directory outside the project checkout. For sibling checkouts, example values are `../gray-factory/` for the rules and `../project-agent-runtime/` for the runtime.
2. Rewrite the template's `../rules/…` link destinations as paths from the copied `AGENTS.md` through your `RULES_ROOT`, for example `../gray-factory/rules/CODER.md`. For each language in your project, link the applicable coding and review profiles directly in the role entries, including the WATCHDOG entry where applicable. The template supplies Go profiles. Replace or remove them as appropriate for your project.
3. Add a direct link to your project settings in the copied `AGENTS.md`. Tell all roles to read those settings before working. Record the language for ticket, report, plan, and note content as `DOCUMENT_LANGUAGE`. Keep the shared template headings and identifiers. Put any project-specific tool commands, cache locations, Git publication rules, or mentorship context in that settings file.
4. Add `/PERSONAL.md` to the project's `.gitignore`. If you use personal communication preferences, save them in a local `PERSONAL.md` next to the copied `AGENTS.md`. Remove the inline code formatting around the example sentence under personal preferences so the router links directly to the optional file.

Invoke a role by adding its marker to a request, for example `@LEAD`. Ticket inputs, reports, and lifecycle state live under `RUNTIME_ROOT`.
