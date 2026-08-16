# 08 — Conjugate dephasing and pump frontier

This note replaces the earlier trace-spectral endgame.  The finite-cutoff dephasing algebra survives, but positivity must be taken **after actual-state compression**.  The continuum historical estimate remains open.

Let `A_u=ad_u=[u,.]`, `J=sgn C`,
\[
A_u^\perp=\tfrac12(A_u-JA_uJ),\qquad
\mathbb B_u=-\nu^{-1}C^{-1}A_u^\perp C^{-1}.
\]
In the positive metric `g(a,b)=<Lambda^{-1}a,b>`, `mathbb B` is self-adjoint and `J mathbb B J=-mathbb B`.  Below, finite-cutoff adjoints, traces, and Hilbert-Schmidt norms are taken after `g`-orthonormalization.  After the natural heat-clock normalization there is a unit actual-state direction `y` with
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

## 6. Current frontier

The next module is not a new global flow.  It is a **state-weighted pump-depletion balance** coupling the conjugate density to the existing Germano stress work.  A bad critical block must be paid by actual viscous/FDR loss, depletion of a finite low-frequency pump, or curvature capacity required to refill/reorient that pump.  The remaining tasks are to derive that intrinsic pump balance, prove cutoff/low-frequency stability of the optimal capacity, and then pack the resulting bad blocks.  No global-regularity claim is made.
