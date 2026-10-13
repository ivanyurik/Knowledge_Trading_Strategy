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

Source: CALL-2026-10-07-002, turns 021–034, 048–055, 061–080; related historical source: CALL-2026-10-05-001.
