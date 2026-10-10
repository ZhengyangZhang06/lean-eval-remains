# LeanEval remaining-problems experiment

Eleven benchmark problems, using `github-theorem-prover` from `humanfia/math-lean-flow`, branch `feature/humanize-api-update`, deployed revision [`6feb940`](https://github.com/humanfia/math-lean-flow/commit/6feb940fb9fde23dcd09f5686514cb4d6be913f2).

[Live proving status](https://humanfia.github.io/lean-eval-remains/theorem-status/index.html) (available after the first successful Pages deployment).

Hosting status (2026-10-10): GitHub currently rejects Pages for this private repository under its account plan (HTTP 422). No live site is claimed; generated website source is retained in `gh-pages`. GitHub proof issues and PRs do not require Pages to be available.

Each problem has an isolated branch, a root issue, recursive child issues, and verified solution PRs. Root PRs target the corresponding problem branch. Automatic merging and manual issue closure are disabled. An open issue, running worker, or successful build is not proof acceptance.

Lean: `leanprover/lean4:v4.35.0-rc4`. Mathlib: `a02a63c2100af866343c74550041885f8f39f099`. Internet research is enabled. Each root must pass the full original benchmark comparator and Nanoda. The motivic-invariants problem retains all six theorem targets; the Bose-gas and Hopf problems also retain their definition holes.

| Problem | Contract branch |
| --- | --- |
| annals_bose_gases | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/annals_bose_gases) |
| annals_motivic_invariants | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/annals_motivic_invariants) |
| cdt_linearIndependent | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/cdt_linearIndependent) |
| feit_thompson | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/feit_thompson) |
| gorenstein_walter | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/gorenstein_walter) |
| hopf_s6_complex_structure | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/hopf_s6_complex_structure) |
| mandelbar_not_path_connected | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/mandelbar_not_path_connected) |
| shafarevich_solvable_galois | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/shafarevich_solvable_galois) |
| smooth_knot_has_quadrisecant | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/smooth_knot_has_quadrisecant) |
| sphere_theorem_differentiable | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/sphere_theorem_differentiable) |
| wang_zahl_kakeya_dimH | [frozen problem](https://github.com/humanfia/lean-eval-remains/tree/problems/wang_zahl_kakeya_dimH) |
