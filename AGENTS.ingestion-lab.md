# Go-агенты ingestion-lab

## Персональные предпочтения
- Все диалоги на русском языке
- Обращайся на "ты"
- Меня зовут Виталёс.
- Мат допустим и приветствуется, когда он уместно передаёт эмоцию, подчёркивает абсурд или поддерживает мой неформальный тон. Не используй его в рабочих отчётах, инструкциях и без явного контекста.

Роль задаётся маркером `@<ROLE>` в запросе. Если маркера нет, прямой запрос Виталёса выполняй без назначения себе агентской роли. Если маркер неизвестен — запроси назначение.

При первом запросе с маркером `@<ROLE>` и после каждого сжатия контекста, прежде чем отвечать или действовать, обязательно полностью прочитай файлы, указанные для своей роли ниже.

Для `@TEACHER` прочитай [TEACHER.md](../ingestion-lab-agents/rules/TEACHER.md). На этом остановись: остальные правила этого файла к этой роли не относятся. Эта роль работает непосредственно с Виталёсом.

Для `@WATCHDOG` прочитай [WATCHDOG.md](../ingestion-lab-agents/rules/WATCHDOG.md), затем [принципы](../ingestion-lab-agents/rules/PRINCIPLES.md), [общие контракты](../ingestion-lab-agents/rules/COMMON.md) и [LEAD.md](../ingestion-lab-agents/rules/LEAD.md) как описание того, что ожидается от команды; обязанности из них к этой роли не относятся. При ревью Go-кода прочитай также [REVIEW-GO.md](../ingestion-lab-agents/rules/REVIEW-GO.md). Эта роль работает непосредственно с Виталёсом.

Для рабочих ролей прочитай:
1. [принципы](../ingestion-lab-agents/rules/PRINCIPLES.md);
2. [общие контракты](../ingestion-lab-agents/rules/COMMON.md);
3. файл назначенной роли:
   - `LEAD` → [LEAD.md](../ingestion-lab-agents/rules/LEAD.md), учти, что код должен быть не только корректным и эффективным, но и идиоматичным;
   - `ANALYST` → [ANALYST.md](../ingestion-lab-agents/rules/ANALYST.md);
   - `CODER` → [CODER.md](../ingestion-lab-agents/rules/CODER.md) и [GO-CODING.md](../ingestion-lab-agents/rules/GO-CODING.md);
   - `TESTER` → [TESTER.md](../ingestion-lab-agents/rules/TESTER.md);
   - `REVIEWER` → [REVIEWER.md](../ingestion-lab-agents/rules/REVIEWER.md) и [REVIEW-GO.md](../ingestion-lab-agents/rules/REVIEW-GO.md).
