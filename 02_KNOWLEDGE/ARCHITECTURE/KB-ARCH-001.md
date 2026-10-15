# KB-ARCH-001 — Modular Knowledge Architecture

Status: CONFIRMED for documentation approach; implementation details remain subject to review.

## Purpose
The project knowledge base should avoid a single giant document. It should use a navigable modular structure.

## Structure
- Global overview / system purpose.
- Global modules.
- Module relationship map.
- Individual module cards.
- Module inputs.
- Module outputs.
- Dependencies and impacts.
- Nested submodules.
- Navigation/index files that point the agent to the relevant module.

## Agent behavior
When new information arrives, the agent should:
1. Identify the relevant existing module.
2. Extend that module if the information belongs there.
3. Create a new module only when the information represents genuinely new scope.
4. Maintain links between modules.
5. Load only the context required for the current task rather than the whole repository.

## Validation
An auditor should periodically traverse modules and relationships, looking for omissions and contradictions.

Source: CALL-2026-10-06-001, lines 13, 33, 55-61, 136-140.


## Phase indicator and trading orchestrator — source extension

The speaker describes a proposed division of responsibilities:
- A phase indicator calculates market phases and exports phase plots to a table.
- The trading orchestrator consumes the exported table data and applies trade rules; it should not independently recalculate phases.
- Four slot-based divergence sheets are described for weekly, daily, 720 and 240 timeframes. A separate 4H phase sheet is described as containing phase state and the latest impulse divergence without historical slots.
- The speaker says the phase indicator's on-chart phase placements are currently incorrect, while expecting the exported data structure to remain stable as placements are corrected.
- A universal exporter is said to export divergence plots, phase plots and other integrated indicators to their corresponding destinations.

This is a source-bound design description, not proof that every component is implemented or validated. Exact sheet/indicator names and detailed trading rules remain open.

Source: CALL-2026-10-15-001
