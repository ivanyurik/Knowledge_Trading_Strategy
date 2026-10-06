# Project Knowledge Manager Methodology

## 1. Purpose

This repository is a long-term, traceable knowledge base designed for future retrieval, not passive transcript storage.

The core model is:

`transcript input → correction gate → canonical transcript → structured knowledge → topic registry → targeted retrieval`

The final user-facing goal is:

`question → topic → relevant sources → targeted reading → evidence-based answer`

## 2. Three-layer architecture

Keep the repository intentionally small and stable.

### Layer 1 — Navigation
`00_INDEX/`

This is the library catalog:
- `MASTER_INDEX.md` — entry point and system map.
- `TOPIC_INDEX.md` — topic registry and source routing.
- Other indexes — decisions, requirements, open questions, conflicts.

### Layer 2 — Structured knowledge
`02_KNOWLEDGE/` plus `03_DECISIONS/`, `04_OPEN_QUESTIONS/`, `05_CONFLICTS/`

These files contain normalized knowledge and unresolved project state.

### Layer 3 — Primary sources
`01_RAW_TRANSCRIPTS/`

Despite its legacy name, this contains only corrected canonical transcripts. Raw ASR is never stored.

Do not add more repository layers merely to represent individual topics.

## 3. Canonical transcript model

A supplied transcript is an input artifact.

It must first pass the transcription correction gate.

Only the corrected result is stored in GitHub as:

`01_RAW_TRANSCRIPTS/YYYY/MM/CALL-YYYY-MM-DD-NNN.md`

There is no repository layer for raw source, raw backup, immutable raw transcript, or RAW/CLEAN pairs.

## 4. Transcription correction

- HIGH confidence: automatically correct clear ASR hallucinations, technical terms, names, numbers and abbreviations.
- MEDIUM confidence: do not invent wording; mark `NEEDS_REVIEW`.
- LOW confidence: do not guess.
- Correction happens before knowledge extraction.

If correction cannot be completed, do not report `PROCESSED`.

## 5. Structured knowledge

Required categories:
- Requirements
- Decisions
- Business Rules
- Architecture
- Workflows
- Data
- Integrations
- UI/UX
- Assumptions
- Risks
- Open Questions
- Conflicts
- Proposals

Every extracted fact must point to a canonical CALL-ID.

Reuse existing IDs when the knowledge is an extension of an existing item. Create a new ID only for genuinely new knowledge.

## 6. Topic registry

`00_INDEX/TOPIC_INDEX.md` is the canonical topic registry.

A topic is a retrieval concept, not a keyword occurrence.

Create or update a topic when the transcript contains information that may need to be found again: a rule, requirement, decision, concept, architecture component, workflow, important assumption, risk, question, conflict, or other meaningful subject.

Do not create topics for incidental mentions.

### Topic creation algorithm

For every meaningful candidate topic:
1. Normalize the topic name.
2. Check existing Topic IDs and aliases.
3. If an equivalent topic exists, update that entry.
4. Add the current CALL-ID to its source list if the CALL materially discusses the topic.
5. Add/update related knowledge IDs.
6. Add related decision/question/conflict IDs.
7. If no equivalent topic exists, create a new stable Topic ID.
8. Recheck duplicates and orphan references.

### Important distinction

Topic ≠ Knowledge ≠ Source.

Example:
- Topic: `Fibonacci Grid`
- Knowledge: `KB-BL-001`
- Decision: `DEC-2026-10-06-001`
- Source: `CALL-2026-10-06-001`

The topic points to the other artifacts. It does not duplicate their full content.

## 7. Targeted retrieval

When answering a later question:
1. Start with `MASTER_INDEX.md`.
2. Resolve the user's concept to one or more Topic IDs using `TOPIC_INDEX.md`.
3. Read linked structured knowledge first.
4. Collect the listed CALL-ID sources.
5. Read only those canonical transcripts when exact wording, historical context, or cross-call comparison is required.
6. Synthesize the answer with source traceability.
7. If the Index is incomplete or stale, expand the search only as a fallback and repair the Index afterward.

The Index is a routing layer, not an authority that replaces source evidence.

## 8. Topic maintenance

When a new CALL is processed:
- existing topics receive new source references;
- genuinely new topics receive new Topic IDs;
- topic aliases may be extended when useful;
- related topics may be linked;
- stale/orphan references are repaired;
- no topic-specific folders are created;
- no duplicate topic is created because of wording variation.

The Topic Index must be updated in the same logical processing cycle as the CALL.

## 9. Modular knowledge architecture

Use modules, relationships, module cards, inputs/outputs and dependencies where the knowledge itself warrants them.

Do not create a new module for every new topic. New modules require genuinely new scope.

## 10. Traceability and conflicts

Every extracted fact points to a canonical CALL-ID.

Conflicts remain explicit. Newer evidence may supersede older knowledge only when explicitly supported. Historical source evidence remains traceable.

If an artifact is explicitly authoritative, it has priority over earlier discussion where they conflict.

## 11. Completion statuses

- `PROCESSED` — all mandatory checks passed.
- `NEEDS_REVIEW` — processing completed but review items remain.
- `BLOCKED` — a mandatory step could not be completed.

## 12. Stable repository structure

- `00_INDEX`
- `01_RAW_TRANSCRIPTS` — canonical corrected transcripts only; legacy/compatibility name.
- `02_KNOWLEDGE`
- `03_DECISIONS`
- `04_OPEN_QUESTIONS`
- `05_CONFLICTS`
- `99_SYSTEM`

`INBOX` is not part of the processing model.