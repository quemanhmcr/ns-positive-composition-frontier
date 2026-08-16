# 08 — Conjugate dephasing and pump frontier

This note replaces the earlier trace-spectral endgame.  The finite-cutoff dephasing algebra survives, but positivity must be taken **after actual-state compression**.  The continuum historical estimate remains open.

Let `A_u=ad_u=[u,.]`, `J=sgn C`,
\[
A_u^\perp=\tfrac12(A_u-JA_uJ),\qquad
\mathbb B_u=-\nu^{-1}C^{-1}A_u^\perp C^{-1}.
\]
In the positive metric `g(a,b)=<Lambda^{-1}a,b>`, `mathbb B` is self-adjoint and `J mathbb B J=-mathbb B`.  Below, finite-cutoff adjoints, traces, and Hilbert-Schmidt norms are taken after `g`-orthonormalization.  After the natural heat-clock normalization the unit actual-state direction may be taken as `y=C^2u/sqrt(M_3)`, with
\[
\boxed{r=\langle y,\mathbb B y\rangle_g=\kappa/(\nu M_3),\qquad
(d/d\sigma)\log K=2(r-1).}
\]

## 1. Quadratic heat is operator dephasing

In a Fourier-helicity cutoff basis,
\[
(\mathbb B_{H_su})_{k\ell}=e^{-s|k-\ell|^2}(\mathbb B_u)_{k\ell}.
\]
With `X_j e_k=k_j e_k`, set
\[
\mathcal A_XB=\sum_{j=1}^3[X_j,[X_j,B]],\qquad
\mathcal D_X(R,S)=\langle R,\mathcal A_XS\rangle_{HS}.
\]
Then
\[
\boxed{\partial_t\mathbb B=-\nu\mathcal A_X\mathbb B+\mathbb B_{F_E(u)}.}
\]
The old trace entropy `Tr(mathbb B-I)_+^2` is not the final observable: in the `1+1` block `mathbb B=[[0,b],[b,0]]`, `y=e_+` gives actual gain `r=0` although the trace positive part is large for `b>1`.  Thus positive spectral projection before state compression overpays hypothetical directions.

## 2. Optimal dephasing gauge

Let `Z=mathbb B_{F_E}`.  Remove isospectral rotations in the dual metric of quadratic heat.  On finite cutoffs define through carrier-zero regularization
\[
\mathfrak q_{\mathbb B}(Z)^2
=\liminf_{\varepsilon\downarrow0}\inf_{\Omega^*=-\Omega}
\langle Z-[\Omega,\mathbb B],(\mathcal A_X+\varepsilon I)^{-1}
(Z-[\Omega,\mathbb B])\rangle.
\]
For a bounded-capacity convergent minimizer, the Euler-Lagrange equations give
\[
\boxed{Z=[\Omega_*,\mathbb B]+\mathcal A_XH_*,\qquad [H_*,\mathbb B]=0,}
\]
and
\[
\boxed{\mathfrak q_{\mathbb B}(Z)^2=\mathcal D_X(H_*,H_*)=\operatorname{Tr}(H_*Z).}
\]
Equivalently, after the same regularization,
\[
\boxed{\mathfrak q_{\mathbb B}(Z)^2=
\sup_{H=H^*,\,[H,\mathbb B]=0}
\{2\operatorname{Tr}(HZ)-\mathcal D_X(H,H)\}.}
\]
So Euler regeneration is split into free spectral rotation plus the true dephasing-gradient part that can change occupied gain.

## 3. Conjugate actual-state density

Fix terminal time `t` and propagate the actual pure state backward by
\[
\boxed{\partial_s\rho_s^t=\nu\mathcal A_X\rho_s^t+[\Omega_*,\rho_s^t],\qquad
\rho_t^t=|y(t)\rangle\langle y(t)|.}
\]
Backward in physical time this is dephasing plus unitary conjugation, hence `rho>=0`, `Tr rho=1`, and
\[
\partial_s\operatorname{Tr}\rho^2=2\nu\mathcal D_X(\rho,\rho).
\]
The heat and isospectral terms cancel exactly in `Tr(rho mathbb B)`.  Completing the square gives
\[
\boxed{\frac d{ds}\bigl(\operatorname{Tr}(\rho\mathbb B)-\operatorname{Tr}\rho^2\bigr)
=\frac{\mathfrak q_{\mathbb B}(Z)^2}{8\nu}
-2\nu\mathcal D_X\!\left(\rho-\frac{H_*}{4\nu},\rho-\frac{H_*}{4\nu}\right).}
\]
Thus
\[
\boxed{r(t)-1+2\nu\!\int_a^t\!\mathcal D_X\!\left(\rho_s^t-\frac{H_*}{4\nu},\rho_s^t-\frac{H_*}{4\nu}\right)ds
=\mathcal W_{a\to t}+\frac1{8\nu}\!\int_a^t\!\mathfrak q_{\mathbb B}(Z)^2ds,}
\]
where `mathcal W_{a->t}=Tr(rho_a^t mathbb B(a))-Tr((rho_a^t)^2)`.  The dangerous quantity is now the actual supercritical excess `r(t)-1`, not full operator spectrum.

## 4. Jacobi is assembled before positivity

Because `[H_*,mathbb B]=0`,
\[
\operatorname{Tr}(H_*\mathbb B_F)
=\operatorname{Tr}(H_*(\mathbb B_F+[A_u,\mathbb B])).
\]
Hence the linear term in the dual capacity may use the covariant Euler source before the supremum is taken.  With
\[
\mathcal K=[A_u,C],\qquad \mathcal N=N_C(u,\cdot),
\]
Jacobi gives
\[
\boxed{C(\mathcal K_{F_E}+[A_u,\mathcal K])
=-\mathcal K^2-[A_u,\mathcal N]+[A_{Cu},\mathcal K]-\mathcal N_{F_E}.}
\]
After the Sylvester functional calculus relating `mathbb B` to `mathcal K^perp`, the secular source therefore starts at genuine curl-curvature/Nijenhuis order.  Full cyclic structure is assembled before quadratic positivity.

## 5. Affine kill-test: heat alone is not the endpoint

For an affine base `U=Sx`, a Kelvin packet `v=a(t)e^{ik(t)\cdot x}` satisfies
\[
\boxed{k'=-S^Tk,\qquad
a'=-Sa+2k\frac{k^TSa}{|k|^2}-\nu|k|^2a.}
\]
The fixed-pump example
\[
S=\operatorname{diag}(-2\gamma,\gamma,\gamma),\quad k(0)=k_0e_2,\quad a(0)=a_0e_1
\]
has
\[
k=k_0e^{-\gamma t}e_2,\qquad
a=a_0\exp\!\left(2\gamma t-\frac{\nu k_0^2}{2\gamma}(1-e^{-2\gamma t})\right)e_1,
\]
so critical packet growth can persist while `nu int |k|^2 dt` is finite.  Therefore “Kelvin mixing always pays the endpoint” is false.  This affine pump has infinite spatial energy; finite-energy Navier-Stokes must include pump depletion/backreaction.

A useful scaling diagnostic is obtained from Bernstein:
\[
\|\nabla P_{\le q}u\|_\infty\lesssim E^{1/2}q^{5/2}.
\]
Under the model assumptions `|S|~(T-t)^(-1)` and `|k|~(T-t)^(-p)`, relative infrared coherence requires `p>2/5`, while finite viscous phase requires `p<1/2`.  Thus a heat-neutral affine loophole, if any, is forced into the narrow model wedge `2/5<p<1/2`; this is a diagnostic, not a proved closure theorem.

## 6. Exact physical-state wave-action / Germano bridge

The normalized conjugate density alone does not carry the amplitude of the physical state.  The missing amplitude can be kept without leaving the Cartan/curl structure.  Set
\[
\phi=C^2u,\qquad
\Gamma_u=|\phi\rangle\langle\phi|_g,
\qquad
\mathscr G_U:=-CA_UC^{-1}=-A_U+\mathcal K_UC^{-1},
\]
where `mathcal K_U=[A_U,C]`.  Then
\[
\boxed{\phi_t=\mathscr G_u\phi-\nu C^2\phi.}
\]
The unnormalized rank-one covariance has the exact moment ladder
\[
\boxed{
\operatorname{Tr}_g(\Gamma_u)=M_3,\qquad
\operatorname{Tr}_g(\Gamma_u\Lambda^{-2})=K,\qquad
\operatorname{Tr}_g(\Gamma_u\Lambda^{-3})=E.}
\]
Thus `Lambda^{-3}` is the finite-energy wave-action conversion that is lost when one keeps only `Tr rho=1`.

The amplifier is exactly the critical-moment symmetric part of this physical generator:
\[
\boxed{
\mathbb B_U
=\nu^{-1}\operatorname{Sym}_g(\Lambda^{-2}\mathscr G_U).}
\]
Indeed `Lambda^{-2} mathscr G_U=-C^{-1}A_UC^{-1}` and the `g`-self-adjoint part of `A_U` is `A_U^perp`.  Consequently, for every self-adjoint state `rho`,
\[
\boxed{
\nu\operatorname{Tr}_g(\rho\mathbb B_U)
=\operatorname{Re}\operatorname{Tr}_g(\rho\Lambda^{-2}\mathscr G_U).}
\]
This identifies the present conjugate amplifier as a normalized critical-work observable of the actual `C^2u` flow.

The next lower moment is exactly physical pump work.  For every divergence-free `U`,
\[
\boxed{
\operatorname{Re}\operatorname{Tr}_g(\Gamma_u\Lambda^{-3}\mathscr G_U)
=-\langle U,F_E(u)\rangle.}
\]
For a heat depth `h`, self-adjointness of `H_h` gives
\[
W_h=\langle H_hu,H_hF_E(u)\rangle
=\langle H_{2h}u,F_E(u)\rangle,
\]
so
\[
\boxed{
\operatorname{Re}\operatorname{Tr}_g
(\Gamma_u\Lambda^{-3}\mathscr G_{H_{2h}u})=-W_h.}
\]
Equivalently, the finite low-frequency pump storage obeys the exact balance
\[
\boxed{
\frac12\partial_t\|H_hu\|_2^2
+\nu\|\Lambda H_hu\|_2^2
+\operatorname{Re}\operatorname{Tr}_g
(\Gamma_u\Lambda^{-3}\mathscr G_{H_{2h}u})=0.}
\]
A fixed affine pump is excluded at exactly the right point: this storage is not finite for an infinite-energy affine field.

To couple this identity to the backward conjugate state, let
\[
\rho_{\rm act}=\Gamma_u/M_3,
\qquad
\Delta\rho_s^t=\rho_s^t-\rho_{\rm act}(s).
\]
At every fixed heat depth `h`, the exact conjugate/Germano balance is
\[
\boxed{
\frac12\partial_s\|H_hu\|_2^2
+\nu\|\Lambda H_hu\|_2^2
+M_3\operatorname{Re}\operatorname{Tr}_g
(\rho_s^t\Lambda^{-3}\mathscr G_{H_{2h}u})
=\mathcal E_{\rm align},}
\]
with the explicit alignment defect
\[
\boxed{
\mathcal E_{\rm align}
=M_3\operatorname{Re}\operatorname{Tr}_g
(\Delta\rho_s^t\Lambda^{-3}\mathscr G_{H_{2h}u}).}
\]
The defect vanishes at the terminal time but not historically.  Dropping it would identify a normalized diagnostic state with the physical action covariance and is therefore not an exact depletion argument.

The physical generator already exposes where refill/reorientation must enter:
\[
\mathscr G_u=-A_u+\mathcal K C^{-1}.
\]
The first term is inherited Lie transport; the failure of curl to follow that transport is `mathcal K C^{-1}`.  Before any modulus is taken, fresh evolution of `mathcal K` is governed by the existing Euler-curl Bianchi-Riccati identity
\[
C(\mathcal K_{F_E}+[A_u,\mathcal K])
=-\mathcal K^2-[A_u,\mathcal N]+[A_{Cu},\mathcal K]-\mathcal N_{F_E}.
\]
Thus a successful control of `mathcal E_align` has a structurally correct route back to `mathcal K`, `N_C`, and the full Jacobi source; one-step `mathcal K` must not be squared occurrence by occurrence.

There are two exact obstructions to treating the present trace-one conjugate flow as already sufficient.  First, a finite-dimensional nondegenerate three-mode Cartan sanity test has daughter relative growth independent of a common small amplitude `epsilon`, while pump-energy depletion is `O(epsilon^2)`.  Hence no amplitude-free normalized-gain-to-depletion estimate can follow from Cartan homogeneity alone; an actual action/covariance weight is necessary.  Second, every Fourier-diagonal `Q=f(X)` lies in the kernel of `mathcal A_X`, so along the conjugate flow
\[
\boxed{
\frac d{ds}\operatorname{Tr}(\rho Q)
=\operatorname{Tr}(\rho[Q,\Omega_*]).}
\]
In particular `Q=Lambda^{-3}` carries the finite-energy action but receives no dephasing/FDR control.  Pure isospectral rotations can therefore reorient carrier action at zero `mathfrak q_B` cost in the abstract finite-cutoff geometry.  Any estimate charging such reorientation must use additional physical Cartan/Jacobi information, not the dephasing capacity alone.

## 7. Self-audit: the alignment gap is not yet a certified reduction

The exact pump identity is real, but by itself it does **not** show that the remaining historical estimate is smaller than the original critical-growth problem.  The reason is visible by evolving the normalized physical covariance itself.  Put
\[
L_u=\mathscr G_u-\nu\Lambda^2,
\qquad
\alpha_u=\operatorname{Tr}_g\bigl((L_u+L_u^{\dagger_g})\rho_{\rm act}\bigr)
=\partial_t\log M_3.
\]
Since `Gamma_t=L_u Gamma+Gamma L_u^{dagger_g}`, one has the exact normalized law
\[
\boxed{
\partial_t\rho_{\rm act}
=L_u\rho_{\rm act}+\rho_{\rm act}L_u^{\dagger_g}
-\alpha_u\rho_{\rm act}.}
\]
Subtracting this from the backward conjugate equation gives
\[
\boxed{
\partial_s\Delta\rho
=\nu\mathcal A_X\Delta\rho+[\Omega_*,\Delta\rho]
+\mathcal S_{\rm align},}
\]
where
\[
\boxed{
\mathcal S_{\rm align}
=\nu\mathcal A_X\rho_{\rm act}+[\Omega_*,\rho_{\rm act}]
-L_u\rho_{\rm act}-\rho_{\rm act}L_u^{\dagger_g}
+\alpha_u\rho_{\rm act}.}
\]
Although `Delta rho_t=0`, the source `mathcal S_align(t)` is generically nonzero.  In particular it contains the full physical generator `mathscr G_u=-A_u+mathcal K C^{-1}`.  Therefore a direct estimate of `Delta rho` can simply reintroduce the original one-step stretching problem under a new name.

There is a second, related issue.  The optimal `Omega_*` is obtained by quotienting `mathbb B_F` modulo **all** isospectral commutators.  This is legitimate for instantaneous spectral deformation, but it does not make `Omega_*` the physical transport connection of `rho_act`.  The identity
\[
\operatorname{Tr}(H_*\mathbb B_F)
=\operatorname{Tr}(H_*(\mathbb B_F+[A_u,\mathbb B]))
\]
uses `[H_*,mathbb B]=0`; it does not imply `Omega_*` equals the physical skew transport.  The finite-cutoff kernel test with `q_B=0` but changing `Tr(rho Lambda^{-3})` shows that the unconstrained quotient can remove carrier reorientation which is invisible to dephasing but relevant to finite pump action.

Hence the present Flow machine is, at this stage, a **diagnostic/structural reduction, not yet a quantitative closure reduction**.  It has genuinely eliminated false routes (trace entropy, heat-only infrared closure, amplitude-free depletion) and exposed the exact finite-pump work, but the remaining alignment/reorientation theorem has not been proved smaller than the original regularity gap.

The next go/no-go test must therefore occur **before** any estimate of `mathcal E_align`: derive a physically anchored connection or a two-state duality for which inherited transport cancels exactly and for which the residual source is forced to `mathcal K`, `N_C`, or the full Bianchi/Jacobi combination before positivity.  If no such identity exists, continuing to bound `Delta rho` or adding another entropy/corrector would be circular and the Flow machine must be augmented or replaced.  Only if this anchoring succeeds should one seek the blockwise trichotomy
\[
\text{viscous/FDR loss},\qquad
\text{finite Germano pump depletion},\qquad
\text{physical carrier reconfiguration through }\mathcal K/N_C.
\]
Cutoff/infrared packing remains a separate later gate.  A global `h^{-3/2}` integration of pump storage merely reconstructs `K` and is circular.  No global-regularity claim is made.
