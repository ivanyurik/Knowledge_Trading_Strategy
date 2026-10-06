# Processing Checklist

Цей файл є обов'язковим completion gate для кожного CALL.

## Mandatory sequence

1. [ ] Repository structure inspected
2. [ ] `99_SYSTEM` instructions inspected
3. [ ] `00_INDEX/MASTER_INDEX.md` inspected
4. [ ] `00_INDEX/TOPIC_INDEX.md` inspected
5. [ ] Input transcript validated
6. [ ] Full transcription correction pass completed
7. [ ] Only corrected canonical transcript written to `01_RAW_TRANSCRIPTS/YYYY/MM/`
8. [ ] Raw ASR input NOT stored anywhere in repository
9. [ ] HIGH-confidence hallucinations/errors corrected
10. [ ] MEDIUM-confidence cases marked `NEEDS_REVIEW`
11. [ ] LOW-confidence cases not guessed
12. [ ] Requirements checked
13. [ ] Decisions checked
14. [ ] Business Rules checked
15. [ ] Architecture checked
16. [ ] Workflows checked
17. [ ] Data checked
18. [ ] Integrations checked
19. [ ] UI/UX checked
20. [ ] Assumptions checked
21. [ ] Risks checked
22. [ ] Open Questions checked
23. [ ] Conflicts checked
24. [ ] Proposals checked
25. [ ] Existing knowledge searched for duplicates
26. [ ] Existing Topic IDs and aliases searched
27. [ ] Existing IDs reused where applicable
28. [ ] New IDs created only for genuinely new knowledge/topics
29. [ ] Topic entries created only for meaningful retrieval concepts
30. [ ] Current CALL-ID added to every materially discussed existing topic
31. [ ] Related KB/DEC/OQ/CON links updated
32. [ ] Source references added
33. [ ] Relevant indexes updated
34. [ ] Root `CHANGELOG.md` updated
35. [ ] Changed files re-read
36. [ ] References and IDs verified
37. [ ] Processing Report completed
38. [ ] Completion Gate passed

## Topic-specific QA

- [ ] No topic exists only because a keyword was mentioned incidentally.
- [ ] No duplicate topic was created because of naming variation.
- [ ] No topic-specific folder was created.
- [ ] Topic entries point to real CALL-ID sources.
- [ ] Every materially discussed topic from the CALL is represented.
- [ ] Index does not duplicate full knowledge content.

## Transcription gate

Supplied transcript is input, not canonical source.
Correction must happen before knowledge extraction.
HIGH-confidence errors are corrected; MEDIUM-confidence cases are flagged; LOW-confidence cases are not guessed.

## Forbidden

- storing raw ASR;
- creating raw/backup/audit copies;
- treating uncorrected ASR as canonical;
- silently resolving conflicts;
- inventing uncertain wording;
- reporting `PROCESSED` with skipped checks.

## Status

`PROCESSED` — all mandatory checks passed.
`NEEDS_REVIEW` — processing completed but review items remain.
`BLOCKED` — a mandatory processing step could not be completed.