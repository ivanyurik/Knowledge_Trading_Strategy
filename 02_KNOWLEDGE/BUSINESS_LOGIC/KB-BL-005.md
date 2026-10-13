# KB-BL-005 — Spot BTC Accumulation and Strategy-Diagram Integration

Status: NEEDS_REVIEW

## Goal discussed

The conversation describes a goal of maintaining approximately 50% of the trading deposit in BTC on spot while trading ordinary futures. It discusses buying spot BTC at a qualifying long-entry point and describes using profit released after an impulse-trade take-profit to buy BTC. The exact trigger label and exception logic are not sufficiently clear in this ASR source to formalize as a final rule.

The discussion also states a long-horizon intent not to sell spot BTC before the market peak, with a fallback exit if the peak is missed. The exact exit condition and how it is identified are not fully specified here.

## Price threshold conflict

The diagram discussion includes a threshold around 57,600:
- One branch is described as “if below 57,600, do not make the spot purchase”.
- A participant immediately challenges this, reasoning that a lower price could be the desired buying opportunity and that the condition may be reversed.

[NEEDS_REVIEW: the threshold, comparison operator, and meaning of the price reference must be verified against the authoritative Telegram specification and final strategy diagram. Neither branch is treated as confirmed.]

## Diagram integration scope

The desired human-facing diagram should illustrate how the new spot-BTC rule fits into the existing strategy, using only the specifically named original diagram as its basis. The goal is not to reproduce all internal implementation logic or every dependency from a continuation diagram. The participants request direct connections to the relevant original blocks, with readable labels and working links.

This is a presentation/integration goal discussed in the call; exact block IDs, branch logic, and price conditions require comparison with the referenced Telegram message and authoritative diagram.

## Related short eligibility discussion

The same conversation says short orders are not currently allowed while a virtual trade's stop condition remains active. This differs in wording/scope from the prior CALL's discussion of a short prohibition after the first impulse take-profit beyond the zero Fibonacci level.

Resolution: do not merge these statements into a single universal rule. Keep the state/phase conditions open until checked against the authoritative final diagram.
## Additional source details — purchase timing and 50% cap

The later discussion adds the following candidate rules:
- A purchase may be triggered at a qualifying long entry and also at the take-profit of an impulse long, using a trigger-limit mechanism as described by the participants.
- The rationale for buying after take-profit is that the trade has released new funds, which are then allocated to spot BTC.
- If the current spot-BTC share is already 50% or higher, the proposed flow skips the purchase.
- A candidate accumulation interval is described from the first bullish 1W divergence above the bottom until the next bearish 1W divergence. The discussion shows that the decision branch and exact interval logic were not clearly represented in the diagram.
- The stated long-horizon goal remains to hold spot BTC until the market peak, with a fallback exit if the peak is missed. The exact peak-miss signal is not formalized here.

[NEEDS_REVIEW: confirm whether these triggers apply at all long entries or only within the accumulation interval, and verify the exact trigger label, exception order, threshold and exit signal against the authoritative Telegram specification/diagram.]
## Additional clarification attempt — bottom confirmation, threshold and exceptions

The later conversation attempts to clarify the accumulation cycle but ends with a request for a more explicit final text. The candidate sequence discussed is:

- Do not buy spot BTC before the bottom has been confirmed.
- The first bullish weekly divergence above the confirmed bottom may mark the start of the accumulation interval.
- The interval may continue until the first subsequent bearish weekly divergence; participants also discuss a fallback spot exit if a weekly divergence appears lower than the previous one, as a possible sign that the market peak was missed.
- The 57,600 threshold is discussed as a condition for whether buying begins. This source leans toward “no buying below 57,600; begin only after the bottom/upswing condition is confirmed and price is above the threshold,” but the discussion remains confused and the final rule is explicitly not yet written.
- Spot BTC purchases are discussed both at qualifying long entries and at long take-profits via Trigger Limit. The rationale for take-profit purchases is that newly realized funds become available.
- The 50% spot-BTC target and the exception to skip a purchase when the spot share is already 50% or higher are repeated.

[NEEDS_REVIEW: exact ordering of bottom confirmation, threshold crossing, exception checks, long-entry purchases, take-profit purchases and spot exit is not settled. This CALL does not close the conflicts from CALL-2026-10-07-002; use the authoritative final diagram/specification.]

Source: CALL-2026-10-07-002, turns 021–034, 048–055, 061–080; related historical source: CALL-2026-10-05-001.; CALL-2026-10-07-003; CALL-2026-10-08-001
