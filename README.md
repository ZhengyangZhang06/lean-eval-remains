# LeanEval remaining-problems experiment

Eleven benchmark problems, using `github-theorem-prover` from `humanfia/math-lean-flow`, branch `feature/humanize-api-update`. New Docker issue jobs use revision [`92d69bf`](https://github.com/humanfia/math-lean-flow/commit/92d69bf); the two original rollout-canary jobs retain their immutable earlier runtime.

[Live proving-status website](https://zhengyangzhang06.github.io/lean-eval-remains/theorem-status/).

This is a Git copy of the original experiment, with all 13 source branches copied on 2026-10-10. It is not a GitHub repository transfer: existing issues, PRs and active proof workers remain in [humanfia/lean-eval-remains](https://github.com/humanfia/lean-eval-remains). Their original links are preserved; opening those private records requires repository access. The copied contract branches are frozen snapshots, not a claim of continuous proof-branch mirroring.

The experiment has a shared pool of **128 Docker workers**, one per physical node, using **`codex/gpt-6-astra:max`** for both worker and reviewer roles. There is no two-worker-per-problem quota: independently ready theorem issues from the same problem can use any free pool nodes. Available pollers, assigned issue jobs, model turns and proved theorems are different counts. At the 2026-10-10 08:24 UTC rollout observation, 21 jobs were assigned across all 11 problems; five belonged to Shafarevich. Newly assigned jobs may still be validating references.

Speculative parent formalization was enabled on 2026-10-10 at 08:44 UTC by resuming the broker with `--enable-speculative-proving`. New job grants enable speculative mode; previously running jobs retain their original immutable settings. Parents may draft using unfinished children's exact interfaces, then wait for actual child proofs and normal verification. These drafts do not mark children or parents proved. The broker-only restart preserved all 128 worker containers and the 25 then-owned job grants; 17 newly eligible tasks were subsequently granted speculative mode.

The website observes all 11 preserved runs without changing proof acceptance. Each assigned DAG task shows its physical node, Docker task, worker phase and original heartbeat time, with full details in its tooltip and theorem row. The overview counts shared fleet capacity and idle workers once, not once per problem. Separate read-only monitors measure Codex/Lean/Lake processes in each worker container's process tree, matched to its exact Docker task. The dashboard reports coverage across all 128 nodes; stale or missing reports are partial/unknown, not zero. These are operating-system process counts, not active API requests. Monitors were deployed without restarting proof jobs.

Live observations publish all 11 problem feeds together in one atomic `status-live` update, targeting 30-second cycles (longer if observation/publication takes longer). A separate supervised process publishes Pages snapshots every ten minutes; Pages work cannot block live updates. Both publishers use node-local Git storage, while proof workspaces stay on shared storage. The overview checks feeds every 30 seconds. Data older than three minutes is excluded from live counts, with explicit stale/unknown warnings; saved progress remains visible. The reusable publisher is maintained in the flow repository. Publication is not proof acceptance.

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
