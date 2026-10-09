# BASE-TASK-A-030 — Implement human-decision checkpoint task contract

## Description

Implement the selected explicit human-checkpoint task mechanism so unattended agents and orchestrators can pause between completed research and separately authorized execution without guessing or impersonating human approval.

## Requirements

- Apply the approved design from BASE-TASK-A-020 to the generic task lifecycle, schema and readable examples.
- Give agents a deterministic way to identify a pending human answer, formulate a precise question, record the returned decision and make successor tasks eligible only as explicitly authorized.
- Preserve existing task IDs, Dispatch, claims, branches and conservative no-answer behavior.
- Provide a migration/compatibility story for ordinary existing tasks and explain how a human-gate task differs from BLOCKED and FROZEN.

## Constraints / non-goals

- Depends on a maintainer-approved design; an agent cannot infer approval from silence, a model's response or completing prerequisite research.
- This task does not independently authorize applying the new mechanism across consumer repositories.

## Acceptance criteria

- The baseline task contract supports the approved human checkpoint with examples and unambiguous no-answer behavior.
- Consumers can adopt the change without invalidating existing lifecycle state.

## Validation

- Review prospective state transitions and authorization invariants, including automated loops and interrupted-session recovery.
- Check baseline instructions and a representative consumer task ledger for consistency.
