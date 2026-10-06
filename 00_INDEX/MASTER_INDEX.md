# Master Index

## Purpose

Це головна сторінка бібліотеки Knowledge Trading Strategy.

Вона показує верхній шар системи, але не дублює весь repository. Для пошуку конкретної теми переходь у `TOPIC_INDEX.md`.

## Retrieval model

`question → topic → relevant knowledge → relevant CALLs → targeted transcript reading → answer`

AI не повинен читати всі транскрипції, якщо Topic Index дозволяє визначити релевантні джерела.

## Main navigation

- **Topic catalog:** `00_INDEX/TOPIC_INDEX.md`
- **Knowledge:** `02_KNOWLEDGE/`
- **Decisions:** `00_INDEX/DECISIONS_INDEX.md`
- **Requirements:** `00_INDEX/REQUIREMENTS_INDEX.md`
- **Open Questions:** `00_INDEX/OPEN_QUESTIONS_INDEX.md`
- **Conflicts:** `00_INDEX/CONFLICTS_INDEX.md`
- **System methodology:** `99_SYSTEM/METHODOLOGY.md`

## Repository map

- `00_INDEX/` — карта та індекси.
- `01_RAW_TRANSCRIPTS/` — canonical corrected transcripts only; legacy/compatibility name.
- `02_KNOWLEDGE/` — structured knowledge.
- `03_DECISIONS/` — decisions.
- `04_OPEN_QUESTIONS/` — unresolved questions.
- `05_CONFLICTS/` — explicit conflicts.
- `99_SYSTEM/` — methodology and operational rules.

## Knowledge areas

- Architecture → `02_KNOWLEDGE/ARCHITECTURE/`
- Business Logic → `02_KNOWLEDGE/BUSINESS_LOGIC/`
- Requirements → `02_KNOWLEDGE/REQUIREMENTS/`
- Workflows → `02_KNOWLEDGE/WORKFLOWS/`
- Data → `02_KNOWLEDGE/DATA/`
- Integrations → `02_KNOWLEDGE/INTEGRATIONS/`

## Current CALLs

### CALL-2026-10-06-001
Status: `NEEDS_REVIEW`

Canonical transcript:
`01_RAW_TRANSCRIPTS/2026/10/CALL-2026-10-06-001.md`

Related knowledge:
- `02_KNOWLEDGE/ARCHITECTURE/KB-ARCH-001.md`
- `02_KNOWLEDGE/BUSINESS_LOGIC/KB-BL-001.md`

Related decisions/questions/conflicts:
- `03_DECISIONS/DEC-2026-10-06-001.md`
- `04_OPEN_QUESTIONS/OQ-2026-10-06-001.md`
- `05_CONFLICTS/CON-2026-10-06-001.md`

Processing report:
- `99_SYSTEM/PROCESSING_REPORTS/CALL-2026-10-06-001.md`

## Agent entry point

Read `99_SYSTEM/AGENT_INSTRUCTIONS.md` before processing the repository.