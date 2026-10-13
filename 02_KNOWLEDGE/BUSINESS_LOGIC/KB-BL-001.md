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
## Weekly bearish-divergence “ignore” semantics — later source

The discussion describes an existing rule under which a weekly bearish divergence in the first half of a trend is ignored when the global indicator does not provide the specified support. The participants say they followed the written rule but question whether “ignore” means only “do not enter a short” or means fully ignoring the signal while continuing to hold/enter an impulse trade against it.

The call also discusses whether an earlier bearish weekly divergence should have caused the current impulse trade to be closed, but does not establish a new, conflict-free exit rule.

[NEEDS_REVIEW: the exact support condition, first-half boundary, and operational meaning of “ignore” must be checked against the authoritative final diagram. Do not generalize the call's live-position discussion into trade advice.]
Source: CALL-2026-10-06-001, lines 5-11, 74-82, 88-111, 121-130, 141.; CALL-2026-10-07-003
