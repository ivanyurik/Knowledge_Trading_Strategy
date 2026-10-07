# Changelog

## 2026-10-07

### CALL-2026-10-07-001 repository reconciliation
- Reconciled the existing CALL index/knowledge references with the restored canonical transcript at `01_RAW_TRANSCRIPTS/2026/10/CALL-2026-10-07-001.md`.
- Confirmed existing KB/OQ/CON/topic-routing artifacts are reused; no duplicate knowledge IDs or topic artifacts were created.
- Confirmed final processing state remains `NEEDS_REVIEW` because the documented review items remain unresolved.

## 2026-10-07

### Hard source-boundary rule
- Added a mandatory fail-closed rule forbidding external web/internet search for project facts, retrieval, processing and validation.
- Canonical source remains exclusively `ivanyurik/Knowledge_Trading_Strategy`.
- External sources are allowed only when the user explicitly requests external research for a specific task and must remain clearly separated from repository-confirmed facts.
- Missing repository evidence must not be filled from web, memory, inference or other external sources.

## 2026-10-07

### CALL-2026-10-07-001 processing
- Added corrected canonical transcript: `01_RAW_TRANSCRIPTS/2026/10/CALL-2026-10-07-001.md`.
- Added `KB-BL-002` covering divergence lifecycle, invalidation and multi-timeframe entry preparation.
- Added `KB-WF-001` covering the three-class divergence alert workflow.
- Added `OQ-2026-10-07-001` for unresolved ATR/stop, divergence-point, alert and multi-timeframe questions.
- Added `CON-2026-10-07-001` for explicit ambiguities around ATR stop formulation, weekly trend scope and alert formalization.
- Updated Topic Index and retrieval indexes.
- Processing status remains NEEDS_REVIEW because unresolved/medium-confidence items remain.

## 2026-10-06

### Project Knowledge Manager synchronization
- Replaced the legacy raw-transcript repository model with the current corrected-canonical-transcript model.
- Raw ASR is explicitly forbidden from repository storage.
- Updated README, system instructions, methodology, checklist, file format and change policy.
- Updated transcript, index and navigation documentation.
- Added system and structured-knowledge entry-point READMEs.
- Clarified that 01_RAW_TRANSCRIPTS is a legacy/compatibility directory name containing canonical corrected transcripts only.
- Removed repository-level processing reliance on INBOX.
- CALL-2026-10-06-001 remains NEEDS_REVIEW because strategy-rule review items remain.

### Plugin synchronization
- Updated Project Knowledge Manager to version 0.7.1 with the same topic-registry and targeted-retrieval rules defined by this repository.

### Knowledge retrieval architecture
- Established 00_INDEX/MASTER_INDEX.md as the library entry point.
- Established 00_INDEX/TOPIC_INDEX.md as the canonical living topic registry.
- Defined the retrieval route: question → topic → relevant knowledge → relevant CALLs → targeted transcript reading.
- Topic entries now route to materially relevant CALL-ID sources and related KB/DEC/OQ/CON artifacts.
- New topics do not create topic-specific folders or files.
- Existing topics are extended instead of duplicated when later CALLs discuss the same subject.
- Added 00_INDEX/CONFLICTS_INDEX.md.
- Added topic-registry QA checks to the processing completion gate.
