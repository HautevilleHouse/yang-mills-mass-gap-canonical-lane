# Scripts

- `ym_closure_guard.py`: canonical-lane closure gate evaluator for Yang-Mills.

Guard inputs:

- `artifacts/constants_registry.json`
- `artifacts/stitch_constants.json`

Guard output:

- `repro/certificate_runtime.json`

Output schema includes:

- native gate keys (`Y_G*`),
- normalized gate layer (`G1..G6,GCoh,GM`) under `normalized`,
- strict pass flags: `all_pass`, `all_pass_normalized`.
