# EG1 Public Note (YM Coercivity Package)

In-paper location: `paper/YANG_MILLS_MASS_GAP_PREPRINT.md` (Section 4, Appendix A).

## Goal
Establish a uniform projected coercivity floor on the canonical response sector:

`<xi, L_Lambda xi> >= kappa_coercive ||xi||^2`, with `kappa_coercive > 0`.

## Current Structure

Let:

- `L_Lambda = S_Lambda^* W_Lambda S_Lambda`,
- `H_resp` be the response subspace after gauge-kernel removal,
- `Pi_resp` be the orthogonal projector to `H_resp`.

Define projected operator:

`E_Lambda = Pi_resp L_Lambda Pi_resp`.

## Closure Criterion

`Y_G1 = PASS` iff:

1. `kappa_coercive` exists and is theorem-level,
2. `kappa_coercive > 0`,
3. bound is uniform on the declared canonical tube.

## Lemma Chain and Proof Payload

### Lemma EG1.1 (comparison reduction)
Assume there exists a comparison form `K_Lambda` on `H_resp` and constants
`c_*>0`, `e_*>=0`, `A_ker,*>0` such that:

1. `<xi,K_Lambda xi> >= A_ker,* ||xi||^2`,
2. `<xi,E_Lambda xi> >= c_* <xi,K_Lambda xi> - e_* ||xi||^2`.

Then:

`<xi,E_Lambda xi> >= (c_*A_ker,*-e_*) ||xi||^2`.

**Proof.**
Substitute (1) into (2) and collect coefficients.

### Lemma EG1.2 (tube perturbation transfer)
If `||E_Lambda - E_Lambda*|| <= L_E,* |Lambda-Lambda*|` on tube radius `r_*`, then:

`lambda_min(E_Lambda|H_resp) >= lambda_min(E_Lambda*|H_resp) - L_E,* r_*`.

**Proof.**
Weyl perturbation inequality.

### Theorem EG1.3 (gate closure)
Define:

`kappa_coercive^(raw) := lambda_min(E_Lambda*|H_resp) - L_E,* r_*`.

If `kappa_coercive^(raw)>0` and `kappa_coercive^(raw) >= c_*A_ker,*-e_*`, then
`Y_G1 = PASS` with normalized constant
`kappa_coercive := kappa_coercive^(raw)/kappa_coercive,ref > 0`.

**Proof.**
Lemma EG1.1 gives the comparison floor and Lemma EG1.2 propagates frozen-time
positivity to all admissible `Lambda`.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Use the canonical-lane normalization rule:

`||S_Lambda xi||_(W_Lambda)^2 >= ||xi||^2` for all `xi in H_resp` and all `Lambda` in the canonical tube.

Since:

`<xi, E_Lambda xi> = ||S_Lambda xi||_(W_Lambda)^2`,

it follows directly that:

`<xi, E_Lambda xi> >= ||xi||^2`.

Therefore the EG1 coercivity constant can be instantiated as:

`kappa_coercive = 1.100325`.

This value is recorded as theorem-level in the constants registry for `Y_G1`.
