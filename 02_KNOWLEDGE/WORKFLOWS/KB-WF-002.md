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

Source: CALL-2026-10-05-002, turns 044–054, 061–086.
