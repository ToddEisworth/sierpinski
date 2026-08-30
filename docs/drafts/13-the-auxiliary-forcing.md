# 13. The Auxiliary Forcing

## Marked strategy states

Fix the winning strategy \(\Sigma\) and palette \(H\). For
\(y\in\mathcal Y_\Sigma\), let

- \(T_y\) be its finite skew tree;
- \(m_y\) be its resolution height; and
- \(p_s^y\) be its interpretation condition for every represented face
  \(s\in[B]^{\leq3}\).

Put

\[
B_y=\{\alpha\in B:F(\alpha)\restriction m_y
\text{ lies on the terminal front of }T_y\}.
\]

Let \(\operatorname{fs}(y)\) consist of the finite \(a\subseteq B_y\) whose
members occupy distinct terminal nodes. For \(a\in\operatorname{fs}(y)\), set

\[
\operatorname{seal}_y(a)
=
\bigcup_{s\in[a]^{\leq3}}p_s^y.
\tag{13.1}
\]

This is a Cohen condition by the diagram-union lemma.
We use the convention

\[
\operatorname{seal}_y(\varnothing)=1_P,
\]

the empty Cohen condition.

We use a finite function \(f:B\to2\) to record membership decisions and write

\[
a_f=f^{-1}(\{1\}).
\]

The points in \(a_f\) are the **kept points**. The zero values merely prevent a
point from being selected later.

## The ground-model forcing

!!! definition "The forcing \(Q^*\)"

    A condition is a triple

    \[
    q=(r,y,f)
    \]

    such that

    1. \(y\in\mathcal Y_\Sigma\);
    2. \(f\in\operatorname{Fn}(B,2)\);
    3. \(a_f\in\operatorname{fs}(y)\); and
    4. \(r\in P\) and

       \[
       r\leq\operatorname{seal}_y(a_f).
       \]

For \(q_i=(r_i,y_i,f_i)\), put \(q_1\leq_{Q^*}q_0\) if

- \(r_1\leq_P r_0\);
- \(f_1\supseteq f_0\); and
- \((y_1,a_{f_1})\) is a structural \(\Sigma\)-extension of
  \((y_0,a_{f_0})\).

In particular, old branches, old face data, and old color decisions are
preserved. Structural extension is used here, not literal end-extension of a
play transcript.

## The Cohen projection

Define

\[
\pi:Q^*\longrightarrow P,
\qquad
\pi(r,y,f)=r.
\]

!!! lemma "Projection lemma"

    The map \(\pi\) is a complete projection.

**Proof.** It is order preserving. If \(s\leq r\), then

\[
(s,y,f)\leq(r,y,f),
\]

because

\[
s\leq r\leq\operatorname{seal}_y(a_f).
\]

Finally, an empty marked position has empty seal, so every \(s\in P\) occurs as
the projection of some condition. \(\square\)

## The quotient

Let \(G\subseteq P\) be generic. In \(V[G]\), define

\[
Q_G=Q^*/G
=
\{(r,y,f)\in Q^*:r\in G\},
\tag{13.2}
\]

with the inherited order. Standard projection theory gives

\[
Q^*\simeq P*\dot Q_G.
\]

If \((r,y,f)\in Q_G\) and \(t\in[a_f]^3\), then

\[
r\leq\operatorname{seal}_y(a_f)\leq p_t^y.
\]

Since \(r\in G\), also \(p_t^y\in G\). Thus every triple kept by a quotient
condition has its deciding interpretation condition in the Cohen generic.

**Next:** [The Knaster Property](14-the-knaster-property.md).
