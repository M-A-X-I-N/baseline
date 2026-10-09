# BASE-PROV-A-010 — Design multi-agent and orchestrator provenance

## Description

Investigate how commit trailers should accurately represent multiple substantive agent contributors and agent orchestration or review that did not itself author changes.

## Requirements

- Define when multiple Agent-authored-by trailers are truthful and how ordering, duplication, names, model identity and human authorship are represented.
- Compare an optional agent-work-description trailer versus role-specific contribution/provenance trailers, preserving compatibility with the existing single-agent format.
- Distinguish authorship, orchestration, planning, review, operation and human approval without automatically assigning code authorship to coordinators.
- Document reproducible parsing rules for analytics and migration of existing records without destructive history edits.
- Present unresolved subjective choices to the maintainer before any normative trailer change.

## Maintainer direction

- **2026-10-09 maintainer direction:** Keep orchestrator-only provenance undecided until investigation. Neither a role-specific trailer nor expanding `Agent-authored-by:` to orchestration is preselected.
- Present alternatives, accurate attribution boundaries and backward-compatibility implications for a later explicit decision; research must not silently amend the live provenance grammar.

## Constraints / non-goals

- Investigation/design only; do not promulgate a role grammar or rewrite commit history as an unreviewed default.
- Never claim nonexistent substantive contributions or human approval.

## Acceptance criteria

- Alternative schemas and examples covering multiple authors, non-author orchestrators, and mixed human/agent work are documented with tradeoffs.
- Maintainer decision points are explicit.

## Validation

- Check examples against existing PROVENANCE.md and GIT.md and the git-trailer parsing model.
