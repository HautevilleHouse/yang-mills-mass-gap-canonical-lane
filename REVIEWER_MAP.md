# Reviewer Map

## Claim Scope
- Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level Yang-Mills closure claim is satisfied.
- Physical/classical bridge claim: the standard Yang-Mills existence + mass-gap statement additionally uses the explicit bridge assumptions `YM_EQ1` and `YM_EQ2` from Section `6.4` and Appendix `E`.

## Theorem Dependency Chain
1. `EG1`: projected coercivity / structural floor.
2. `EG2`: capture + flow/restart invariance.
3. `EG3`: finite-restart spacing (no Zeno cascade).
4. `EG4`: compactness-rigidity and endpoint identification.
5. Scalar closure: `Y_G1, Y_G2, Y_G3, Y_G4, Y_G5, Y_G6, Y_GM` all `PASS`.
6. `YM_EQ1`: determining-class adequacy on the reconstructed admissible class.
7. `YM_EQ2`: positivity-to-gap transfer inequality on the reconstructed class.

Primary files:
- `paper/YANG_MILLS_MASS_GAP_PREPRINT.md`
- `notes/EG1_public.md`
- `notes/EG2_public.md`
- `notes/EG3_public.md`
- `notes/EG4_public.md`
- `notes/IDENTIFICATION_BRIDGE.md`

## Falsification Conditions
- `repro/certificate_runtime.json` has any non-`PASS` gate.
- `lane.active_lane != "manifold_constrained"`.
- `all_pass != true`.
- Any manifest hash mismatch under `repro/repro_manifest.json`.
- A verified counterexample to any EG theorem statement used in the paper.

## Reproducibility Check
Run:

```bash
bash repro/run_repro.sh
```

Then verify:

```bash
python3 - <<'PY'
import json
from pathlib import Path
d=json.loads(Path("repro/certificate_runtime.json").read_text())
assert d.get("all_pass") is True
assert d.get("lane",{}).get("active_lane") == "manifold_constrained"
for g in ["Y_G1","Y_G2","Y_G3","Y_G4","Y_G5","Y_G6","Y_GM"]:
    assert d["gates"].get(g) == "PASS", g
print("OK")
PY
```
