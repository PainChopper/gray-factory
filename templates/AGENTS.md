# Агенты проекта

## Корни

- `PRODUCT_ROOT` — `./`
- `RULES_ROOT` — `<путь к корню Gray Factory>`
- `RUNTIME_ROOT` — `<путь к локальному runtime>`

Пути корней и ссылки отсчитываются от этого файла.

## Настройки проекта

<!-- Вставь прямую Markdown-ссылку на файл настроек проекта, который должны прочитать все роли, включая TEACHER и WATCHDOG. -->

## Персональные предпочтения

`Если рядом есть [PERSONAL.md](PERSONAL.md), прочитай его до ответа: там предпочтения владельца по общению.`

## Маршрутизация

Роль задаётся маркером `@<ROLE>` в запросе. Без маркера выполняй прямой запрос владельца без назначения себе роли. Если маркер неизвестен, уточни назначение.

При первом запросе с маркером `@<ROLE>` и после каждого сжатия контекста полностью прочитай указанные для роли файлы до ответа или действий.

- `@TEACHER` — [TEACHER.md](../rules/TEACHER.md). На этом остановись: общие правила рабочих ролей к TEACHER не относятся. TEACHER работает непосредственно с владельцем.
- `@WATCHDOG` — [WATCHDOG.md](../rules/WATCHDOG.md), затем [PRINCIPLES.md](../rules/PRINCIPLES.md), [COMMON.md](../rules/COMMON.md) и [LEAD.md](../rules/LEAD.md) как описание того, что ожидается от команды. Обязанности из этих трёх файлов к WATCHDOG не относятся. При ревью Go-кода прочитай также [REVIEW-GO.md](../rules/REVIEW-GO.md). WATCHDOG работает непосредственно с владельцем.
- Рабочие роли — сначала [PRINCIPLES.md](../rules/PRINCIPLES.md) и [COMMON.md](../rules/COMMON.md), затем правила назначенной роли:
  - `@LEAD` — [LEAD.md](../rules/LEAD.md).
  - `@ANALYST` — [ANALYST.md](../rules/ANALYST.md).
  - `@CODER` — [CODER.md](../rules/CODER.md). Заменяемый пример профиля языка для Go — [GO-CODING.md](../rules/GO-CODING.md).
  - `@TESTER` — [TESTER.md](../rules/TESTER.md).
  - `@REVIEWER` — [REVIEWER.md](../rules/REVIEWER.md). Заменяемый пример профиля языка для Go — [REVIEW-GO.md](../rules/REVIEW-GO.md).
