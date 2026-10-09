# Tasks

This is the authoritative scheduling index for sufficiently specified executable agent work.

Full non-terminal task instructions and temporary tracked task workspaces live under [`tasks/`](tasks/). Reminders and initiatives are not executable work and do not belong in Dispatch.

## Dispatch

_No QUEUED task is currently dispatched._

Dispatch is an ordered authorization/priority list, not a lifecycle state. Only `QUEUED` tasks with satisfied dependencies belong here. Claiming a task changes it to `IN_PROGRESS`, removes it from Dispatch, and records a live claim below.

## Active claims

Claims are live coordination locks, not identity or recovery credentials. The task index remains authoritative for lifecycle state.

| Task | Lineage | Canonical branch | Claimed at (UTC) | Notes |
|---|---|---|---|---|

## Active task index

### BASE-TASK-A

| ID | State | Depends on | Title | Summary |
|---|---|---|---|---|
| [`BASE-TASK-A-010`](tasks/BASE-TASK-A/BASE-TASK-A-010.md) | QUEUED | — | Permit controlled changes to unstarted tasks | Refine pre-start amendments without modifying already-owned work or granting execution. |
| [`BASE-TASK-A-020`](tasks/BASE-TASK-A/BASE-TASK-A-020.md) | QUEUED | — | Design explicit human-decision checkpoint tasks | Define an auditable approval/check-in gate for unattended agent loops. |
| [`BASE-TASK-A-030`](tasks/BASE-TASK-A/BASE-TASK-A-030.md) | QUEUED | `BASE-TASK-A-020` | Implement human-decision checkpoint task contract | Codify the approved safe wait-for-human task form after research and maintainer agreement. |

### BASE-PROV-A

| ID | State | Depends on | Title | Summary |
|---|---|---|---|---|
| [`BASE-PROV-A-010`](tasks/BASE-PROV-A/BASE-PROV-A-010.md) | QUEUED | — | Design multi-agent and orchestrator provenance | Compare multiple authorship trailers with role-based orchestration records; human decision before policy. |
| [`BASE-PROV-A-020`](tasks/BASE-PROV-A/BASE-PROV-A-020.md) | QUEUED | `BASE-PROV-A-010` | Investigate agent contribution analytics | Define truthful cross-repo commit/churn/surviving-code and binary-asset metrics. |

When tasks are added, record at least ID, state, dependencies, title, and a concise summary here, with the full execution contract in a linked file under `tasks/`.

## Task contract

Generic lifecycle, state meanings, Dispatch/claim behavior, recovery, dependency-vs-blocker distinction, deferred validation, and terminal advancement rules come from [`../.agents/baseline/WORKFLOW.md`](../.agents/baseline/WORKFLOW.md).

This index owns mutable scheduling metadata. Task specification files own full execution instructions. Do not duplicate mutable state in both places.
