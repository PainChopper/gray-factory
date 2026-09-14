# <TicketId> — <Human Title>

Result: `<значение согласно rules/<ROLE>.md>`
CreatedAt: `<YYYY-MM-DD HH:MM timezone>`
TicketId: `<TXXXX>`
Task: `<реальный внешний идентификатор рабочей задачи>`
Role: `<ANALYST | CODER | TESTER>`
Title: `<slug-based-short-title>`
SourceTicket: `<MAIL/<ROLE>/IN/...md | direct-owner-request>`

**Сводка для владельца**

`<Одним-двумя короткими абзацами без списка сообщи владельцу, что сделано или проверено и каков итог. Укажи следующий шаг и вопрос владельцу, только если они действительно нужны.>`

## FACTS

### Summary

`<что фактически произошло>`

### Delivered

- `<что произведено или зафиксировано>`

### ChangedFiles

- `<relative path | NONE>`

### ChecksRun

- `<команда/действие → exit code или наблюдение>`

### EvidenceAndArtifacts

- `<RUNLOGS/... или другой relative path | none>`

## JUDGMENT

### ResultBasis

- `<критерий → evidence → вывод>`

### ScopeCompliance

- `<доказательство соблюдения scope и запретов>`

### IssuesAndRisks

- `<проблема, риск или непроверенное условие | none>`

### NotDoneBecauseOutOfScope

- `<сознательно не выполненная идея | none>`

### FollowUp

- `<минимальный handoff | none>`

## Blocker

`<для BLOCKED: блокер, факты, условие продолжения и один вопрос при необходимости | not applicable>`

## FailureReason

`<для FAILED: точная причина | not applicable>`
