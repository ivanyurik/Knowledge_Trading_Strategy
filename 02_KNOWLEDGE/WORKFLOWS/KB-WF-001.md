# KB-WF-001 — Divergence Monitoring and Alert Workflow

Status: NEEDS_REVIEW

## Purpose

Describe the manual monitoring workflow discussed in CALL-2026-10-07-001 for keeping future divergence events actionable without continuously watching the chart.

## Three alert classes

1. Indicator-line crossing alert
   - Trigger: a histogram bar crosses a relevant dotted line.
   - Action: inspect the corresponding price-chart pivot and determine whether the event represents hidden divergence or an irrelevant crossing.

2. New-pivot alert
   - Trigger: a new histogram pivot creates a new relevant dotted line.
   - Action: connect that pivot to the corresponding price-chart pivot, draw/update the dotted line, and move the future-divergence alert to the nearest relevant point.

3. Approach-to-target alert
   - Trigger: price approaches a precomputed/expected future divergence point or pending-limit area.
   - Action: re-check whether the predicted divergence is still valid before leaving the pending order in place.

## Rolling monitoring rule

The described workflow keeps attention on the nearest actionable future events. As new pivots appear, old alerts are moved to the new nearest points. As price approaches an alert, the condition is revalidated rather than assumed to remain valid indefinitely.

## Manual-first validation

The participants explicitly discuss first learning and validating the process manually in replay across four timeframes. Automation of boxes, zones and their movement is considered only after the manual sequence is understood.

[NEEDS_REVIEW: whether the three alert classes are intended as permanent system requirements or current manual operating practice.]

Source: CALL-2026-10-07-001
