# 7. Strong-Similarity Interpretation Sequences

## Interpretation systems

For \(m<\omega\), let \(I_m\) consist of the \(m\)-resolved subsets of \(B\) of
size at most three. An **interpretation system at height \(m\)** is a family

\[
x=\langle p_s^x:s\in I_m\rangle
\]

such that:

1. \(p_s^x\in P_s\);
2. if \(u\subseteq s\), then

   \[
   p_s^x\restriction(b_u\times\omega)=p_u^x;
   \]

3. if \(s\equiv^m_{\mathrm{str}}t\), then

   \[
   p_s^x=h_{s,t}(p_t^x);
   \]

4. every component indexed by a triple decides its color.

Although the displayed family is large, it is determined by finitely many type
representatives at height \(m\).

Let \(R_m\) be the class of prepared interpretation systems at height \(m\).
For systems \(x\in R_m\) and \(y\in R_n\), write

\[
x\sqsubseteq y
\]

if \(m\leq n\) and every component of \(y\) refining old data strengthens the
corresponding component of \(x\). Thus \(y\) is the later, stronger system.

## Increasing the resolution

!!! lemma "Resolution extension"

    If \(x\in R_m\) and \(n>m\), then there is \(y\in R_n\) such that

    \[
    x\sqsubseteq y.
    \]

    The extension may simultaneously absorb finitely many coherent
    lower-dimensional strengthenings.

**Proof.** Copy the old face data to the refined type complex at height \(n\).
Use finite absorption to incorporate the prescribed strengthenings. There are
only finitely many new strong similarity types at height \(n\); apply the
canonical seed lemma to make their triple representatives decisive, and then
copy them equivariantly. Packet completion restores preparation. \(\square\)

## Persistence

If \(x\sqsubseteq y\), \(t\) was already resolved in \(x\), and

\[
p_t^x\Vdash\dot d(t)=i,
\]

then

\[
p_t^y\Vdash\dot d(t)=i.
\tag{7.1}
\]

Thus increasing the resolution never changes an earlier decision.

## Interpretation sequences

An **interpretation sequence** is an increasing sequence

\[
x_0\sqsubseteq x_1\sqsubseteq x_2\sqsubseteq\cdots,
\qquad x_m\in R_{n_m},
\]

with \(n_m<n_{m+1}\). It need not be fixed globally before the construction.
The resolution-extension lemma allows the sequence to be built along the
actual history of the game, after Player II's finite coherent strengthening is
known.

For every finite set \(a\subseteq B\), some sufficiently late system resolves
\(a\), and finite capture then gives one condition deciding every triple from
\(a\) according to ordered strong similarity.

!!! note "Output"

    The interpretation layer is coherent, decisive, stable under later
    resolution, and flexible enough to absorb finite information supplied
    during the game.

**Next:** [Skew-Tree Templates](08-skew-tree-templates.md).
