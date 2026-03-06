# Canonical Routing Index (Yang-Mills)

This file is the single routing map for where each proof package lives in:

- main preprint sections/appendices,
- mirror note files,
- certificate/artifact keys.

## Gate Routing

| Gate | Main preprint location | Mirror note | Registry/artifact key(s) |
|---|---|---|---|
| `Y_G1` (coercivity) | `Section 4`, `Appendix A` | `notes/EG1_public.md` | `kappa_coercive` |
| `Y_G2` (capture) | `Section 5`, `Appendix B` | `notes/EG2_public.md` | `sigma_capture` |
| `Y_G3` (compactness/no-Zeno) | `Section 5`, `Appendix C` | `notes/EG3_public.md` | `kappa_compact` |
| `Y_G4` (reconstruction positivity) | `Section 6`, `Appendix D` | `notes/EG4_public.md` | `rho_os` |
| `Y_G5` (mass-gap floor) | `Section 6`, `Appendix E` | `notes/EG4_public.md` | `m_gap_lower` |
| `Y_G6` (strict coherence) | `Section 8`, `Appendix E` | all `EG*` notes | `eps_coh` |
| `Y_GM` (final strict margin) | `Section 8` | derived (no standalone note) | all above keys |

## Identification Routing

| Topic | Main preprint location | Mirror note |
|---|---|---|
| Determining class and lock | `Section 6.3`, `Appendix E` | `notes/IDENTIFICATION_BRIDGE.md` |

## Repro Routing

| Artifact | Path |
|---|---|
| Runner | `repro/run_repro.sh` |
| Guard | `scripts/ym_closure_guard.py` |
| Runtime certificate | `repro/certificate_runtime.json` |
| Baseline certificate | `repro/certificate_baseline.json` |
| Registry | `artifacts/constants_registry.json` |
| Stitch constants | `artifacts/stitch_constants.json` |
| Third-party rerun protocol | `repro/THIRD_PARTY_RERUN_PROTOCOL.md` |

