# 15. Density and the Generic Object

Work in \(V[G]\), where \(G\subseteq P\) is generic, and let \(Q_G\) be the
quotient forcing.

## Adding new kept points

For \(\xi<\omega_1\), define

\[
D_\xi=
\{(r,y,f)\in Q_G:(\exists\alpha\in a_f)\,\alpha>\xi\}.
\]

!!! lemma "Promotion density"

    Every \(D_\xi\) is dense in \(Q_G\).

**Proof.** Let \(q=(r,y,f)\in Q_G\). For every \(s\leq r\), relative promotion
provides

- a fresh \(\alpha>\xi\) in a permitted cone;
- a prepared extension \(y'\) carrying the old points and \(\alpha\);
- an extension \(f'\supseteq f\) with \(f'(\alpha)=1\); and
- a Cohen condition

  \[
  s'\leq s,\operatorname{seal}_{y'}(a_{f'}).
  \]

Hence the Cohen conditions supporting such promotions are dense below \(r\).
Because \(r\in G\), the filter \(G\) contains one of them. The corresponding
\((s',y',f')\) belongs to \(D_\xi\) and extends \(q\). \(\square\)

For each \(\alpha\in B\), the set of conditions deciding \(f(\alpha)\) is also
dense: if \(\alpha\) is not selected, it may simply be assigned value \(0\).

## Lengthening the tree

For \(k<\omega\), put

\[
E_k=\{(r,y,f)\in Q_G:\operatorname{rank}(T_y)\geq k\}.
\]

The relative one-split lemma shows that every \(E_k\) is dense.

## The generic set and tree

Let \(K\subseteq Q_G\) be generic, and define

\[
A=\{\alpha\in B:(\exists(r,y,f)\in K)\ f(\alpha)=1\}
\]

and

\[
T=\bigcup\{T_y:(r,y,f)\in K\}.
\]

Because \(K\) meets every \(D_\xi\), the set \(A\) is unbounded in \(B\) and
hence has cardinality \(\aleph_1\). The Knaster property preserves
\(\omega_1\).

Because \(K\) meets every \(E_k\), the tree \(T\) has unbounded finite rank.
Structural extension and directedness of \(K\) imply that \(T\) is a strong
skew copy of \(2^{<\omega}\). Every \(F(\alpha)\), \(\alpha\in A\), follows a
branch through \(T\).

## Every generic triple is sealed

Let \(t\in[A]^3\). Choose three conditions in \(K\) witnessing that the members
of \(t\) are kept. Directedness gives one condition

\[
(r,y,f)\in K
\]

extending all three. Then \(t\subseteq a_f\), and

\[
r\leq\operatorname{seal}_y(a_f)\leq p_t^y.
\]

Since \(r\in G\), we have \(p_t^y\in G\). Therefore

\[
d(t)=H\bigl(\operatorname{simtp}_{\mathrm{ord}}(F[t])\bigr).
\tag{15.1}
\]

Thus every triple from the generic uncountable set is a kept triple and is
canonized on the generic skew tree.

**Next:** [The Final Canonization Theorem](16-final-canonization-theorem.md).
