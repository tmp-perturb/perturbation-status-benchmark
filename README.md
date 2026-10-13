# Perturbation-status estimation benchmark

Omnibenchmark plan for Papalexi 2021, Norman 2019, and Replogle 2022.
Mixscape, Mixscale, and PS are benchmarked as perturbation-status estimators.
The target-expression baseline is computed transiently inside the metric
collector and retained only as a reference comparator. The current benchmark is
data-only: figure generation remains in the separate thesis figure framework.

Method scripts and benchmark configuration are versioned inside their owning
modules; no module imports code or environments from the original development
project. Fixed Apptainer definitions are published with the method repositories
and the plan uses their public, versioned GitHub Release images. All module repositories are
pinned to reviewed commits in the `tmp-perturb` organization.

The only remaining machine-local values are the three source H5AD parameters.
They are the benchmark inputs and are intentionally left for a separate data
distribution decision.
