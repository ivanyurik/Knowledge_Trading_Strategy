# KB-BL-004 — Phase Start Marker and Short Eligibility Discussion

Status: NEEDS_REVIEW

## Phase-start marker requirements discussed

The conversation describes a red vertical marker at the opening of the weekly candle that starts the “Остановка + Flat” phase.

The marker is described as having:
- a label equivalent to “Start остановки + Flat”;
- the start time shown;
- white text;
- synchronized placement across all timeframes;
- its position tied to the opening of the candle that starts the phase.

The speaker explicitly corrects a field interpretation: although the UI field may be named “price of divergence appearance”, for this phase marker it should represent the opening price of the candle from which the “Остановка + Flat” phase begins, not a divergence appearance price.

[NEEDS_REVIEW: confirm the exact canonical phase label and marker field names against the authoritative final strategy diagram/indicator specification.]

## Short eligibility discussion

The conversation discusses whether a short limit order should be displayed/allowed while a long setup and phase transition are active. One passage says the short should not be visible/enterable in the current situation; later, the speaker states that shorting becomes prohibited only after the first take-profit of the impulse move beyond the zero Fibonacci level, and concludes that this take-profit has not yet occurred.

This is evidence of a context-dependent rule discussion, not a fully validated global rule. Do not infer unconditional short permission or prohibition from this CALL alone.

## Indicator implementation context

- The PivHist Monitor script is being updated in a working file.
- The participants discuss extending chart lines to the right, anchoring them to the relevant wick, and duplicating a corresponding line for the short side.
- The conversation mentions implementing the guaranteed-divergence logic in the indicator, but does not provide a complete technical specification.

Source: CALL-2026-10-05-001, turns 003–014, 048–084, 087–107, 120.
