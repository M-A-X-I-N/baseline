# BASE-TASK-A-010 — Permit controlled changes to unstarted tasks

## Description

Refine the generic task contract so a not-yet-started task can be amended without an unnecessary cancel/supersede cycle when upstream work, explicit maintainer direction, or an evident correction changes the right scope.

## Requirements

- Define the editable/unstarted boundary, including QUEUED, FROZEN and BLOCKED versus claimed or already-worked tasks; require checking live claims and branches rather than trusting state labels alone.
- Specify how to adjust requirements, acceptance criteria, dependency links, and index summaries while keeping published IDs stable and avoiding silent scope inflation.
- Record when a change is editorial versus substantively new work requiring human authorization or an additional task.
- Clarify how dependency-driven task updates differ from task execution and Dispatch authorization.

## Constraints / non-goals

- Do not modify or reassign tasks already in progress, claimed by another lineage, or represented by substantive commits without authorized reconciliation.
- Do not imply that editing, queuing, thawing, or unblocking grants permission to execute.

## Acceptance criteria

- Generic task policy explicitly permits safe pre-start amendments and preserves immutable IDs, claims and Dispatch safeguards.
- A task-identity and amendment example covers upstream-task discoveries, human changes and obvious corrections.

## Validation

- Review against the baseline WORKFLOW.md and a consuming repository task ledger; check lifecycle and authority consistency.
