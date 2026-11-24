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

- `@TEACHER` — [teacher.md](../rules/teacher.md). На этом остановись: общие правила рабочих ролей к TEACHER не относятся. TEACHER работает непосредственно с владельцем.
- `@WATCHDOG` — [watchdog.md](../rules/watchdog.md), затем [principles.md](../rules/principles.md), [common.md](../rules/common.md) и [lead.md](../rules/lead.md) как описание того, что ожидается от команды. Обязанности из этих трёх файлов к WATCHDOG не относятся. При ревью Go-кода прочитай также [review-go.md](../rules/review-go.md). WATCHDOG работает непосредственно с владельцем.
- Рабочие роли — сначала [principles.md](../rules/principles.md) и [common.md](../rules/common.md), затем правила назначенной роли:
  - `@LEAD` — [lead.md](../rules/lead.md).
  - `@ANALYST` — [analyst.md](../rules/analyst.md).
  - `@CODER` — [coder.md](../rules/coder.md). Заменяемый пример профиля языка для Go — [go-coding.md](../rules/go-coding.md).
  - `@TESTER` — [tester.md](../rules/tester.md).
  - `@REVIEWER` — [reviewer.md](../rules/reviewer.md). Заменяемый пример профиля языка для Go — [review-go.md](../rules/review-go.md).
