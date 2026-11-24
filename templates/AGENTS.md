# Агенты проекта

Перед началом работы прочитай [правила проекта](./AGENTS.project-rules.md) из корня продукта.

Пути в этом роутере отсчитываются от каталога `AGENTS.md` в продукте. Правила проекта задают `PRODUCT_ROOT`, `RULES_ROOT`, `RUNTIME_ROOT` и применимые профили ролей.

## Маршрутизация

Роль задаётся маркером `@<ROLE>` в запросе. Без маркера выполняй прямой запрос владельца без назначения себе роли. Если маркер неизвестен, уточни назначение.

При первом запросе с маркером `@<ROLE>` и после каждого сжатия контекста полностью прочитай указанные для роли файлы и применимые профили из правил проекта до ответа или действий.

- `@TEACHER` — [teacher.md](../rules/teacher.md). На этом остановись: общие правила рабочих ролей к TEACHER не относятся. TEACHER работает непосредственно с владельцем.
- `@WATCHDOG` — [watchdog.md](../rules/watchdog.md), затем [principles.md](../rules/principles.md), [common.md](../rules/common.md) и [lead.md](../rules/lead.md) как описание того, что ожидается от команды. Обязанности из этих трёх файлов к WATCHDOG не относятся. WATCHDOG работает непосредственно с владельцем.
- Рабочие роли — сначала [principles.md](../rules/principles.md) и [common.md](../rules/common.md), затем правила назначенной роли:
  - `@LEAD` — [lead.md](../rules/lead.md).
  - `@ANALYST` — [analyst.md](../rules/analyst.md).
  - `@CODER` — [coder.md](../rules/coder.md).
  - `@TESTER` — [tester.md](../rules/tester.md).
  - `@REVIEWER` — [reviewer.md](../rules/reviewer.md).
