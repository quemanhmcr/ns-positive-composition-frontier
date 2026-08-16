# Research status

## Closed structural chain

Critical dynamics is reduced to fixed Cartan Euler current plus diagonal quadratic heat.  One-step sign monotonicity, a global `10/13` law, a full-Euler companion theorem from Jacobi alone, and a monotone radial Herglotz-phase shortcut are ruled out.  The sharp physical triangle law remains

\[
M^2F_{\log}\le Q_\triangle.
\]

## Current frontier

The minimal critical action is

\[
\boxed{
\mathcal A_K=\frac{\kappa^2}{KM_3},\qquad
(\log K)'=\frac1{2\nu}\left[\mathcal A_K-
\frac{(\kappa-2\nu M_3)^2}{KM_3}\right].
}
\]

For `H_s=e^{-s Lambda^2}`, the covariance stress

\[
\tau_s=H_s(u\otimes u)-H_su\otimes H_su\succeq0
\]

obeys the exact Germano cocycle and Loewner heat law.  They produce an intrinsic positive cost `mathfrak C(u)` satisfying

\[
\boxed{\mathcal A_K\le (2\sqrt{2\pi})^{-1}\,\mathfrak C(u)/M_3.}
\]

## Remaining theorem

It is sufficient to prove

\[
\boxed{\int_0^T\mathfrak C(u(t))/M_3(t)\,dt<\infty.}
\]

Scale composition is already positive; the sole current seam is cutoff-independent control of **physical-time covariance regeneration toward zero heat depth** by the actual Cartan/Jacobi current.  Energy dissipation alone is insufficient by scaling.  No global-regularity claim is made until this estimate is proved.

## Sharpened torsion/conjugate route

A new exact full-state sharpening is

\[
\boxed{2\kappa=\langle u,N_J(u,\Lambda u)\rangle,\qquad
\mathcal A_K\le \mathcal T_J:=
\frac{\|\Lambda^{-1/2}N_J(u,\Lambda u)\|_2^2}{4M_3}.}
\]

The Cartan strain `S_u=[J_u,C]` satisfies `F_E=S_u u`; its heat incompatibility is expressed by the curl-Nijenhuis tensor `N_C`.  On backward heat tents, an adjoint/conjugate equation removes the inherited residual term `DF_E(U_s) R_s` exactly, leaving only fresh two-step regeneration and Euler/heat curvature.  Thus `int T_J dt < infinity` is a new sufficient **candidate route**, not a proved estimate.  See `docs/07-torsion-conjugate-frontier.md`.

## Physical corotating dephasing frontier

The optimal isospectral gauge remains an exact diagnostic quotient but is no longer used as the physical endgame connection: it can quotient carrier reorientation that is invisible to dephasing but relevant to finite pump action.  Split the actual Lie transport by the positive helicity metric,
\[
A_u^{\rm rot}=\tfrac12(A_u+JA_uJ),\qquad
A_u^\perp=\tfrac12(A_u-JA_uJ),
\]
and choose the canonical physical rotation
\[
\boxed{\Omega_{\rm phys}=-A_u^{\rm rot}.}
\]
Then
\[
\boxed{
\mathcal R_{\rm phys}
:=\mathbb B_{F_E}-[\Omega_{\rm phys},\mathbb B]
=\operatorname{Sym}_g(\mathbb B_{F_E}+[A_u,\mathbb B]).}
\]
Thus bare one-step transport is removed before positivity, while the productive strain is not declared free.  Full Jacobi/Bianchi structure therefore enters before actual-state compression.

For the backward terminal actual state driven by dephasing plus `Omega_phys`, let `Pi_0` project onto `ker mathcal A_X`, `R_0=Pi_0 R_phys`, `R_1=(I-Pi_0)R_phys`, `delta=D_X(rho,rho)`, and `beta=Tr(rho R_1)`.  The exact scalar completion after state compression is
\[
\boxed{
\beta-2\nu\delta=\frac{\beta^2}{8\nu\delta}
-2\nu\delta\left(1-\frac{\beta}{4\nu\delta}\right)^2,}
\]
with `beta^2/delta=0` when `delta=0`.  Hence the positive curvature capacity is state weighted rather than a full operator trace cost.  For mean-zero periodic states,
\[
\boxed{\mathcal R_0=\Pi_0[A_u^{\rm rot},\mathbb B],}
\]
so the only exact dephasing-kernel seam is a zero-net-carrier two-step backreaction/reorientation loop, not the original one-step stretching gap.

The finite-pump conversion is also exact.  With `phi=C^2u`, `Gamma=|phi><phi|_g`, `ell=K/E`, and
\[
\mathcal P_2(U)=\nu\operatorname{Tr}_g(\Gamma\mathbb B_U),\qquad
\mathcal P_3(U)=-\langle U,F_E(u)\rangle,
\]
one has
\[
\boxed{
|\mathcal P_2(U)-\ell\mathcal P_3(U)|
\le \|(\Lambda-\ell)u\|_2\,\|J_UCu\|_2.}
\]
For `U=H_{2h}u`, `mathcal P_3=-W_h`; on an exact single shell the error vanishes and positive critical work forces finite Germano pump depletion.  The affine fixed-pump loophole fails because its pump storage is infinite.  The current decisive gate is to control the state-weighted kernel loop by finite pump depletion, full Bianchi/Nijenhuis reconfiguration, or FDR-visible loss of coherence, without occurrence-wise squaring.  Cutoff/infrared packing remains separate.  See `docs/08-dephasing-spectral-endgame.md`.
