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

## 2. Optimal dephasing gauge (diagnostic quotient)

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

## 3. Conjugate actual-state density for the diagnostic quotient

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
This exposes the correct structural source but also shows why the direct alignment route is not acceptable: subtracting an optimal-gauge conjugate state from the physical covariance leaves inherited transport in the state equation.  Section 7 replaces that comparison by a physically anchored corotating connection; no estimate of `mathcal E_align` is used.

There are two exact obstructions to treating the present trace-one conjugate flow as already sufficient.  First, a finite-dimensional nondegenerate three-mode Cartan sanity test has daughter relative growth independent of a common small amplitude `epsilon`, while pump-energy depletion is `O(epsilon^2)`.  Hence no amplitude-free normalized-gain-to-depletion estimate can follow from Cartan homogeneity alone; an actual action/covariance weight is necessary.  Second, every Fourier-diagonal `Q=f(X)` lies in the kernel of `mathcal A_X`, so along the conjugate flow
\[
\boxed{
\frac d{ds}\operatorname{Tr}(\rho Q)
=\operatorname{Tr}(\rho[Q,\Omega_*]).}
\]
In particular `Q=Lambda^{-3}` carries the finite-energy action but receives no dephasing/FDR control.  Pure isospectral rotations can therefore reorient carrier action at zero `mathfrak q_B` cost in the abstract finite-cutoff geometry.  Any estimate charging such reorientation must use additional physical Cartan/Jacobi information, not the dephasing capacity alone.

## 7. Physical corotating connection: the anchoring test succeeds

The self-audit above identifies the problem with `Omega_*`: it is an optimal spectral quotient, not the physical transport connection.  The correct anchoring is obtained by taking only the `g`-skew part of the actual Lie transport as free rotation.  Since
\[
A_u^{\dagger_g}=-JA_uJ,
\]
set
\[
\boxed{
A_u^{\rm rot}:=\frac12(A_u+JA_uJ),\qquad
A_u^\perp:=\frac12(A_u-JA_uJ),
}
\]
so `A_u^rot` is `g`-skew, commutes with `J`, while `A_u^perp` is `g`-self-adjoint, anticommutes with `J`, and is exactly the productive strain entering `mathbb B`.  The physically anchored corotating connection is
\[
\boxed{\Omega_{\rm phys}:=-A_u^{\rm rot}.}
\]
It quotients only the metric-preserving rotation of the actual Cartan transport; the productive strain is not declared free.

This choice passes the anchoring go/no-go test exactly.  Put
\[
\mathcal R_{\rm phys}
:=\mathbb B_{F_E}-[\Omega_{\rm phys},\mathbb B]
=\mathbb B_{F_E}+[A_u^{\rm rot},\mathbb B].
\]
Because `[A_u^perp,mathbb B]` is `g`-skew,
\[
\boxed{
\mathcal R_{\rm phys}
=\operatorname{Sym}_g\!\left(\mathbb B_{F_E}+[A_u,\mathbb B]\right).}
\]
Thus inherited one-step transport has disappeared **before positivity**.  The remaining self-adjoint source is the physical symmetric compression of the full covariant Euler source.  Through the existing Sylvester relation between `mathbb B` and `mathcal K^perp`, the Bianchi-Riccati identity
\[
C(\mathcal K_{F_E}+[A_u,\mathcal K])
=-\mathcal K^2-[A_u,\mathcal N]+[A_{Cu},\mathcal K]-\mathcal N_{F_E}
\]
therefore applies before any modulus is taken.  This is a genuine algebraic reduction: no bare `A_u` remains in `mathcal R_phys`.

The material-pullback calculation explains why this is the canonical split.  If `P_t=-A_uP`, then
\[
\widetilde C=P^{-1}CP,\qquad
\partial_t\widetilde C=P^{-1}\mathcal K P,
\]
and for material vorticity `eta=P^{-1}Cu`,
\[
\partial_t\eta=-\nu\widetilde C^{\,2}\eta.
\]
However the positive helicity polarization moves by
\[
\partial_t(P^{-1}JP)=P^{-1}[A_u,J]P,
\qquad [A_u,J]J=2A_u^\perp.
\]
So a full Lagrangian pullback merely moves the dangerous one-step strain into the positive metric.  Removing only `A_u^rot` is the objective corotating version: rotation is free, strain is retained as physical work.

Fix terminal time `t` and propagate the actual terminal rank-one state by this physical connection,
\[
\boxed{
\partial_s\rho_s^t
=\nu\mathcal A_X\rho_s^t+[\Omega_{\rm phys},\rho_s^t],
\qquad \rho_t^t=|y(t)\rangle\langle y(t)|.}
\]
Because `Omega_phys` is `g`-skew, positivity and trace one are preserved backward.  Since
\[
\partial_t\mathbb B
=-\nu\mathcal A_X\mathbb B+[\Omega_{\rm phys},\mathbb B]
+\mathcal R_{\rm phys},
\]
there is the exact actual-state-compressed identity
\[
\boxed{
\frac d{ds}
\left(\operatorname{Tr}(\rho\mathbb B)-\operatorname{Tr}\rho^2\right)
=\operatorname{Tr}(\rho\mathcal R_{\rm phys})
-2\nu\mathcal D_X(\rho,\rho).}
\]
No comparison with `rho_act` is needed, so the previous alignment defect is not the new seam.

Let `Pi_0` be the finite-cutoff orthogonal projection onto `ker mathcal A_X` and write
\[
\mathcal R_0=\Pi_0\mathcal R_{\rm phys},\qquad
\mathcal R_1=(I-\Pi_0)\mathcal R_{\rm phys}.
\]
Set
\[
\delta=\mathcal D_X(\rho,\rho),\qquad
\beta=\operatorname{Tr}(\rho\mathcal R_1),\qquad
\chi=\operatorname{Tr}(\rho\mathcal R_0).
\]
If `delta=0`, then `rho` lies in `ker mathcal A_X`, hence `beta=0`.  With the convention `beta^2/delta=0` in that case, scalar completion **after actual-state compression** gives
\[
\boxed{
\beta-2\nu\delta
=\frac1{8\nu}\frac{\beta^2}{\delta}
-2\nu\delta\left(1-\frac{\beta}{4\nu\delta}\right)^2.}
\]
Therefore
\[
\boxed{
\begin{aligned}
r(t)-1
&+2\nu\int_a^t
\mathcal D_X(\rho,\rho)
\left(1-\frac{\operatorname{Tr}(\rho\mathcal R_1)}
{4\nu\mathcal D_X(\rho,\rho)}\right)^2ds\\
&=\mathcal W^{\rm phys}_{a\to t}
+\int_a^t\operatorname{Tr}(\rho\mathcal R_0)\,ds
+\frac1{8\nu}\int_a^t
\frac{\operatorname{Tr}(\rho\mathcal R_1)^2}
{\mathcal D_X(\rho,\rho)}\,ds,
\end{aligned}}
\]
where
\[
\mathcal W^{\rm phys}_{a\to t}
=\operatorname{Tr}(\rho_a^t\mathbb B(a))
-\operatorname{Tr}((\rho_a^t)^2).
\]
The positive curvature capacity is now **state weighted**.  It is no larger than the corresponding full dual heat capacity by Cauchy, but it does not pay curvature directions unused by the actual conjugate state.

For mean-zero periodic states, `Pi_0 mathbb B=Pi_0 mathbb B_{F_E}=0`.  Hence
\[
\boxed{
\mathcal R_0
=\Pi_0[A_u^{\rm rot},\mathbb B].}
\]
Thus the exact dephasing-kernel obstruction has been reduced to a zero-net-carrier, two-step `q,-q` backreaction/reorientation loop.  It is already after the physical connection and after full Jacobi/Bianchi assembly; it is not the old one-step stretching gap in new notation.

## 8. Exact critical-work / finite-pump conversion

The same physical generator gives a pointwise work-energy conversion between critical amplification and finite pump depletion.  For any divergence-free pump `U`, define
\[
\mathcal P_2(U)
:=\nu\operatorname{Tr}_g(\Gamma_u\mathbb B_U)
=\operatorname{Re}\operatorname{Tr}_g
(\Gamma_u\Lambda^{-2}\mathscr G_U),
\]
\[
\mathcal P_3(U)
:=\operatorname{Re}\operatorname{Tr}_g
(\Gamma_u\Lambda^{-3}\mathscr G_U)
=-\langle U,F_E(u)\rangle.
\]
Let
\[
\ell:=K/E,
\qquad s=(\Lambda-\ell)u.
\]
Then exactly
\[
\boxed{
\mathcal P_2(U)-\ell\mathcal P_3(U)
=\operatorname{Re}g\!\left(
\Lambda^{-3/2}(\Lambda-\ell)\phi,
\Lambda^{-3/2}\mathscr G_U\phi\right).}
\]
The two factors have the intrinsic norms
\[
\left\|\Lambda^{-3/2}(\Lambda-\ell)\phi\right\|_g
=\|s\|_2,
\]
\[
\left\|\Lambda^{-3/2}\mathscr G_U\phi\right\|_g
=\|J_UCu\|_2,
\]
so, only after the exact identity is assembled,
\[
\boxed{
|\mathcal P_2(U)-\ell\mathcal P_3(U)|
\le \|s\|_2\,\|J_UCu\|_2.}
\]
For the actual heat-depth pump `U=H_{2h}u`, `mathcal P_3(U)=-W_h`, hence
\[
\boxed{
|\mathcal P_2(H_{2h}u)+\ell W_h|
\le \|s\|_2\,\|J_{H_{2h}u}Cu\|_2.}
\]
The equality case is rigid and physically correct: if the actual energy state lies on a single `Lambda=ell` shell, then `s=0` and
\[
\boxed{\mathcal P_2(H_{2h}u)=-\ell W_h.}
\]
Thus positive critical work from a coherent low-frequency pump forces negative Germano work and therefore depletion of the finite storage `||H_hu||_2^2/2`.  The fixed affine counterexample fails here for the correct reason: that pump storage is infinite.

The pump split is also exact at operator level:
\[
\boxed{
\mathbb B_u
=\mathbb B_{H_{2h}u}+\mathbb B_{(I-H_{2h})u}
=e^{-2h\mathcal A_X}\mathbb B_u
+(I-e^{-2h\mathcal A_X})\mathbb B_u.}
\]
Hence a bad state can only avoid the finite low-pump work channel by using a dephasing-visible high-pump remainder, by having nontrivial shell-spread error `s`, or by reconfiguring/refilling through the covariant curvature source above.

## 9. Current frontier

The optimal `Omega_*` quotient remains a useful diagnostic lower capacity, but it is no longer the physical endgame gauge.  The anchoring problem itself is now resolved algebraically by `Omega_phys=-A_u^rot`: inherited transport is removed without declaring productive strain or carrier action free, and the fresh source is the state-compressed symmetric Bianchi/Jacobi curvature.

The decisive unresolved term is now narrower:
\[
\boxed{
\text{state-weighted dephasing-kernel backreaction }
\operatorname{Tr}(\rho\mathcal R_0),
\qquad
\mathcal R_0=\Pi_0[A_u^{\rm rot},\mathbb B],}
\]
together with cutoff/infrared stability of the low-pump conversion.  This kernel term is a closed two-step carrier loop, not a bare one-step strain.  The next theorem must connect its persistent favorable sign to at least one of
\[
\text{finite Germano pump depletion},\qquad
\text{state-weighted Bianchi/Nijenhuis reconfiguration},\qquad
\text{loss of carrier/shell coherence already visible to FDR}.
\]
No occurrence-wise squaring of the loop is allowed.  If this kernel term cannot be tied to the finite pump storage or to the full Bianchi/Nijenhuis source without reintroducing bare `A_u`, then a new conditional-covariance/wave-action module is genuinely required.  Cutoff/infrared packing remains a later gate, and no global-regularity claim is made.
