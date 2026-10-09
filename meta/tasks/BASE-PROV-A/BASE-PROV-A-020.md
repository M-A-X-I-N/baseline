# BASE-PROV-A-020 — Investigate agent contribution analytics and attribution limits

## Description

Research a reusable, repository-independent analyzer of the agent provenance system before implementing statistics. Study commit, diff, surviving-code and asset metrics without presenting weak attribution as fact.

## Requirements

- Specify commit participation counts and how a shared commit is apportioned or counted for multiple agents.
- Investigate additions/deletions and Git rename/binary semantics; distinguish gross churn from net retained content.
- Assess blame-based surviving line attribution, partial ownership, generated code, merges, moved lines, and the stability implications of rebases.
- For non-line-oriented assets, assess per-file/asset change counts, byte deltas, and attribution limitations rather than pretending every asset has meaningful LoC.
- Define exportable structured result and a human-readable summary for arbitrary repository/ref/time filters.
- Call out dependence on a provenance schema that can represent multiple agents and non-author roles.

## Constraints / non-goals

- Research and specification only, not an executable analytics implementation.
- Do not imply current-file authorship or asset authorship can be derived unambiguously from Git history.

## Acceptance criteria

- A bounded implementation proposal and metric taxonomy distinguish measurable facts, heuristics and unknown attribution.
- An eventual tool ownership location is proposed without treating baseline policy as a general utilities dump.

## Validation

- Test conceptual attribution on representative solo, joint, orchestrated, renamed, deleted and binary-asset commit examples.
