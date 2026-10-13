# KB-BL-003 — Guaranteed Divergence Classification and Global Target Data

Status: NEEDS_REVIEW

## Scope

This item records the discussion of guaranteed/non-guaranteed divergence classification, ATR-distance criteria, Global Target data selection, and reported sample statistics. It does not promote unresolved statements into final trading rules.

## Global Target data selection

- The participants identify a potential data-consistency problem: some calculations appear to use the previous candle/switch's Global Target rather than the Global Target associated with the candle on which the divergence appeared.
- An explicit work instruction is discussed to recalculate the complete set of tables consistently using the Global Target from the divergence-event candle, not from the previous switch/candle.
- The discussion also notes that the current Global Target value may reflect the value at export time, while the exact value at the moment Classic Pending was touched may not have been saved. This makes the historical measurement point a material open question.

[NEEDS_REVIEW: verify the actual source columns and recalculated tables before treating this as a validated dataset rule.]

## Guaranteed-divergence filter

- The conversation compares distances involving candle open, Classic Pending, a divergence point, Global Target and ATR.
- Two incompatible formulations are spoken in the same discussion: one says the open-to-Classic-Pending distance should be 0.5 ATR and Global Target more than 1 ATR; a correction then reverses which distance should exceed 1 ATR and which should be below 0.5 ATR.
- Participants question why some events that appear guaranteed to them were classified as non-guaranteed by the filter.
- The conversation also raises the possibility that the indicator has differently behaving green sources/shades, which could affect classification. The exact technical term for the source is ASR-uncertain.

No single final ATR inequality or implementation rule is confirmed by this CALL.

## Reported statistics and support

- The participants mention an overall 96% result and 4 divergences out of 108 that did not appear, alongside additional percentages by timeframe/category.
- These values are spoken while reviewing a summary file, but the source table is not attached to this CALL and some category-to-percentage mapping is ASR-uncertain. Treat them as reported figures, not independently validated metrics.
- The discussion compares cases with and without support and whether a divergence appeared or a break-even exit was possible. The counts and labels are not sufficiently clear to establish a rule.

## Required follow-up

- Verify the event-candle Global Target field against the actual source data.
- Recalculate all comparison tables from a consistent source definition.
- Resolve the ATR threshold inequality from an authoritative strategy artifact.
- Reconcile the classifier output with manually reviewed examples.
- Validate reported percentages against the underlying table.

Source: CALL-2026-10-04-001, turns 011–036, 046–049, 076–087, 094–096.
