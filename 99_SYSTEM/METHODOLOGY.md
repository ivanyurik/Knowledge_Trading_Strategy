# Knowledge Base Methodology

## 1. Purpose

This repository is the long-term memory of the project. It stores meeting transcripts as primary evidence and maintains a structured, searchable knowledge layer above them.

## 2. Source hierarchy

1. Explicit final decision
2. Explicit confirmed requirement
3. Explicit business rule
4. Explicit statement from discussion
5. Assumption
6. Proposal
7. Agent inference

Inference must never silently become project truth.

## 3. Layers

### Layer 1 — RAW SOURCE
Original transcript exactly as received. Never rewrite, summarize over, or delete it.

### Layer 2 — CLEAN SOURCE
Optional corrected transcript representation. Corrections must preserve the original wording and explain why a correction is justified.

### Layer 3 — STRUCTURED KNOWLEDGE
Requirements, decisions, business rules, architecture, workflows, assumptions, risks, questions and conflicts.

### Layer 4 — NAVIGATION
Indexes that let an agent locate relevant files without reading the whole repository.

## 4. Immutable source rule

The original transcript is evidence. It must remain recoverable exactly as supplied.

## 5. Traceability

Every structured item must contain:
- unique ID
- status
- source transcript ID
- source location when available
- date
- confidence where interpretation is involved

## 6. Conflict handling

Never resolve historical contradictions by silently overwriting the old information. Record both statements, link them, and mark the newer decision as superseding the older one only when the discussion explicitly establishes that.

## 7. Deduplication

Do not create duplicate knowledge documents for the same stable fact. Update the existing knowledge item and add the new source reference.

## 8. Historical preservation

Superseded decisions and requirements remain in history. Mark their status instead of deleting them.

## 9. Human review

Human review is required for:
- medium/low-confidence transcription corrections
- unresolved contradictions
- inferred requirements
- inferred decisions
- changes that materially alter established architecture or business logic
