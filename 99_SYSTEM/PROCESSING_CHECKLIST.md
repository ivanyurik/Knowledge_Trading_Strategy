# PROCESSING CHECKLIST

Цей файл є обов'язковим completion gate для кожного обробленого transcript.

## Правило

CALL не можна вважати повністю обробленим, якщо будь-який обов'язковий пункт нижче не перевірений.

Якщо пункт неможливо виконати через відсутність даних або доступу, статус обробки має бути `NEEDS_REVIEW` або `BLOCKED`, а причина повинна бути вказана у Processing Report.

## Mandatory processing sequence

1. [ ] Repository structure inspected
2. [ ] `99_SYSTEM/` instructions inspected
3. [ ] Relevant indexes inspected
4. [ ] Input transcript validated
5. [ ] Original transcript preserved exactly
6. [ ] Canonical raw transcript created in `01_RAW_TRANSCRIPTS/YYYY/MM/`
7. [ ] Transcription hallucinations/errors reviewed
8. [ ] HIGH-confidence corrections recorded
9. [ ] MEDIUM-confidence corrections flagged for review
10. [ ] LOW-confidence uncertain text preserved without correction
11. [ ] Requirements checked
12. [ ] Decisions checked
13. [ ] Business rules checked
14. [ ] Architecture checked
15. [ ] Workflows checked
16. [ ] Data checked
17. [ ] Integrations checked
18. [ ] Assumptions checked
19. [ ] Risks checked
20. [ ] Open questions checked
21. [ ] Conflicts checked
22. [ ] Existing knowledge searched for duplicates
23. [ ] Existing IDs reused where applicable
24. [ ] New IDs created only for genuinely new knowledge
25. [ ] Source references added to extracted knowledge
26. [ ] Relevant indexes updated
27. [ ] `CHANGELOG.md` updated
28. [ ] Changed files re-read and verified
29. [ ] References and IDs checked for consistency
30. [ ] Processing Report created
31. [ ] Completion Gate passed

## Transcription gate

**The transcription review must happen before the processed transcript is treated as final knowledge input.**

The agent must:

- inspect the supplied transcript for hallucinations, mangled technical terms, names, numbers, product names and contextually impossible phrases;
- correct only HIGH-confidence errors automatically;
- preserve MEDIUM-confidence cases and explicitly flag them;
- never invent a correction when the intended wording is uncertain;
- preserve the original supplied transcript unchanged;
- keep the corrected representation separate from the immutable source.

A transcript is not considered transcription-reviewed until this check is explicitly recorded.

## Empty category rule

If a category contains no applicable information, mark it as checked and record `NONE FOUND`.

Do not silently skip a category.

## Completion rule

The final status may be:

- `PROCESSED` — all mandatory checks passed;
- `NEEDS_REVIEW` — processing completed but one or more review items remain;
- `BLOCKED` — a required processing step could not be completed.

Never report `PROCESSED` when a mandatory check was skipped.

## Verification

Before final response, compare the Processing Report against this checklist. The report must reflect the actual state of every mandatory stage.
