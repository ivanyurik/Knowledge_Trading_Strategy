# Changelog

## 2026-10-13

### Batch processing — eight transcript sources
- Added `99_SYSTEM/PROCESSING_REPORTS/BATCH-2026-10-13.md` with the source inventory, 765-turn reconciliation, repository integrity checks and unresolved semantic review items.
- Verified that the combined transcript duplicates the eight separate source files; it was not treated as an additional CALL.
- Confirmed that all eight new CALLs remain NEEDS_REVIEW; no unresolved strategy rule was promoted to a confirmed decision.

## 2026-10-08

### CALL-2026-10-08-001 — spot BTC clarification attempt
- Added corrected canonical transcript with 96 numbered turns; the discussion ends by requesting a more explicit final text, so the rule remains NEEDS_REVIEW.
- Extended `KB-BL-005` with the bottom-confirmation/57,600 gate, long-entry and take-profit triggers, 50% cap and peak-miss exit discussion.
- Added `OQ-2026-10-08-001` and `CON-2026-10-08-001`; linked the source through spot-BTC, divergence and final-diagram topics.
- GitHub permission discussion was recorded as an open question; actual collaborator permissions were not inferred from the transcript.

## 2026-10-07

### CALL-2026-10-07-001 processing
- Added corrected canonical transcript: `01_RAW_TRANSCRIPTS/2026/10/CALL-2026-10-07-001.md`.
- Added `KB-BL-002` covering divergence lifecycle, invalidation and multi-timeframe entry preparation.
- Added `KB-WF-001` covering the three-class divergence alert workflow.
- Added `OQ-2026-10-07-001` for unresolved ATR/stop, divergence-point, alert and multi-timeframe questions.
- Added `CON-2026-10-07-001` for ambiguities around ATR stop formulation, weekly trend scope and alert formalization.
- Updated Topic Index and retrieval indexes. Status remains NEEDS_REVIEW because unresolved/medium-confidence items remain.

### CALL-2026-10-07-002 — spot BTC rule and diagram integration
- Added corrected canonical transcript with 107 numbered turns; threshold and state-rule ambiguity remains marked NEEDS_REVIEW.
- Added `KB-BL-005`, `OQ-2026-10-07-002` and `CON-2026-10-07-002` for spot-BTC accumulation, the 57,600 threshold, sell conditions and short eligibility.
- Extended `KB-WF-002` with a constrained human-facing diagram integration workflow; added `TOPIC-SPOT-BTC-001` and updated final-diagram routing.
- No final purchase threshold or short rule was selected because the source contains unresolved contradictions.

### CALL-2026-10-07-003 — range and stop review
- Added corrected canonical transcript with 174 numbered turns; uncertain range, stop and weekly-divergence passages remain marked NEEDS_REVIEW.
- Extended `KB-BL-001`, `KB-BL-003`, `KB-BL-004` and `KB-BL-005` with source-bound notes on weekly-divergence handling, ATR alignment, range boundaries and spot-BTC accumulation.
- Added `OQ-2026-10-07-003` and `CON-2026-10-07-003` for unresolved range/phase semantics, “ignore” behavior and stop-method evidence.
- One discrepant stop event was not treated as statistical evidence; no new trading decision was promoted.

### CALL-2026-10-07-001 repository reconciliation
- Reconciled the existing CALL index/knowledge references with the canonical transcript at `01_RAW_TRANSCRIPTS/2026/10/CALL-2026-10-07-001.md`.
- Confirmed existing KB/OQ/CON/topic-routing artifacts are reused; no duplicate knowledge IDs or topic artifacts were created.
- Final processing state remains NEEDS_REVIEW because documented review items remain unresolved.

### Hard source-boundary rule
- Added a mandatory fail-closed rule forbidding external web/internet search for project facts, retrieval, processing and validation.
- Canonical source remains exclusively `ivanyurik/Knowledge_Trading_Strategy`.
- External sources are allowed only when the user explicitly requests external research for a specific task and must remain separated from repository-confirmed facts.
- Missing repository evidence must not be filled from web, memory, inference or other external sources.

### Canonical transcript storage format hard lock
- Added a mandatory turn-level transcript format to `99_SYSTEM/AGENT_INSTRUCTIONS.md`.
- Canonical transcripts must use `## Transcript` and sequential records `001 — Спікер N: ...` in chronological order.
- Speaker-grouped transcript sections are not an acceptable canonical storage format.
- If reliable original turn boundaries are unavailable, the transcript remains NEEDS_REVIEW; turn boundaries must never be invented.

## 2026-10-06

### Project Knowledge Manager synchronization
- Replaced the legacy raw-transcript repository model with the corrected-canonical-transcript model.
- Raw ASR is explicitly forbidden from repository storage.
- Updated README, system instructions, methodology, checklist, file format and change policy.
- Updated transcript, index and navigation documentation.
- Added system and structured-knowledge entry-point READMEs.
- Clarified that `01_RAW_TRANSCRIPTS` is a legacy/compatibility directory name containing canonical corrected transcripts only.
- Removed repository-level processing reliance on INBOX.
- `CALL-2026-10-06-001` remains NEEDS_REVIEW because strategy-rule review items remain.

### Plugin synchronization
- Updated Project Knowledge Manager to version 0.7.1 with the same topic-registry and targeted-retrieval rules defined by this repository.

### Knowledge retrieval architecture
- Established `00_INDEX/MASTER_INDEX.md` as the library entry point.
- Established `00_INDEX/TOPIC_INDEX.md` as the canonical living topic registry.
- Defined the retrieval route: question → topic → relevant knowledge → relevant CALLs → targeted transcript reading.
- Topic entries route to materially relevant CALL-ID sources and related KB/DEC/OQ/CON artifacts.
- New topics do not create topic-specific folders or files.
- Existing topics are extended instead of duplicated when later CALLs discuss the same subject.
- Added `00_INDEX/CONFLICTS_INDEX.md`.
- Added topic-registry QA checks to the processing completion gate.

## 2026-10-05

### CALL-2026-10-05-001 — phase marker and short eligibility
- Added corrected canonical transcript with 120 numbered source turns; ambiguous price/state phrases remain marked NEEDS_REVIEW.
- Added `KB-BL-004`, `OQ-2026-10-05-001` and `CON-2026-10-05-001` for phase-start marker semantics and unresolved short eligibility.
- Reused PivHist/final-diagram topics and added a focused phase-marker topic; no new decision was promoted from the conflicting discussion.
- Final status remains NEEDS_REVIEW pending authoritative-diagram and chart validation.

### CALL-2026-10-05-002 — Miro diagram editing workflow
- Added corrected canonical transcript with 86 numbered source turns; uncertain board names, account/access claims and ASR-corrupted terms remain marked NEEDS_REVIEW.
- Added `KB-WF-002` and `OQ-2026-10-05-002` for safe Miro editing, exact diagram identity, plugin access and validation.
- Extended the authoritative diagram topic and added `TOPIC-MIRO-EDIT-001`; temporary account-access discussion was not promoted to a strategy rule.
- Final status remains NEEDS_REVIEW pending diagram/access validation.

### CALL-2026-10-05-003 — diagram readability and future visualization
- Added corrected canonical transcript with 16 numbered source turns and explicit review markers for incomplete visual context.
- Extended `KB-WF-002` with short-arrow-label guidance, full-table comparison and the distinction between current reference diagrams and a proposed future website.
- Added `OQ-2026-10-05-003` and extended `TOPIC-MIRO-EDIT-001`; no implementation status or final architecture decision was inferred.
- Final status remains NEEDS_REVIEW pending confirmation of the future website's role and UI conventions.

## 2026-10-04

### CALL-2026-10-04-001 — guaranteed-divergence and Global Target review
- Added corrected canonical transcript in sequential turn-level format (96 source turns); unresolved ASR passages remain explicitly marked NEEDS_REVIEW.
- Added `KB-BL-003` for guaranteed-divergence classification and Global Target data semantics.
- Added `OQ-2026-10-04-001` and `CON-2026-10-04-001` for unresolved ATR thresholds, Global Target measurement point, classifier mismatch and summary-data validation.
- Extended the existing divergence topic and added `TOPIC-GUAR-001`; no decision was created because the ATR criteria conflict in the source.
- Final processing status remains NEEDS_REVIEW; reported percentages were not treated as independently verified metrics.

### CALL-2026-10-04-002 — nested divergence pairing and post-close break-even review
- Added corrected canonical transcript with all 70 source turns in chronological, numbered format; uncertain terminology remains marked NEEDS_REVIEW.
- Extended `KB-BL-002` with the one-to-one nested divergence pairing constraint, unsuccessful-touch semantics and post-close break-even review.
- Added `OQ-2026-10-04-002`; reused existing divergence and multi-timeframe topics rather than creating duplicate topics or a new decision.
- Final processing status remains NEEDS_REVIEW pending confirmation of exact filters, support definitions and source-table measurements.
