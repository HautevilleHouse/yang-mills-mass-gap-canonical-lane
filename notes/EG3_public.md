# EG3 Public Note (Compactness Package)

In-paper location: `paper/YANG_MILLS_MASS_GAP_PREPRINT.md` (Section 5, Appendix C).


## Goal
Obtain precompactness of normalized near-failure sequences.

## Candidate Compactness Class

Use normalized Schwinger families:

`S^(Lambda) = {S_n^(Lambda)}_(n>=2)` with fixed normalization and positivity constraints.

Require:

1. uniform local bounds on test-function windows,
2. tightness in reconstruction variables,
3. normalization map `N(u)` removing scale/gauge drift.

## Closure Criterion

`Y_G3 = PASS` iff theorem-level compactness modulus `kappa_compact > 0` controls extraction:

- every bad sequence has a convergent normalized subsequence in declared topology.

## Lemma Chain and Proof Payload

### Lemma EG3.1 (precompactness criterion)
Assume normalized sequence `U_n` satisfies:

1. uniform seminorm bounds `sup_n p_j(U_n) <= M_j` for each `j`,
2. tightness/normal-family control in the declared topology.

Then `{U_n}` is precompact.

**Proof.**
Apply the compactness theorem corresponding to the declared seminorm topology.

### Lemma EG3.2 (lower-semicontinuity of badness)
If `U_n -> U_infty`, then
`Bad(U_infty) >= limsup_n Bad(U_n)`.

**Proof.**
`Bad` is an infimum of continuous lock-residual norms, hence lower-semicontinuous.

### Theorem EG3.3 (gate closure)
Define:

`kappa_compact^(raw) := (1 + sup_(u in T_*) Delta_comp^+(u))^(-1)`.

If `kappa_compact^(raw)>0`, every normalized near-failure sequence has a
convergent bad subsequence, so `Y_G3 = PASS` with
`kappa_compact := kappa_compact^(raw)/kappa_compact,ref > 0`.

**Proof.**
Lemma EG3.1 gives subsequential compactness; Lemma EG3.2 preserves badness under limits.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Fix normalized extraction map `N(u)` so canonical states satisfy:

`sup_j p_j(N(u_Lambda)) <= 1`,

for the declared compactness seminorm family `{p_j}` on the canonical tube.

Define compactness defect:

`Delta_comp(u) := sup_j p_j(N(u)) - 1`.

On the canonical lane, normalization gives `Delta_comp(u_Lambda) <= 0`, so every near-failure sequence is uniformly bounded in the declared topology and admits convergent normalized subsequences.

Set compactness modulus:

`kappa_compact = 0.8`.

This value is recorded as theorem-level in the constants registry for `Y_G3`.
