# BASE-AGENT-ANALYTICS — Repository-independent agent contribution analytics

**Status:** OPEN

## Goal

Eventually provide trustworthy agent-contribution analytics for an arbitrary Git repository using the standardized agent provenance trailers, while preserving uncertainty for collaborative work and non-text assets.

## Current state / coverage

The generic baseline currently requires `Agent-authored-by:` on wholly agent-authored substantive commits. It has no policy yet for multiple agent authors or orchestrator-only roles, and no analytics command-line tool. The maintainer wants initial commit and insertion/deletion counts followed by current surviving-code and binary/asset-oriented statistics.

## Known gaps

- Multiple-agent and orchestrator-only trailer semantics, stable parse rules and backward compatibility.
- Commit participation statistics, shared-commit counting policies, lines added/removed and rename/merge handling.
- Surviving line authorship through blame and limitations around generated, moved, removed or reformatted content.
- Per-asset/binary counts, byte deltas and approximate attribution where lines of code are meaningless.
- An eventual reusable tool and clear report formats for arbitrary repository/ref selections.

## Deliberate boundaries / deferred work

- Analytics is not proof of actual human or agent intellectual contribution. Separate precise Git measurements from heuristics.
- No history rewrite or automatic insertion of missing provenance.
- Do not implement the tool before multi-agent trailer/role choices are agreed and feasibility research identifies a sensible home for executable tooling; baseline's instruction repo should not become an arbitrary utilities warehouse by accident.

## Related executable tasks

- [`BASE-PROV-A-010`](../tasks/BASE-PROV-A/BASE-PROV-A-010.md) — provenance semantics.
- [`BASE-PROV-A-020`](../tasks/BASE-PROV-A/BASE-PROV-A-020.md) — analytics feasibility and metric model.

## Promotion / closure criteria

Promote a bounded implementation task once the attribution schema and metric limitations are settled. Complete when a reusable analyzer produces documented, reproducible and honestly qualified metrics on representative text and asset-heavy repositories.
