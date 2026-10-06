# Project Knowledge Manager Methodology

## 1. Purpose

This repository is the long-term, traceable knowledge base of the project.

The system is:

transcript input → correction gate → canonical transcript → structured knowledge → navigation/indexes

The repository is not a raw transcript archive.

## 2. Canonical source model

A supplied transcript is an input artifact.

It must first pass the transcription correction gate.

Only the corrected result is stored in GitHub as the canonical transcript:

01_RAW_TRANSCRIPTS/YYYY/MM/CALL-YYYY-MM-DD-NNN.md

Despite the directory name, raw ASR is never stored.

There is no repository layer for RAW SOURCE, raw transcript backup, immutable original transcript, or CLEAN SOURCE paired with a raw source.

## 3. Transcription correction policy

HIGH confidence: automatically correct clear ASR hallucinations, mangled technical terms, names, numbers, abbreviations and product/platform names.

MEDIUM confidence: do not invent wording; mark NEEDS_REVIEW.

LOW confidence: do not guess.

Correction happens before knowledge extraction.

If correction cannot be completed, status is NEEDS_REVIEW or BLOCKED, never PROCESSED.

## 4. Structured knowledge

Knowledge is separated from the transcript into navigable modules.

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

Every extracted fact points to its canonical CALL-ID.

## 5. Modular architecture

Use:
- global project/system overview;
- module index;
- module relationship map;
- individual module cards;
- inputs and outputs;
- dependencies and impacts;
- nested submodules;
- navigation indexes.

When new information arrives, first determine whether it extends an existing module. Create a new module only when genuinely new scope exists.

Do not load the entire repository when a smaller module-specific context is sufficient.

## 6. Traceability

Required source format:

Source: CALL-YYYY-MM-DD-NNN

Where practical include transcript location, evidence, related IDs and status.

Agent inference must never silently become project fact.

## 7. Conflicts and history

Conflicts remain explicit.

Do not silently rewrite history to make contradictory statements disappear.

When newer evidence explicitly supersedes an older item, mark the old item SUPERSEDED while preserving traceability.

When unresolved, keep the conflict open.

## 8. Authoritative project artifacts

If the project explicitly designates an artifact as authoritative, it has priority over earlier discussion when the two conflict.

For the current strategy work, the final strategy diagram is the higher-priority source for unresolved strategy-rule differences.

## 9. Navigation

00_INDEX exists so an agent can find the right knowledge without reading the entire repository.

Indexes must be updated whenever new knowledge or a new CALL is added.

## 10. Completion statuses

PROCESSED — all mandatory checks passed.

NEEDS_REVIEW — processing completed but review items remain.

BLOCKED — a mandatory step could not be completed.

## 11. Repository naming

00_INDEX
01_RAW_TRANSCRIPTS — canonical corrected transcripts only; legacy/compatibility name
02_KNOWLEDGE
03_DECISIONS
04_OPEN_QUESTIONS
05_CONFLICTS
99_SYSTEM

INBOX is not part of the processing model and must not be used to store transcripts.