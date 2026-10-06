# Change Policy

## Allowed

- Add new transcripts.
- Add new knowledge items.
- Update indexes.
- Add source references.
- Mark decisions or requirements as superseded when explicitly supported.
- Add corrections with evidence.
- Add conflicts.

## Restricted

Changes to established requirements, decisions, architecture or business logic require explicit source evidence.

## Never

Never delete source transcripts or silently rewrite historical knowledge.

## Git

Prefer one logical processing commit per transcript.

Suggested commit message:

`knowledge: process CALL-YYYY-MM-DD-NNN`
