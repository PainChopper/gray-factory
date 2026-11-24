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

- `@TEACHER` — [TEACHER.md](../../gray-factory/rules/TEACHER.md). На этом остановись: общие правила рабочих ролей к TEACHER не относятся. TEACHER работает непосредственно с владельцем.
- `@WATCHDOG` — [WATCHDOG.md](../../gray-factory/rules/WATCHDOG.md), затем [PRINCIPLES.md](../../gray-factory/rules/PRINCIPLES.md), [COMMON.md](../../gray-factory/rules/COMMON.md) и [LEAD.md](../../gray-factory/rules/LEAD.md) как описание того, что ожидается от команды. Обязанности из этих трёх файлов к WATCHDOG не относятся. При ревью Go-кода прочитай также [REVIEW-GO.md](../../gray-factory/rules/REVIEW-GO.md). WATCHDOG работает непосредственно с владельцем.
- Рабочие роли — сначала [PRINCIPLES.md](../../gray-factory/rules/PRINCIPLES.md) и [COMMON.md](../../gray-factory/rules/COMMON.md), затем правила назначенной роли:
  - `@LEAD` — [LEAD.md](../../gray-factory/rules/LEAD.md).
  - `@ANALYST` — [ANALYST.md](../../gray-factory/rules/ANALYST.md).
  - `@CODER` — [CODER.md](../../gray-factory/rules/CODER.md) и [GO-CODING.md](../../gray-factory/rules/GO-CODING.md).
  - `@TESTER` — [TESTER.md](../../gray-factory/rules/TESTER.md).
  - `@REVIEWER` — [REVIEWER.md](../../gray-factory/rules/REVIEWER.md) и [REVIEW-GO.md](../../gray-factory/rules/REVIEW-GO.md).
