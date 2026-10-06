# KB-BL-001 — Strategy Logic Clarifications from CALL-2026-10-06-001

Status: NEEDS_REVIEW

## Confirmed / strongly supported
- Manual placement of the Fibonacci grid must not be used for the strategy dataset; the indicator-generated grid is the intended source.
- Historical data should be exported with the indicator-generated Fibonacci grid in the relevant positions.
- The project distinguishes strategy phases including:
  - боротьба на початку;
  - імпульсний рух;
  - зупинка плюс ретест.
- 1v1 is treated in the discussion as a distinct signal.
- D1V is referenced as a table/column identifier, but its exact definition is not established by this call.
- The state-machine discussion describes long and short branches as potentially parallel, each having its own phase; a trend change affects the corresponding branch. This was explicitly said to depend on context and must be validated against the final diagram.
- The final diagram is intended to have higher priority than earlier discussion if a contradiction is found.

## Needs review
- Exact 1W rules.
- Exact 1D exception/behavior.
- Exact first-half-of-global-trend filter.
- Exact meaning of D1V.
- Exact exit trigger and candle-color rule.
- Exact meaning of the ASR-corrupted terms around the stop/transition phase.

Source: CALL-2026-10-06-001, lines 5-11, 74-82, 88-111, 121-130, 141.
