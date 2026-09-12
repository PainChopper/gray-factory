# <TicketId> — <Human Title>

Result: `<значение согласно rules/<ROLE>.md>`
CreatedAt: `<YYYY-MM-DD HH:MM timezone>`
TicketId: `<TXXXX>`
Task: `<реальный внешний идентификатор, например SMS-745>`
Role: `<REVIEWER>`
Title: `<slug-based-short-title>`
SourceTicket: `<MAIL/<ROLE>/IN/...md | direct-owner-request>`

## Сводка для владельца

- Надо: `<что требовалось независимо проверить>`
- Проверено: `<что проверено простыми словами>`
- Итог: `<принято | не принято | доказательств недостаточно — почему>`
- Дальше: `<следующий понятный шаг | ничего>`
- От владельца: `<ничего | одно конкретное решение>`

## VerificationTarget

`<стабильный объект проверки>`

## Inputs

- `<TaskPath, отчёт, diff, артефакт или исходное состояние>`

## Procedure

- `<независимое действие, команда или сценарий>`

## Evidence

- `<наблюдаемый факт, exit code или RUNLOGS/...>`

## ChangedFiles

- `<относительный путь каждого изменённого файла | NONE, если verification была read-only>`

## AcceptanceMatrix

| Критерий/запрет | Procedure | Evidence | Результат |
|---|---|---|---|
| `<условие>` | `<проверка>` | `<факт>` | `<выполнен | не выполнен | не проверен>` |

## IssuesAndLimitations

- `<дефект, ограничение или непроверенная область | none>`

## RequiredFixOrEvidence

- `<минимальное исправление или evidence | none>`

## FollowUp

- `<handoff LEAD>`
