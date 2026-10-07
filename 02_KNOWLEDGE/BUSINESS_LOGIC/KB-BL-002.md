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

Source: CALL-2026-10-07-001
