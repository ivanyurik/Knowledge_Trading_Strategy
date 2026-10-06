# Changelog

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

### Knowledge retrieval architecture
- Established 00_INDEX/MASTER_INDEX.md as the library entry point.
- Established 00_INDEX/TOPIC_INDEX.md as the canonical living topic registry.
- Defined the retrieval route: question → topic → relevant knowledge → relevant CALLs → targeted transcript reading.
- Topic entries now route to materially relevant CALL-ID sources and related KB/DEC/OQ/CON artifacts.
- New topics do not create topic-specific folders or files.
- Existing topics are extended instead of duplicated when later CALLs discuss the same subject.
- Added 00_INDEX/CONFLICTS_INDEX.md.
- Added topic-registry QA checks to the processing completion gate.
