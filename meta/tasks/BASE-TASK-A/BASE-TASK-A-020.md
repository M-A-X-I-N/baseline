# BASE-TASK-A-020 — Design explicit human-decision checkpoint tasks

## Description

Define a first-class way for agent workflows to stop and ask the maintainer for an explicit decision or authorization, especially between an investigation and an implementation phase.

## Requirements

- Compare a designated task variant/kind against an ordinary task with an explicit human gate, identifying which semantics need codification.
- Specify scheduling, dependency, Dispatch, ownership, timeout/absence, completion evidence, and branching behavior for unattended or orchestrated loops.
- Define precise questions, available decisions, recorded answer/source, and safe no-answer behavior; never treat silence as approval.
- Cover how follow-up implementation tasks become eligible without conflating completed investigation with implementation approval.

## Constraints / non-goals

- Design only; do not implement a new lifecycle state or automatic approval mechanism before examining the existing task contract.
- Do not change existing task authorization semantics or permit agents to fabricate maintainer input.

## Acceptance criteria

- A reviewable design with concrete examples and migration/backward compatibility implications is available.
- Any policy choice genuinely requiring maintainer judgment is surfaced explicitly.

## Validation

- Cross-check against WORKFLOW.md, claimed lineages, Dispatch and typical automated orchestrator cases.
