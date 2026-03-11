# Public Reproducibility Pack (YM Canonical Lane)

## Objective
Provide a local, hash-locked rerun path for the Yang-Mills closure gate certificate.

Authoritative routing index:

- `paper/CANONICAL_ROUTING_INDEX.md`

## Included Artifacts

1. `repro_manifest.json`,
2. `run_repro.sh`,
3. baseline output `certificate_baseline.json`,
4. `THIRD_PARTY_RERUN_PROTOCOL.md`.

## Runner

From repository root:

```bash
bash repro/run_repro.sh
```

This executes:

```bash
python3 scripts/ym_closure_guard.py --strict-coh-zero --registry artifacts/constants_registry.json --stitch artifacts/stitch_constants.json --out repro/certificate_runtime.json --history repro/drift_guard_runs.jsonl --pretty
```

## Pass Criteria

1. `repro/certificate_runtime.json` exists,
2. lane is `manifold_constrained`,
3. `all_pass` is `true`,
4. all gates `Y_G1,Y_G2,Y_G3,Y_G4,Y_G5,Y_G6,Y_GM` are `PASS`.

## Current Runtime Snapshot

At current registry state:

- `Y_G1..Y_G6,Y_GM = PASS`,
- strict margin `= 1.0`,
- lane remains `manifold_constrained`.
