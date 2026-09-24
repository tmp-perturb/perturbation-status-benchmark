# Conversion report

## Pipeline mapping

| Stage | Module repository | Contract |
| --- | --- | --- |
| Data | `perturbation-status-data` | Canonical H5AD plus dataset specification |
| Shared signature | `perturbation-status-mixscape-mixscale` | CalcPerturbSig checkpoint and target shards |
| Status estimation | `perturbation-status-mixscape-mixscale` | Mixscape or Mixscale canonical cell scores |
| Status estimation | `perturbation-status-ps` | PS canonical cell scores |
| Metrics | `perturbation-status-metrics` | Complete v0.3 benchmark archive and summary |

## Metric interpretation

The benchmark compares three methods: Mixscape, Mixscale, and PS. Target
expression is generated transiently inside the engagement metric and is never
treated as a method. Profile reproducibility is construct-aware: eligible pairs
must have distinct construct IDs and disjoint observed guide sets. Papalexi and
Replogle are estimable; Norman is explicitly not applicable.

## Assumptions

- Absolute local data and environment paths are retained for internal review.
- Shared signature generation is a technical dependency, not a method ranking.
- PS accepts the stage-level shared-artifact argument but does not read it.

## Validation

- Omnibenchmark plan validation and 16-rule dry-run passed.
- Papalexi 2021 completed end to end for all three methods and all benchmark stages.
- The transient target-expression reference covered all 13,757 eligible targeted cells.
