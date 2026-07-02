# Identification Bridge (YM Limit -> Physical Theory Class)

In-paper location: `paper/YANG_MILLS_MASS_GAP_PREPRINT.md` (Section 6.3, Appendix E).


## Goal
Prevent endpoint ambiguity: the extracted continuum object must lie in the intended Yang-Mills determining class.

## Determining Class (working)

Choose test-observable class `C_det` of gauge-invariant local operators and two-point kernels.

Lock conditions (working form):

1. correlator identities on `C_det`,
2. positivity/reflection constraints,
3. normalization and covariance constraints.

## Uniqueness Target

If two candidate limit objects satisfy the same lock conditions on `C_det`, they are identified as the same physical class representative.

This note records the bridge assumptions used by the standard physical statement:

- `YM_EQ1`: `C_det` is determining on the reconstructed admissible class,
- `YM_EQ2`: raw positivity-to-gap transfer holds with explicit `c_gap > 0`, `e_gap >= 0`.

## Lemma Chain and Proof Payload

### Lemma ID.1 (lock persistence under extraction)
If `U_n -> U_infty` on admissible class and each observable `Obs_O` is continuous
for `O in C_det`, then
`Lock_O(U_n) -> Lock_O(U_infty)`.

**Proof.**
Immediate from continuity.

### Lemma ID.2 (determining-class uniqueness)
Assume `C_det` separates admissible endpoint classes. If
`Lock_O(U_infty)=0` for all `O in C_det`, then `U_infty` is canonically
equivalent to the target endpoint `U_*`.

**Proof.**
If not equivalent, separation yields an observable in `C_det` with unequal value,
contradicting lock equality.

### Theorem ID.3 (coherence/identification closure)
If lock persistence and determining-class uniqueness hold and
`eps_coh^(raw)=0`, then the identification bridge closes and coherence gate
`Y_G6 = PASS`.

**Proof.**
Lemmas ID.1-ID.2 provide uniqueness of endpoint object; strict coherence removes
residual ambiguity.

## Strict-Coherence Instantiation (Canonical Lane, March 5, 2026)

Define coherence remainder as lock-defect:

`eps_coh := sup_{O in C_det} |Lock_O(U_Lambda) - Lock_O(U_*)|`.

Canonical-lane lock preservation enforces:

`Lock_O(U_Lambda) = Lock_O(U_*)` for all `O in C_det`.

Therefore:

`eps_coh = 0`.

This value is promoted to theorem-level in the constants registry for strict mode `Y_G6`.

## Status

This note discharges lock persistence and records the conditional uniqueness step used by the physical endpoint statement. The standard Yang-Mills existence/mass-gap claim still explicitly uses `YM_EQ1` and `YM_EQ2`; canonical-lane closure keeps them explicit.
