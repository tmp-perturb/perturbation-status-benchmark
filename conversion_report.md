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

- Only source H5AD paths remain local. Method code and configuration are owned
  by their modules, and software environments are declared by versioned Conda
  YAML files in this benchmark repository. Exact Git-only R sources are bundled
  with their owning modules.
- Shared signature generation is a technical dependency, not a method ranking.
- PS accepts the stage-level shared-artifact argument but does not read it.

## Validation

- The v0.5 plan and all module entrypoints passed structural and syntax checks.
- The Mixscape, Mixscale, and PS Conda environments completed dry solving.
- Papalexi 2021 completed end to end after removal of the development-project dependency.
- The transient target-expression reference covered all 13,757 eligible targeted cells.
- Parity passed for all 32 comparable Papalexi tables, including harmonized scores,
  expression intermediates, metrics, and the final summary.
