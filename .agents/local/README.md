# Local instruction router

This file is repository-owned. It indexes repository-specific normative instructions, executable-work locations, and local memory organization.

Adding a repository-specific instruction file does **not** require a matching baseline file. Register the new file and its read trigger here; do not modify the baseline router merely to make the local file discoverable.

## Always for substantial repository work

Read [`REPOSITORY.md`](REPOSITORY.md).

It owns the repository-specific identity, source-of-truth map, engineering conventions, and local task/reminder/initiative locations.

## Subject-triggered local policy

Add repository-specific instruction files and their read triggers here as they become necessary.

Do not create local instruction files merely to mirror baseline filenames.

## Executable-work locations

The seed layout groups repository-control surfaces under [`../../project_control/`](../../project_control/):

- ledger / Dispatch / Active claims: [`../../project_control/tasks.md`](../../project_control/tasks.md);
- active task specifications/workspaces: [`../../project_control/tasks/`](../../project_control/tasks/);
- reminders: [`../../project_control/reminders.md`](../../project_control/reminders.md);
- initiatives: [`../../project_control/initiatives/`](../../project_control/initiatives/).

A repository may deliberately choose different local paths. If it does, update this local router and local policy; baseline-owned files should not need modification.

## Local memory organization

Repository-specific non-normative knowledge belongs under `../memory/`.

Do not preload memory and do not create empty taxonomy for appearance. Add categories only when useful knowledge actually needs them.
