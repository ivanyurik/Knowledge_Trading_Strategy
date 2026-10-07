# Topic Index

Це головна картотека тем Knowledge Trading Strategy.

Її призначення — не зберігати повний зміст knowledge, а давати агенту точний маршрут від теми до джерел.

## Retrieval rule

`question → topic → knowledge/decisions/questions/conflicts → CALL-ID → canonical transcript`

Спочатку шукай тут. Не перечитуй весь `01_RAW_TRANSCRIPTS/`, якщо Index уже визначає релевантні CALL.

## Topic entry specification

Кожен запис повинен містити лише необхідний навігаційний контекст:
- Topic ID
- Topic
- Aliases (optional)
- Related topics (optional)
- Occurrences / Sources
- Structured knowledge IDs (optional)
- Decision IDs (optional)
- Open Question IDs (optional)
- Conflict IDs (optional)
- Status

## Rules for creating and updating topics

1. Не кожна згадка є topic. Просте вживання слова без змістовного обговорення не створює topic entry.
2. Якщо topic уже існує, новий CALL додається до `Occurrences / Sources` лише якщо тема матеріально обговорювалась.
3. Якщо topic справді новий, створюється новий stable Topic ID.
4. Не створювати нову тему лише через синонім або інше формулювання — спочатку перевірити aliases та existing topics.
5. Не створювати окрему папку або файл лише для нової теми.
6. Якщо новий CALL розширює existing knowledge, оновлюється existing KB item, а не створюється дубль.
7. Якщо з'явився новий structured knowledge item, він додається до відповідного topic entry.
8. Якщо тема має conflict/question/decision, це відображається посиланням на відповідний ID.
9. Історію не видаляти; використовувати status/relationships.
10. Після кожного processed CALL перевіряти duplicates, orphan references та missing source links.

## Topic registry

### TOPIC-FIB-001 — Fibonacci Grid
**Aliases:** Fibonacci, Fibonacci grid, Fib grid

**Related topics:** Divergence, PivHist, Market Structure

**Occurrences / Sources:**
- `CALL-2026-10-06-001`

**Structured knowledge:**
- `KB-BL-001`

**Decisions:**
- `DEC-2026-10-06-001`

**Open Questions:** None currently indexed

**Conflicts:** None currently indexed

**Status:** ACTIVE / NEEDS_REVIEW

---

### TOPIC-PIVHIST-001 — PivHist
**Aliases:** PivHist, PivHist Monitor

**Related topics:** Fibonacci Grid, State Machine, Market Phase

**Occurrences / Sources:**
- `CALL-2026-10-06-001`

**Structured knowledge:**
- `KB-ARCH-001`
- `KB-BL-001`

**Decisions:**
- `DEC-2026-10-06-001`

**Open Questions:**
- `OQ-2026-10-06-001`

**Conflicts:**
- `CON-2026-10-06-001`

**Status:** ACTIVE / NEEDS_REVIEW

---

### TOPIC-MOD-KB-001 — Modular Knowledge Architecture
**Aliases:** modular KB, module cards, knowledge modules

**Related topics:** Topic Index, Repository Architecture

**Occurrences / Sources:**
- `CALL-2026-10-06-001`

**Structured knowledge:**
- `KB-ARCH-001`

**Decisions:**
- `DEC-2026-10-06-001`

**Open Questions:** None currently indexed

**Conflicts:** None currently indexed

**Status:** CONFIRMED

---

### TOPIC-FINAL-DIAGRAM-001 — Authoritative Final Strategy Diagram
**Aliases:** final diagram, authoritative diagram

**Related topics:** State Machine, PivHist, Strategy Business Logic

**Occurrences / Sources:**
- `CALL-2026-10-06-001`

**Structured knowledge:** None currently indexed

**Decisions:**
- `DEC-2026-10-06-001`

**Open Questions:**
- `OQ-2026-10-06-001`

**Conflicts:**
- `CON-2026-10-06-001`

**Status:** CONFIRMED as source-priority rule

## Maintenance rule

The Topic Index is a living registry. It grows by adding or updating topic entries, not by creating more folders.

A topic should be indexed only when it has enough information value to help future retrieval.

Every topic entry must remain traceable to canonical CALL-ID sources.

---

### TOPIC-DIV-001 — Divergence Lifecycle and Invalidation
**Aliases:** divergence, hidden divergence, classic divergence, divergence box

**Related topics:** PivHist, Market Phase, Alert Workflow, Multi-Timeframe Entry Preparation

**Occurrences / Sources:**
- `CALL-2026-10-07-001`

**Structured knowledge:**
- `KB-BL-002`
- `KB-WF-001`

**Decisions:** None currently indexed

**Open Questions:**
- `OQ-2026-10-07-001`

**Conflicts:**
- `CON-2026-10-07-001`

**Status:** ACTIVE / NEEDS_REVIEW

---

### TOPIC-ALERT-001 — Divergence Alert Workflow
**Aliases:** alert workflow, divergence alerts, three alert types

**Related topics:** Divergence Lifecycle and Invalidation, PivHist, Multi-Timeframe Entry Preparation

**Occurrences / Sources:**
- `CALL-2026-10-07-001`

**Structured knowledge:**
- `KB-WF-001`

**Decisions:** None currently indexed

**Open Questions:**
- `OQ-2026-10-07-001`

**Conflicts:**
- `CON-2026-10-07-001`

**Status:** ACTIVE / NEEDS_REVIEW

---

### TOPIC-MTF-001 — Multi-Timeframe Entry Preparation
**Aliases:** 12H + 4H, multi-timeframe divergence, pending divergence entry

**Related topics:** Divergence Lifecycle and Invalidation, Market Phase, Alert Workflow

**Occurrences / Sources:**
- `CALL-2026-10-07-001`

**Structured knowledge:**
- `KB-BL-002`
- `KB-WF-001`

**Decisions:** None currently indexed

**Open Questions:**
- `OQ-2026-10-07-001`

**Conflicts:**
- `CON-2026-10-07-001`

**Status:** ACTIVE / NEEDS_REVIEW
