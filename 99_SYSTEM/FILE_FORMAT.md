# File Format Specification

## Canonical transcript

Format: `CALL-YYYY-MM-DD-NNN.md`
Location: `01_RAW_TRANSCRIPTS/YYYY/MM/`
The file contains the corrected canonical transcript, not raw ASR.

Recommended sections:
1. Metadata
2. Corrected Transcript
3. `NEEDS_REVIEW` markers where required
4. Processing notes when useful for traceability

Do not add raw transcript or raw-vs-canonical comparison layers.

## Topic entry

Location: `00_INDEX/TOPIC_INDEX.md`

Required fields:
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

Rules:
- Topic IDs are stable.
- An occurrence means meaningful discussion, not incidental mention.
- Existing topics must be reused.
- Topic-specific folders/files are forbidden unless a separate knowledge artifact is independently justified.
- Topic entries remain concise and navigational.

## Knowledge item

Knowledge items live in the appropriate `02_KNOWLEDGE` module.

Recommended fields: ID, Title, Description/Rule, Status, Source, Source location, Related items, Confidence when interpretation is involved.

## Decision

`DEC-YYYY-MM-DD-NNN.md`

Fields: ID, Decision, Status, Rationale, Source, Supersedes, Related items.

## Requirement

`REQ-NNN.md`

Fields: ID, Title, Description, Status, Priority, Source, Source location, Related items.

## Business Rule

`BR-NNN.md`

Fields: ID, Rule, Conditions, Result, Status, Source, Related items.

## Open Question

`OQ-YYYY-MM-DD-NNN.md`

Fields: ID, Question, Status, Context, Source, Related items.

## Conflict

`CON-YYYY-MM-DD-NNN.md`

Fields: ID, Statement A, Source A, Statement B, Source B, Status, Required resolution.

## Processing Report

Location: `99_SYSTEM/PROCESSING_REPORTS/CALL-YYYY-MM-DD-NNN.md`

Records input validation, correction gate, category results, topic changes, knowledge updates, conflicts, review items and completion status.