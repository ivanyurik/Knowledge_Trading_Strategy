# Master Index

## Project
Knowledge Trading Strategy

## Processing model
Project Knowledge Manager

Flow:
transcript input → transcription correction → canonical transcript → structured knowledge → indexes → processing report

Raw ASR is never stored in the repository.

## Repository map
- 00_INDEX/ — navigation and indexes
- 01_RAW_TRANSCRIPTS/ — canonical corrected transcripts only; legacy/compatibility name
- 02_KNOWLEDGE/ — structured knowledge modules
- 03_DECISIONS/ — decisions
- 04_OPEN_QUESTIONS/ — unresolved questions
- 05_CONFLICTS/ — explicit conflicts
- 99_SYSTEM/ — operational methodology and processing rules
- CHANGELOG.md — repository history

## Knowledge areas
- Architecture: 02_KNOWLEDGE/ARCHITECTURE/
- Business Logic: 02_KNOWLEDGE/BUSINESS_LOGIC/
- Requirements: 02_KNOWLEDGE/REQUIREMENTS/
- Workflows: 02_KNOWLEDGE/WORKFLOWS/
- Data: 02_KNOWLEDGE/DATA/
- Integrations: 02_KNOWLEDGE/INTEGRATIONS/

## Current CALLs

### CALL-2026-10-06-001
Status: NEEDS_REVIEW

Canonical transcript:
01_RAW_TRANSCRIPTS/2026/10/CALL-2026-10-06-001.md

Related:
- 02_KNOWLEDGE/ARCHITECTURE/KB-ARCH-001.md
- 02_KNOWLEDGE/BUSINESS_LOGIC/KB-BL-001.md
- 03_DECISIONS/DEC-2026-10-06-001.md
- 04_OPEN_QUESTIONS/OQ-2026-10-06-001.md
- 05_CONFLICTS/CON-2026-10-06-001.md
- 99_SYSTEM/PROCESSING_REPORTS/CALL-2026-10-06-001.md

## Agent entry point
Read 99_SYSTEM/AGENT_INSTRUCTIONS.md before processing the repository.
