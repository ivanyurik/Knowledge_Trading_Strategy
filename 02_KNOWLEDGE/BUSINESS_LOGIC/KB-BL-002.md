# KB-BL-002 — Divergence Lifecycle, Invalidation and Multi-Timeframe Entry Preparation

Status: NEEDS_REVIEW

## Scope

This knowledge item captures the divergence-specific trading logic discussed in CALL-2026-10-07-001. It extends the broader strategy logic in KB-BL-001 without replacing earlier historical knowledge.

## Divergence lifecycle

- A divergence is treated as active only after the relevant indicator bar/pivot is confirmed by candle close.
- The active period starts from the next candle after the confirming candle.
- A divergence remains active until the corresponding invalidation line is crossed according to the discussed rules.
- A box is used to visualize the active interval from its start to its invalidation/end point.
- A price touching or entering the visual box is not itself the invalidation event; the relevant invalidation is the crossing of the corresponding dotted line.
- The box is stopped when the divergence is invalidated.
- Multiple divergences may coexist and are represented independently.

## Pivot correspondence

- Indicator pivots must be matched to the corresponding price-chart pivots.
- A histogram/dotted-line crossing does not automatically mean that a new divergence exists.
- An alert caused by a crossing is a review trigger: the corresponding price pivot must be checked before classifying the event.

## Weekly trend / phase interaction

The discussion states that appearance of a weekly divergence changes the active trend direction and that the beginning-of-struggle phase then uses that direction for trade selection.

[NEEDS_REVIEW: exact formal phase rules and the authoritative weekly/1D rules are not fully established in this CALL and must be checked against the final strategy diagram.]

## Entry preparation

The operational principle is to prepare the trade before the divergence becomes visually obvious, because the reaction may occur immediately after the invalidation-line crossing.

For a short setup discussed in the call:
- the relevant higher-timeframe bearish divergence defines the directional setup;
- the stop is discussed using the last confirmed 1D ATR value;
- a future daily bearish-divergence point may be used to place a limit order in advance;
- as price and the nearest future divergence point move, the pending order is updated.

[NEEDS_REVIEW: exact stop formula, position sizing formula, and whether the mentioned 20% ATR reduction is a general rule are not confirmed.]

## 12H + 4H linkage

- The 12H + 4H setup requires bearish divergence to be active on both timeframes at the moment of entry.
- It does not require a fixed order in which the two divergences appear.
- The two timeframes are otherwise treated as independent.
- A lower-timeframe divergence that appeared first may remain the active condition while the other timeframe later reaches its corresponding divergence point.

## Nested divergence pairing — source extension

The later-reviewed conversation describes a one-to-one pairing constraint for nested divergences:

- Only the nearest qualifying internal divergence is paired with one external divergence; the pair consists of two divergences.
- A single 4H external divergence cannot be reused to pair with three successive 12H internal divergences.
- Once a 12H divergence is paired inside a 4H divergence, that 4H divergence is no longer eligible as the external divergence for a later 12H divergence. A new external divergence is required for the next pair.
- The same one-to-one constraint is described in the reverse direction for 4H divergences nested inside 12H divergences.
- A touch of Classic Pending that does not produce a divergence at the relevant candle close is described as an unsuccessful touch; it consumes neither the external nor internal divergence slot.

[NEEDS_REVIEW: verify the exact price/time filters for qualifying nested divergences and the event definition used by the data tables.]

## Post-close break-even review

The conversation asks to evaluate the first candle after the divergence-confirming candle close (and, in the 1D case, specifically after the 1D candle closes) that returns to the divergence appearance price. A return within the same unfinished/previous period is not considered equivalent to a return after the required candle close.

The transcript also discusses a potential handling distinction for non-guaranteed cases depending on whether support exists. This is stated as a proposed workflow pending final data/statistics and is not promoted to a confirmed trading rule.

Source: CALL-2026-10-07-001; CALL-2026-10-04-002
