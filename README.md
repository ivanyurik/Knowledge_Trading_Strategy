# Knowledge Trading Strategy

Це довгострокова структурована база знань проєкту торгової стратегії.

## Головна мета

Репозиторій побудований не як архів транскрипцій, а як система швидкого відновлення знань.

Користувач повинен мати змогу запитати про конкретну тему, а агент має:
1. знайти тему в `00_INDEX/TOPIC_INDEX.md`;
2. визначити пов'язані structured knowledge, decisions, questions/conflicts;
3. визначити конкретні CALL-ID, у яких тема реально обговорювалась;
4. прочитати лише релевантні canonical transcripts;
5. зібрати й видати підтверджену інформацію з різних джерел.

**Index — це карта пошуку, а не сховище всього knowledge.**

## Основна модель

`canonical transcript → structured knowledge → topic registry → targeted retrieval`

- Transcript є першоджерелом.
- Knowledge files містять структуроване знання.
- Topic Index відповідає на питання «де шукати?».
- AI не повинен перечитувати весь repository, якщо Index дозволяє звузити набір джерел.

## Canonical transcript rule

Сирий ASR-текст НІКОЛИ не зберігається в GitHub.

Кожна нова транскрипція проходить повний correction pass до вилучення knowledge:
- HIGH-confidence ASR-помилки виправляються.
- MEDIUM-confidence місця позначаються `NEEDS_REVIEW`.
- LOW-confidence місця не вгадуються.
- У repository зберігається тільки corrected canonical transcript.

`01_RAW_TRANSCRIPTS/` — legacy/compatibility назва. Вона не означає, що там дозволено зберігати raw ASR.

## Processing flow

1. Отримати transcript як input.
2. Перевірити repository structure, system instructions та indexes.
3. Повністю перевірити й виправити transcription.
4. Зберегти тільки canonical transcript у `01_RAW_TRANSCRIPTS/YYYY/MM/`.
5. Витягнути knowledge categories.
6. Знайти existing knowledge та повторно використати IDs.
7. Оновити або створити Topic Index entries.
8. Для кожної теми оновити список релевантних CALL-ID.
9. Додати source traceability.
10. Оновити knowledge files, indexes та `CHANGELOG.md`.
11. Перечитати змінені файли й перевірити consistency.
12. Завершити Processing Report та Completion Gate.

## Topic Index rules

`00_INDEX/TOPIC_INDEX.md` — головна картотека тем.

Нова згадка не автоматично створює нову тему. Topic додається лише коли вона має інформаційну цінність: правило, вимогу, рішення, концепцію, компонент, workflow, важливе припущення, питання, conflict або інший предмет, який потенційно потрібно буде відновити.

Для кожної теми Index зберігає мінімальний маршрут:
- stable Topic ID;
- назву;
- пов'язані теми;
- relevant CALL-ID;
- structured knowledge IDs;
- decision/question/conflict IDs, якщо вони є;
- поточний status.

Новий CALL:
- якщо тема вже існує — додається нове джерело;
- якщо тема справді нова — створюється новий Topic ID;
- нові папки для кожної теми не створюються;
- дублікати тем не створюються лише через інше формулювання.

## Repository structure

- `00_INDEX/` — картотека та навігація.
- `01_RAW_TRANSCRIPTS/` — тільки canonical corrected transcripts.
- `02_KNOWLEDGE/` — структуроване knowledge.
- `03_DECISIONS/` — decision records.
- `04_OPEN_QUESTIONS/` — unresolved questions.
- `05_CONFLICTS/` — explicit conflicts.
- `99_SYSTEM/` — операційні правила Knowledge Manager.
- `CHANGELOG.md` — історія змін.

`INBOX/` не є частиною processing model і не використовується.

## Core rules

- Не вигадувати невизначені формулювання.
- Не перетворювати proposals на decisions.
- Не перетворювати assumptions на requirements.
- Не приховувати conflicts.
- Не дублювати knowledge items або topics.
- Кожен extracted fact має source reference.
- `PROCESSED` дозволений лише після проходження всіх mandatory checks.

Повна методологія: `99_SYSTEM/METHODOLOGY.md`.
Операційні інструкції: `99_SYSTEM/AGENT_INSTRUCTIONS.md`.