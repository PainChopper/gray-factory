# Агенты ingestion-lab

## Корни

- `PRODUCT_ROOT` — `./`
- `RULES_ROOT` — `../ingestion-lab-agents/`
- `RUNTIME_ROOT` — `../ingestion-lab-agents-runtime/`

Пути корней и ссылки отсчитываются от `AGENTS.md` в checkout продукта, где находится символическая ссылка. Правила лежат в соседнем checkout `../ingestion-lab-agents`. [Публичный репозиторий Gray Factory](https://github.com/PainChopper/gray-factory).

## Настройки проекта

Все роли, включая TEACHER и WATCHDOG, до начала работы читают [настройки проекта](../ingestion-lab-agents/PROJECT.ingestion-lab.md).

## Персональные предпочтения

Если рядом есть [PERSONAL.md](PERSONAL.md), прочитай его до ответа: там предпочтения владельца по общению.

## Маршрутизация

Роль задаётся маркером `@<ROLE>` в запросе. Без маркера выполняй прямой запрос владельца без назначения себе роли. Если маркер неизвестен, уточни назначение.

При первом запросе с маркером `@<ROLE>` и после каждого сжатия контекста полностью прочитай указанные для роли файлы до ответа или действий.

- `@TEACHER` — [TEACHER.md](../ingestion-lab-agents/rules/TEACHER.md). На этом остановись: общие правила рабочих ролей к TEACHER не относятся. TEACHER работает непосредственно с владельцем.
- `@WATCHDOG` — [WATCHDOG.md](../ingestion-lab-agents/rules/WATCHDOG.md), затем [PRINCIPLES.md](../ingestion-lab-agents/rules/PRINCIPLES.md), [COMMON.md](../ingestion-lab-agents/rules/COMMON.md) и [LEAD.md](../ingestion-lab-agents/rules/LEAD.md) как описание того, что ожидается от команды. Обязанности из этих трёх файлов к WATCHDOG не относятся. При ревью Go-кода прочитай также [REVIEW-GO.md](../ingestion-lab-agents/rules/REVIEW-GO.md). WATCHDOG работает непосредственно с владельцем.
- Рабочие роли — сначала [PRINCIPLES.md](../ingestion-lab-agents/rules/PRINCIPLES.md) и [COMMON.md](../ingestion-lab-agents/rules/COMMON.md), затем правила назначенной роли:
  - `@LEAD` — [LEAD.md](../ingestion-lab-agents/rules/LEAD.md).
  - `@ANALYST` — [ANALYST.md](../ingestion-lab-agents/rules/ANALYST.md).
  - `@CODER` — [CODER.md](../ingestion-lab-agents/rules/CODER.md) и [GO-CODING.md](../ingestion-lab-agents/rules/GO-CODING.md).
  - `@TESTER` — [TESTER.md](../ingestion-lab-agents/rules/TESTER.md).
  - `@REVIEWER` — [REVIEWER.md](../ingestion-lab-agents/rules/REVIEWER.md) и [REVIEW-GO.md](../ingestion-lab-agents/rules/REVIEW-GO.md).
