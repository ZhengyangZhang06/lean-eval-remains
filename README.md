# LeanEval remaining-problems experiment

Eleven benchmark problems, using `github-theorem-prover` from `humanfia/math-lean-flow`, branch `feature/humanize-api-update`, deployed revision [`6feb940`](https://github.com/humanfia/math-lean-flow/commit/6feb940fb9fde23dcd09f5686514cb4d6be913f2).

[Live proving-status website](https://zhengyangzhang06.github.io/lean-eval-remains/theorem-status/).

This is a Git copy of the original experiment, with all 13 source branches copied on 2026-10-10. It is not a GitHub repository transfer: existing issues, PRs and active proof workers remain in [humanfia/lean-eval-remains](https://github.com/humanfia/lean-eval-remains). Their original links are preserved; opening those private records requires repository access. The copied contract branches are frozen snapshots, not a claim of continuous proof-branch mirroring.

The website observes all 11 active runs without changing their proof records. Live observations publish repeatedly to `status-live` (60-second waits between cycles, plus publication time); Pages snapshots publish every ten minutes or later if the preceding cycle is still publishing. The overview checks feeds every 30 seconds and shows controllers alive, working issue jobs, idle pollers, live model processes, saved root proof stages, verified results, and observation timestamps. Data older than three minutes is excluded from live counts, with explicit stale/unknown warnings; saved progress remains visible. The reusable publisher is maintained in the flow repository, deployed revision [`48cf300`](https://github.com/humanfia/math-lean-flow/commit/48cf300). Publication is not proof acceptance.

Each problem has an isolated branch, a root issue, recursive child issues, and verified solution PRs. Root PRs target the corresponding problem branch. Automatic merging and manual issue closure are disabled. An open issue, running worker, or successful build is not proof acceptance.

Lean: `leanprover/lean4:v4.35.0-rc4`. Mathlib: `a02a63c2100af866343c74550041885f8f39f099`. Internet research is enabled. Each root must pass the full original benchmark comparator and Nanoda. The motivic-invariants problem retains all six theorem targets; the Bose-gas and Hopf problems also retain their definition holes.

| Problem | Contract branch |
| --- | --- |
| annals_bose_gases | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/annals_bose_gases) |
| annals_motivic_invariants | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/annals_motivic_invariants) |
| cdt_linearIndependent | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/cdt_linearIndependent) |
| feit_thompson | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/feit_thompson) |
| gorenstein_walter | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/gorenstein_walter) |
| hopf_s6_complex_structure | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/hopf_s6_complex_structure) |
| mandelbar_not_path_connected | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/mandelbar_not_path_connected) |
| shafarevich_solvable_galois | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/shafarevich_solvable_galois) |
| smooth_knot_has_quadrisecant | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/smooth_knot_has_quadrisecant) |
| sphere_theorem_differentiable | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/sphere_theorem_differentiable) |
| wang_zahl_kakeya_dimH | [frozen problem](https://github.com/ZhengyangZhang06/lean-eval-remains/tree/problems/wang_zahl_kakeya_dimH) |
