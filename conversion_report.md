# Conversion report

## Pipeline mapping

| Stage | Module repository | Contract |
| --- | --- | --- |
| Data | `perturbation-status-data` | Canonical H5AD plus dataset specification |
| Shared signature | `perturbation-status-mixscape-mixscale` | CalcPerturbSig checkpoint and target shards |
| Status estimation | `perturbation-status-mixscape-mixscale` | Mixscape or Mixscale canonical cell scores |
| Status estimation | `perturbation-status-ps` | PS canonical cell scores |
| Metrics | `perturbation-status-metrics` | Complete current data-only benchmark archive and summary |

## Metric interpretation

The benchmark compares three perturbation-status estimators: Mixscape,
Mixscale, and PS. The target-expression baseline is generated transiently by
the metric collector and is retained as a descriptive reference comparator,
not a fourth primary estimator. Direct-expression validation is NTC-free and
uses the checksum-verified frozen direction-adjusted cell table. Profile
reproducibility is construct-aware and symmetrizes disjoint, batch-matched NTC
halves; eligible pairs require distinct guide implementations and disjoint
targeted cells. Papalexi and Replogle are estimable; Norman is explicitly not
applicable.

## Assumptions

- Absolute local data and environment paths are retained for internal review.
- Shared signature generation is a technical dependency, not a method ranking.
- PS accepts the stage-level shared-artifact argument but does not read it.

## Validation

- Omnibenchmark plan validation and 16-rule dry-run passed.
- Papalexi 2021 completed end to end for all three methods and all data-only benchmark stages.
- The transient target-expression reference covered all 13,757 eligible targeted cells.
- Parity passed for all 32 comparable Papalexi tables, including harmonized scores,
  expression intermediates, metrics, and the final summary.
