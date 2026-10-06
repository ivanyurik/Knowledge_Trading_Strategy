# Knowledge Trading Strategy

Це довгострокова структурована база знань проєкту торгової стратегії.

Репозиторій працює за методологією Project Knowledge Manager: транскрипція є вхідним матеріалом, але сирий ASR-текст НІКОЛИ не зберігається в GitHub.

## Канонічний принцип

Кожна нова транскрипція проходить повний transcription correction pass до вилучення knowledge.
- HIGH-confidence ASR-помилки виправляються.
- MEDIUM-confidence місця позначаються NEEDS_REVIEW без вигадування тексту.
- LOW-confidence місця не вгадуються.
- У GitHub зберігається тільки corrected canonical transcript.
- Raw ASR, backup/raw copy та audit-копії raw transcript не створюються.

## Processing flow

1. Отримати transcript як input.
2. Перевірити repository structure, system instructions та indexes.
3. Повністю перевірити й виправити transcription.
4. Зберегти тільки canonical transcript у 01_RAW_TRANSCRIPTS/YYYY/MM/.
5. Витягнути всі knowledge categories.
6. Знайти existing knowledge та повторно використати IDs.
7. Додати source traceability.
8. Оновити knowledge files, indexes та CHANGELOG.md.
9. Перечитати змінені файли й перевірити consistency.
10. Завершити Processing Report та Completion Gate.

## Repository structure

- 00_INDEX/ — навігація та індекси.
- 01_RAW_TRANSCRIPTS/ — тільки canonical corrected transcripts. Назва RAW є legacy/compatibility naming.
- 02_KNOWLEDGE/ — структуроване knowledge.
- 03_DECISIONS/ — decision records.
- 04_OPEN_QUESTIONS/ — unresolved questions.
- 05_CONFLICTS/ — explicit conflicts.
- 99_SYSTEM/ — операційні правила Knowledge Manager.
- CHANGELOG.md — історія змін.
- INBOX/ більше не є частиною processing model і не використовується для зберігання transcripts.

## Core rules

- Не вигадувати невизначені формулювання.
- Не перетворювати proposals на decisions.
- Не перетворювати assumptions на requirements.
- Не приховувати conflicts.
- Не дублювати knowledge items.
- Кожен extracted fact має source reference.
- PROCESSED дозволений лише після проходження всіх mandatory checks.

Повна методологія: 99_SYSTEM/METHODOLOGY.md.
Операційні інструкції: 99_SYSTEM/AGENT_INSTRUCTIONS.md.