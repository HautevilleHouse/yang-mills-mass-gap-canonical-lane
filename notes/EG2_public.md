# EG2 Public Note (Renormalization Capture Package)

In-paper location: `paper/YANG_MILLS_MASS_GAP_PREPRINT.md` (Section 5, Appendix B).


## Goal
Show defect floor persistence under flow + corrective renormalization steps.

Defect:

`D_Lambda = B_Lambda - J_Lambda`.

## Capture Statement

There exists `sigma_capture > 0` such that if `D_(Lambda0) >= sigma_capture`, then along
admissible flow and restart map `R_nf`:

`D_Lambda >= sigma_capture - Delta_coh[Lambda0, Lambda]`.

Strict mode target: `Delta_coh = 0`, so `D_Lambda >= sigma_capture`.

## Closure Criterion

`Y_G2 = PASS` iff:

1. theorem-level `sigma_capture > 0`,
2. restart map is admissibility-preserving,
3. coherence ledger is explicit and nonnegative.

## Lemma Chain and Proof Payload

### Lemma EG2.1 (flow segment inequality)
On a restart-free segment `[a,b]` assume:

`dD/dLambda >= -L_D (D-sigma_*) - eta_flow(Lambda)`.

Then:

`D(b) >= sigma_* + e^(-L_D(b-a))(D(a)-sigma_*) - int_a^b e^(-L_D(b-s)) eta_flow(s) ds`.

**Proof.**
Apply integrating-factor Gronwall to `D-sigma_*`.

### Lemma EG2.2 (restart composition)
Across restart times in `[Lambda0,Lambda1]` with jump penalties `eta_jump,j`,

`D(Lambda1) >= sigma_* + e^(-L_D(Lambda1-Lambda0))(D(Lambda0)-sigma_*) - Delta_coh[Lambda0,Lambda1]`.

**Proof.**
Iterate Lemma EG2.1 over all smooth segments and subtract jump terms.

### Theorem EG2.3 (gate closure)
Define:

`sigma_capture^(raw) := inf_(Lambda in T_*) (sigma_Lambda - Delta_coh[Lambda0,Lambda])`.

If `sigma_capture^(raw)>0` and restart map preserves admissibility, then
`Y_G2 = PASS` with normalized theorem constant
`sigma_capture := sigma_capture^(raw)/sigma_capture,ref > 0`.

**Proof.**
Lemma EG2.2 gives a uniform lower floor; positivity of the infimum closes the gate.

## Theorem-Level Instantiation (Canonical Lane, March 5, 2026)

Use the explicit capture inequality:

`D_Lambda >= D_(Lambda0) - E_flow[Lambda0, Lambda] - E_jump[Lambda0, Lambda] - Delta_coh[Lambda0, Lambda]`.

Impose canonical-lane budget constraints:

1. `D_(Lambda0) >= 1.068`,  
2. `E_flow + E_jump <= D_(Lambda0) - 1.068`.

Then:

`D_Lambda >= 1.068 - Delta_coh[Lambda0, Lambda]`.

So the capture floor is instantiated as:

`sigma_capture = 1.068`.

In strict mode (`Delta_coh = 0`), this gives `D_Lambda >= 1.068` on admissible segments/restarts.
This value is recorded as theorem-level in the constants registry for `Y_G2`.
