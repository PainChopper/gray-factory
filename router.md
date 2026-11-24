# Агенты проекта

Перед началом работы прочитай [правила проекта](./AGENTS.project-rules.md) из корня продукта.

Пути в этом роутере отсчитываются от каталога `AGENTS.md` в продукте. Правила проекта задают `PRODUCT_ROOT`, `RULES_ROOT`, `RUNTIME_ROOT` и применимые профили ролей.

## Маршрутизация

Роль задаётся маркером `@<ROLE>` в запросе. Без маркера выполняй прямой запрос владельца без назначения себе роли. Если маркер неизвестен, уточни назначение.

При первом запросе с маркером `@<ROLE>` и после каждого сжатия контекста полностью прочитай указанные для роли файлы и применимые профили из правил проекта до ответа или действий.

- `@TEACHER` — [teacher.md](../../gray-factory/rules/teacher.md). На этом остановись: общие правила рабочих ролей к TEACHER не относятся. TEACHER работает непосредственно с владельцем.
- `@WATCHDOG` — [watchdog.md](../../gray-factory/rules/watchdog.md), затем [principles.md](../../gray-factory/rules/principles.md), [common.md](../../gray-factory/rules/common.md) и [lead.md](../../gray-factory/rules/lead.md) как описание того, что ожидается от команды. Обязанности из этих трёх файлов к WATCHDOG не относятся. WATCHDOG работает непосредственно с владельцем.
- Рабочие роли — сначала [principles.md](../../gray-factory/rules/principles.md) и [common.md](../../gray-factory/rules/common.md), затем правила назначенной роли:
  - `@LEAD` — [lead.md](../../gray-factory/rules/lead.md).
  - `@ANALYST` — [analyst.md](../../gray-factory/rules/analyst.md).
  - `@CODER` — [coder.md](../../gray-factory/rules/coder.md).
  - `@TESTER` — [tester.md](../../gray-factory/rules/tester.md).
  - `@REVIEWER` — [reviewer.md](../../gray-factory/rules/reviewer.md).
