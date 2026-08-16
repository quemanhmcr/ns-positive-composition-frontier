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

## Conjugate dephasing frontier

On finite periodic curl cutoffs, the helicity-pair amplifier
\[
\mathbb B_u=-\nu^{-1}C^{-1}A_u^\perp C^{-1}
\]
still obeys exact quadratic-heat dephasing, but the earlier trace positive-part entropy is now rejected: it overpays unstable directions not occupied by the actual state.  The corrected reduction uses an optimal isospectral gauge plus the backward conjugate density `rho_t=|y(t)><y(t)|`.  It yields an exact threshold-matched balance
\[
\boxed{r(t)-1+\text{positive FDR mismatch}
=\text{conjugate storage}+\frac1{8\nu}\int\mathfrak q_{\mathbb B}(\mathbb B_{F_E})^2dt.}
\]
The dual capacity assembles `mathbb B_F+[A_u,mathbb B]` before positivity, so Jacobi/Bianchi reduce the secular source to genuine curl-curvature/Nijenhuis order.  An affine Kelvin kill-test rules out "heat alone" as the infrared endpoint.  The finite-pump bridge is now exact: with `phi=C^2u`, `Gamma_u=|phi><phi|_g`, and `mathscr G_U=-C A_U C^{-1}=-A_U+mathcal K_U C^{-1}`, one has `mathbb B_U=nu^{-1} Sym_g(Lambda^{-2} mathscr G_U)` and
\[
\operatorname{Re}\operatorname{Tr}_g(\Gamma_u\Lambda^{-3}\mathscr G_{H_{2h}u})=-W_h.
\]
Hence the actual `Lambda^{-3}` action moment gives finite Germano pump depletion exactly.  However the current **alignment/action gap is not yet a certified smaller theorem**.  The normalized physical covariance obeys `rho_act,t=L_u rho_act+rho_act L_u^dagger-alpha rho_act` with `L_u=mathscr G_u-nu Lambda^2`; subtracting the backward conjugate flow leaves a source containing the full `mathscr G_u=-A_u+mathcal K C^{-1}`.  Thus directly estimating `rho-rho_act` can repackage the original one-step stretching problem.  Moreover the optimal `Omega_*` quotients all isospectral rotations, whereas physical action reorientation need not be free; `Lambda^{-3}` lies in `ker mathcal A_X` and an abstract finite-cutoff model has `q_B=0` while that action moment changes.  The Flow machine is therefore presently a **diagnostic/structural reduction, not yet a quantitative closure reduction**.  Its next go/no-go gate is an exact physically anchored connection/two-state duality forcing the alignment source to `mathcal K`, `N_C`, or full Bianchi/Jacobi order before positivity.  Without that identity, adding estimates to the alignment defect would be circular.  See `docs/08-dephasing-spectral-endgame.md`.
