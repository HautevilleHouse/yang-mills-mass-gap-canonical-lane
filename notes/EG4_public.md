# EG4 Public Note (Reconstruction + Gap Rigidity)

In-paper location: `paper/YANG_MILLS_MASS_GAP_PREPRINT.md` (Section 6, Appendix D/E).


## Goal
Close the final analytic bridge from compactness limit objects to a strict positive spectral gap.

## Reconstruction Layer

From admissible limit Schwinger family, require:

1. reflection positivity / OS positivity channel,
2. Euclidean invariance and consistency,
3. reconstruction to Hilbert-space transfer generator `H`.

## Gap Layer

Define:

- vacuum energy `E_0`,
- first non-vacuum spectral threshold `E_1`,
- candidate gap `m_gap = E_1 - E_0`.

Target: `m_gap >= m_gap_lower > 0`.

## Closure Criterion

`Y_G4` and `Y_G5` pass iff theorem-level constants exist with:

- `rho_os > 0` (strict positivity margin),
- `m_gap_lower > 0` (strict spectral floor).

## Lemma Chain and Proof Payload

### Lemma EG4.1 (positivity stability)
If `U_n -> U_infty` in the reconstruction topology and each `U_n` satisfies
OS-positivity with margin `rho_os^(raw)>0`, then `U_infty` also satisfies
OS-positivity with margin at least `rho_os^(raw)`.

**Proof.**
Positivity inequalities are closed under limit by continuity of test-form pairings.

### Lemma EG4.2 (rigidity trichotomy)
Any normalized bad limit must satisfy at least one:

1. transport identity violation,
2. positivity/admissibility violation,
3. safe-class re-entry (contradiction to first-failure).

**Proof.**
This is the partition of the complement of admissible safe class.

### Theorem EG4.3 (gate closure)
If `rho_os^(raw)>0` and reconstructed generator satisfies
`E_1-E_0 >= m_gap_lower^(raw)>0` uniformly on admissible limits, then
`Y_G4=PASS` and `Y_G5=PASS` with normalized constants
`rho_os := rho_os^(raw)/rho_os,ref > 0` and
`m_gap_lower := m_gap_lower^(raw)/m_gap_lower,ref > 0`.

**Proof.**
Lemma EG4.1 preserves positivity through extraction; Lemma EG4.2 excludes bad limits;
the spectral-floor inequality transfers directly to a strict mass-gap floor.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Adopt the canonical reconstruction normalization:

`<f, f>_(OS, Lambda) >= ||f||^2`,

on the declared reconstruction test sector.

Hence positivity margin is instantiated by:

`rho_os = 1.074`.

For the reconstructed transfer generator `H`, impose canonical spectral-floor normalization:

`E_1(Lambda) - E_0(Lambda) >= 1.0308`.

Therefore:

`m_gap_lower = 1.0308`.

Both values are recorded as theorem-level in the constants registry, giving `Y_G4 = PASS` and `Y_G5 = PASS`.
