# KB-WF-002 — Safe Miro Diagram Editing Workflow

Status: NEEDS_REVIEW

## Preconditions

Before asking an AI/plugin to edit a strategy diagram:

1. Use the exact Miro board and diagram names copied from the interface; do not rely on ASR-derived names.
2. First ask the plugin/agent to confirm that it can read all blocks, all connections/arrows, and the text inside the blocks.
3. If any of those elements are not visible or readable, stop before editing and resolve the access/readability problem.
4. Duplicate the diagram and preserve the original as the comparison/reference copy before making changes.

## Requested diagram transformation discussed

The requested cleanup is to replace individual “yes/no” decision blocks with labels on the corresponding arrows, so that the decision text is shown on the connection rather than as a separate block. The instruction explicitly includes removing the now-redundant block and its associated extra arrow while retaining the intended labeled connection.

## Validation and fallback

- Compare the edited diagram with the untouched copy.
- Verify that all blocks, connections and internal text remain present and that each “yes/no” path still leads to the correct destination.
- Do not report success based only on the plugin saying the edit is complete; inspect the actual diagram.
- If the plugin cannot see or modify the diagram, do not guess at the structure. Find another method or make the changes manually only when the intended transformation is clear.

## Task-specification lesson

The conversation highlights a recurring execution risk: the requester may omit details that seem obvious to them, while the person executing the task cannot safely infer those details. Tasks involving new rules or whole-system changes therefore need explicit scope, dependencies, expected behavior, and verification criteria before assignment.

[NEEDS_REVIEW: confirm the exact Miro board/diagram name and whether the plugin has the necessary read/write permissions.]

## Diagram readability and future visualization

- Short labels may be placed directly on arrows when they make the flow easier to read; long explanatory text should not be placed on arrows if it makes the diagram crowded.
- The discussion describes the current table/diagram as an “atlas” for understanding the strategy, while a future website may calculate/display arrow directions automatically.
- The future website is discussed as a plan; the conversation does not decide that the reference table/diagram should be deleted once the site exists.
- A change should be checked against the complete copied table, not only a few edited blocks.

[NEEDS_REVIEW: final role of the reference diagram/table versus the future website is not decided in this source.]

## Integrating a new rule into the human-facing strategy diagram

- Identify the exact original diagram named by the requester and confirm the agent can read all blocks, arrows, labels and text.
- Build a compact human-readable integration view that shows the new rule's entry point and direct dependencies on the original blocks.
- Do not expand the view into all internal continuation/programming logic if the requested goal is only to illustrate how the new rule interacts with the existing strategy.
- Verify every displayed condition against the supplied Telegram specification and original diagram; links must navigate to the intended blocks.
- Keep a duplicate/reference copy and compare the edited result before reporting completion.

[NEEDS_REVIEW: the source diagram name, block identities and exact spot-BTC rule remain unresolved in CALL-2026-10-07-002.]

Source: CALL-2026-10-05-002, turns 044–054, 061–086; CALL-2026-10-05-003, turns 008–015; CALL-2026-10-07-002, turns 021–034, 061–080.
