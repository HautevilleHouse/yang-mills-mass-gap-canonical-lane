# Yang-Mills Mass Gap Framework

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18876069.svg)](https://doi.org/10.5281/zenodo.18876069)

Canonical-lane research workspace for the Millennium problem:
existence of a nontrivial quantum Yang-Mills theory on `R^4` with a strict positive mass gap.

## Main Manuscript

- [paper/YANG_MILLS_MASS_GAP_PREPRINT.md](paper/YANG_MILLS_MASS_GAP_PREPRINT.md)
- [paper/CANONICAL_ROUTING_INDEX.md](paper/CANONICAL_ROUTING_INDEX.md)

## Structure

- `paper/`
  - `YANG_MILLS_MASS_GAP_PREPRINT.md`
  - `CANONICAL_ROUTING_INDEX.md`

- `notes/`
  - `EG1_public.md`
  - `EG2_public.md`
  - `EG3_public.md`
  - `EG4_public.md`
  - `IDENTIFICATION_BRIDGE.md`

- `repro/`
  - `REPRO_PACK.md`
  - `THIRD_PARTY_RERUN_PROTOCOL.md`
  - `run_repro.sh`
  - `repro_manifest.json`
  - `certificate_baseline.json`

- `scripts/`
  - `ym_closure_guard.py`

- `artifacts/`
  - `constants_registry.json`
  - `stitch_constants.json`

## Local Repro Command

```bash
bash repro/run_repro.sh
```

This writes `repro/certificate_runtime.json`.

## How To Read This Professionally

1. Theorem chain first: read `paper/YANG_MILLS_MASS_GAP_PREPRINT.md`.
2. Constants provenance second: audit `paper/EXTRACTION_SPEC.md`, `artifacts/constants_extraction_inputs.json`, `artifacts/constants_extracted.json`, and `artifacts/promotion_report.json`.
3. Pipeline third: run `bash repro/run_repro.sh` to audit hashes/provenance/gates; it is reproducibility infrastructure, not theorem generation.

Release modes:

- `normalized`: `status=normalized_placeholder` allowed when explicitly labeled.
- `fully_extracted`: requires `status=derived_numeric` for all required constants/stitch keys.

Current YM runner policy:

- `repro/run_repro.sh` enforces `fully_extracted` mode.

## Routing Rule (inclusion discipline)

Every claim-bearing item must be routed through all three layers:

1. main preprint section/appendix,
2. mirror note under `notes/`,
3. artifact key consumed by `scripts/ym_closure_guard.py`.

Routing map: [paper/CANONICAL_ROUTING_INDEX.md](paper/CANONICAL_ROUTING_INDEX.md)

## Local-Only Policy

- See [LOCAL_ONLY_POLICY.md](LOCAL_ONLY_POLICY.md).
- Remote publish is blocked unless explicitly overridden.

## Citation

- Metadata: [CITATION.cff](CITATION.cff)
- Manuscript target: [paper/YANG_MILLS_MASS_GAP_PREPRINT.md](paper/YANG_MILLS_MASS_GAP_PREPRINT.md)

## Authorship

- Program author: **HautevilleHouse**
- Canonical attribution source: [`CITATION.cff`](CITATION.cff)
