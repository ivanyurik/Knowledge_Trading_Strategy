# Knowledge Base Methodology

## 1. Призначення

Цей репозиторій є довгостроковою пам'яттю проєкту. Він зберігає транскрипти зустрічей як первинні докази та підтримує над ними структурований і придатний для пошуку knowledge layer.

## 2. Source hierarchy

1. Explicit final decision
2. Explicit confirmed requirement
3. Explicit business rule
4. Explicit statement from discussion
5. Assumption
6. Proposal
7. Agent inference

Inference ніколи не може непомітно стати фактом проєкту.

## 3. Layers

### Layer 1 — RAW SOURCE

Оригінальний транскрипт у точному вигляді, у якому його отримано. Його не можна переписувати, замінювати резюме або видаляти.

### Layer 2 — CLEAN SOURCE

Необов'язкове виправлене представлення транскрипту. Кожне виправлення має зберігати оригінальний текст і пояснювати, чому виправлення обґрунтоване.

### Layer 3 — STRUCTURED KNOWLEDGE

Requirements, decisions, business rules, architecture, workflows, assumptions, risks, questions і conflicts.

### Layer 4 — NAVIGATION

Індекси, які дозволяють agent швидко знаходити потрібні файли без читання всього репозиторію.

## 4. Immutable source rule

Оригінальний транскрипт є доказом. Він має залишатися доступним для відновлення в точному вигляді, у якому був отриманий.

## 5. Traceability

Кожен структурований елемент повинен містити:
- унікальний ID
- status
- source transcript ID
- source location, якщо доступна
- date
- confidence, якщо використовується інтерпретація

## 6. Conflict handling

Не можна вирішувати історичні суперечності шляхом непомітного перезапису старої інформації. Потрібно зберегти обидва твердження, пов'язати їх і позначити новіше рішення як таке, що замінює попереднє, лише якщо це прямо випливає з обговорення.

## 7. Deduplication

Не створюйте дублікати knowledge-документів для одного стабільного факту. Оновлюйте наявний knowledge item і додавайте нове source reference.

## 8. Historical preservation

Superseded decisions і requirements залишаються в історії. Змінюється їхній status, але вони не видаляються.

## 9. Human review

Human review обов'язковий для:
- medium/low-confidence виправлень транскрипції
- невирішених суперечностей
- inferred requirements
- inferred decisions
- змін, які суттєво впливають на встановлену architecture або business logic
