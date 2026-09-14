# <TicketId> — <Human Title>

TicketId: `<TXXXX>`
Role: `<ANALYST | CODER | TESTER | REVIEWER>`
Task: `<реальный внешний идентификатор рабочей задачи>`
Title: `<slug-based-short-title>`
CreatedAt: `<YYYY-MM-DD HH:MM timezone>`
OwnerRequest: `<кратко в 1–3 строках>`
PlanRef: `<relative path to PLANS/... | none>`
RepoRoot: `<относительный логический путь к Git checkout | none>`

## Сводка для владельца

`<Одним-двумя короткими абзацами без списка сообщи владельцу, что поручено агенту и какой результат ожидается. Если сейчас нужно решение владельца, сформулируй вопрос.>`

## Scope

- `<что входит в тикет>`

## OutOfScope

- `<что не входит в тикет>`

## ReadAllowlist

- `<логический корень или относительный путь>`

## WriteAllowlist

- `<конкретный ReportPath>`
- `<другой разрешённый логический корень | NONE>`

## RequiredReads

- `<правило, файл или принятый отчёт>`

## RequiredSkills

- `<skill-name — назначение | none>`

## Inputs

- `<входной артефакт или подтверждённый факт>`

## Steps

1. `<минимальный шаг>`
2. `<следующий шаг>`

## Checks

- `<команда или действие → подтверждаемый факт>`

## ArtifactsOut

- Основной OUT: `MAIL/<ROLE>/OUT/TXXXX_YYYYMMDD-HHMM_<ROLE>_<slug>_report.md`.
- Дополнительные артефакты: `<relative paths | none>`.

## Acceptance

- [ ] `<проверяемое условие>`
- [ ] `<доказательство отсутствия запрещённых эффектов>`
