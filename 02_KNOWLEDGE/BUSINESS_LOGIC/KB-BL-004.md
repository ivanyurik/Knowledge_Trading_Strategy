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
## Range boundaries and “Остановка + Flat” — later source

The conversation proposes a range-boundary rule:
- Find the highest wick within the relevant interval bounded by the “Остановка + Flat” phase start and the next relevant boundary.
- A weekly candle must close above that wick to confirm a breakout; a wick alone is explicitly said not to be sufficient.
- The speaker states that this breakout test may apply regardless of whether a trade occurred during the interval.

The participants also discuss a separate rule that a range can start from a 4H divergence on a Fibonacci grid stretched across the range's high/low. They question how to classify price movement into a new range when no qualifying 4H divergence or impulse trade occurred, and why multiple “Остановка + Flat” markers appear consecutively. These points remain unresolved.

[NEEDS_REVIEW: this proposed range-boundary rule must be checked against the authoritative final strategy diagram and historical examples.]
Source: CALL-2026-10-05-001, turns 003–014, 048–084, 087–107, 120.; CALL-2026-10-07-003
