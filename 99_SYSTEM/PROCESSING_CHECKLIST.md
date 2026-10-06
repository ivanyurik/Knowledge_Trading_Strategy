# Processing Checklist

Цей файл є обов'язковим completion gate для кожного CALL.

## Mandatory sequence

1. [ ] Repository structure inspected
2. [ ] 99_SYSTEM instructions inspected
3. [ ] Relevant indexes inspected
4. [ ] Input transcript validated
5. [ ] Full transcription correction pass completed
6. [ ] Only corrected canonical transcript written to 01_RAW_TRANSCRIPTS/YYYY/MM/
7. [ ] Raw ASR input NOT stored anywhere in repository
8. [ ] HIGH-confidence hallucinations/errors corrected
9. [ ] MEDIUM-confidence cases marked NEEDS_REVIEW
10. [ ] LOW-confidence cases not guessed
11. [ ] Requirements checked
12. [ ] Decisions checked
13. [ ] Business Rules checked
14. [ ] Architecture checked
15. [ ] Workflows checked
16. [ ] Data checked
17. [ ] Integrations checked
18. [ ] UI/UX checked
19. [ ] Assumptions checked
20. [ ] Risks checked
21. [ ] Open Questions checked
22. [ ] Conflicts checked
23. [ ] Proposals checked
24. [ ] Existing knowledge searched for duplicates
25. [ ] Existing IDs reused where applicable
26. [ ] New IDs created only for genuinely new knowledge
27. [ ] Source references added
28. [ ] Relevant indexes updated
29. [ ] Root CHANGELOG.md updated
30. [ ] Changed files re-read
31. [ ] References and IDs verified
32. [ ] Processing Report completed
33. [ ] Completion Gate passed

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
- reporting PROCESSED with skipped checks.

## Status

PROCESSED — all mandatory checks passed.
NEEDS_REVIEW — processing completed but review items remain.
BLOCKED — a mandatory processing step could not be completed.