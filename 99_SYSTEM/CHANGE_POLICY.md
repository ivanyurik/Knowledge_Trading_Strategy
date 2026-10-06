# Change Policy

## Allowed

- Add supplied transcripts as processing inputs.
- Add corrected canonical transcripts.
- Add new knowledge items.
- Extend existing knowledge when new source evidence supports it.
- Update indexes and source references.
- Mark knowledge SUPERSEDED when explicitly supported.
- Add corrections, conflicts and review items.
- Update Processing Reports and changelog.

## Canonical transcript rule

Supplied ASR is input, not a repository source layer.
Only the corrected canonical transcript may be written to 01_RAW_TRANSCRIPTS/YYYY/MM/.
Raw ASR, raw backups and raw audit copies are forbidden.

## Restricted

Changes to established requirements, decisions, architecture or business logic require explicit source evidence.
Medium/low-confidence interpretation remains NEEDS_REVIEW until resolved.

## Historical knowledge

Do not silently erase history.
When newer evidence explicitly supersedes an older item, keep the old item, mark it SUPERSEDED and link the newer source.
Unresolved conflicts remain explicit.

## Never

- store raw ASR;
- create raw transcript backups;
- silently overwrite historical knowledge;
- turn proposals into decisions;
- turn assumptions into requirements;
- invent uncertain wording;
- hide conflicts.

## Git

One logical processing commit per CALL is preferred.
Recommended message: knowledge: process CALL-YYYY-MM-DD-NNN