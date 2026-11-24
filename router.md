# Агенты ingestion-lab

## Корни

- `PRODUCT_ROOT` — `./`
- `RULES_ROOT` — `../../gray-factory/`
- `RUNTIME_ROOT` — `../ingestion-lab-agents-runtime/`

Пути корней и ссылки отсчитываются от `AGENTS.md` в checkout продукта, где находится символическая ссылка. Правила лежат в checkout `../../gray-factory/`. [Публичный репозиторий Gray Factory](https://github.com/PainChopper/gray-factory).

## Настройки проекта

Все роли, включая TEACHER и WATCHDOG, до начала работы читают [настройки проекта](../../gray-factory/PROJECT.ingestion-lab.md).

## Маршрутизация

Роль задаётся маркером `@<ROLE>` в запросе. Без маркера выполняй прямой запрос владельца без назначения себе роли. Если маркер неизвестен, уточни назначение.

При первом запросе с маркером `@<ROLE>` и после каждого сжатия контекста полностью прочитай указанные для роли файлы до ответа или действий.

- `@TEACHER` — [teacher.md](../../gray-factory/rules/teacher.md). На этом остановись: общие правила рабочих ролей к TEACHER не относятся. TEACHER работает непосредственно с владельцем.
- `@WATCHDOG` — [watchdog.md](../../gray-factory/rules/watchdog.md), затем [principles.md](../../gray-factory/rules/principles.md), [common.md](../../gray-factory/rules/common.md) и [lead.md](../../gray-factory/rules/lead.md) как описание того, что ожидается от команды. Обязанности из этих трёх файлов к WATCHDOG не относятся. При ревью Go-кода прочитай также [review-go.md](../../gray-factory/rules/review-go.md). WATCHDOG работает непосредственно с владельцем.
- Рабочие роли — сначала [principles.md](../../gray-factory/rules/principles.md) и [common.md](../../gray-factory/rules/common.md), затем правила назначенной роли:
  - `@LEAD` — [lead.md](../../gray-factory/rules/lead.md).
  - `@ANALYST` — [analyst.md](../../gray-factory/rules/analyst.md).
  - `@CODER` — [coder.md](../../gray-factory/rules/coder.md) и [go-coding.md](../../gray-factory/rules/go-coding.md).
  - `@TESTER` — [tester.md](../../gray-factory/rules/tester.md).
  - `@REVIEWER` — [reviewer.md](../../gray-factory/rules/reviewer.md) и [review-go.md](../../gray-factory/rules/review-go.md).
