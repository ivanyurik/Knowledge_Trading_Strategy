# Change Policy

## Allowed

- Add supplied transcripts as processing inputs.
- Add corrected canonical transcripts.
- Add new knowledge items.
- Extend existing knowledge when new source evidence supports it.
- Update Topic Index entries and source references.
- Create a new topic only when genuinely new retrieval scope exists.
- Mark knowledge `SUPERSEDED` when explicitly supported.
- Add corrections, conflicts and review items.
- Update Processing Reports and changelog.

## Canonical transcript rule

Supplied ASR is input, not a repository source layer.

Only the corrected canonical transcript may be written to `01_RAW_TRANSCRIPTS/YYYY/MM/`.

Raw ASR, raw backups and raw audit copies are forbidden.

## Topic change rules

A new CALL does not automatically create a new topic.

Before creating a topic:
1. Check existing Topic IDs.
2. Check aliases and related topics.
3. Decide whether the discussion is materially about the concept.
4. Reuse an existing topic when equivalent.
5. Create a new Topic ID only for genuinely new scope.

Adding a new source to an existing topic is normal index maintenance.

Do not create topic-specific folders or files merely to organize the topic.

## Restricted

Changes to established requirements, decisions, architecture or business logic require explicit source evidence.

Medium/low-confidence interpretation remains `NEEDS_REVIEW` until resolved.

## Historical knowledge

Do not silently erase history.

When newer evidence explicitly supersedes an older item, keep the old item, mark it `SUPERSEDED` and link the newer source.

Unresolved conflicts remain explicit.

## Never

- store raw ASR;
- create raw transcript backups;
- silently overwrite historical knowledge;
- turn proposals into decisions;
- turn assumptions into requirements;
- invent uncertain wording;
- hide conflicts;
- create folders merely because a new topic appeared.

## Git

One logical processing commit per CALL is preferred.

Recommended message: `knowledge: process CALL-YYYY-MM-DD-NNN`