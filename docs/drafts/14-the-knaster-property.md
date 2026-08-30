# 14. The Knaster Property

Recall that a forcing is **Knaster** if every uncountable family of conditions
has an uncountable pairwise compatible subfamily.

## The ground forcing

!!! theorem "Ground Knaster theorem"

    The forcing \(Q^*\) is Knaster.

**Proof.** Let

\[
q_\xi=(r_\xi,y_\xi,f_\xi)
\qquad(\xi<\omega_1)
\]

be conditions. Apply the \(\Delta\)-system lemma and finite-type thinning so
that:

- the domains of the \(f_\xi\)'s form a \(\Delta\)-system and the functions
  agree on its root;
- all finite ordinal data occurring in \(r_\xi\), the prepared tables, and the
  marked diagram form a \(\Delta\)-system and agree on their root;
- all finite skew trees, marked fronts, prepared tables, and diagrams have the
  same collapsed structural type; and
- the canonical maps between two conditions fix the common root.

There are only countably many finite collapsed types, so the resulting family
is still uncountable. Any two marked states are twins.

Fix \(\xi<\eta\) in the thinned family. The function

\[
f_\xi\cup f_\eta
\]

is well defined, and the Cohen conditions have a common extension

\[
s=r_\xi\cup r_\eta.
\]

Apply the relative twin-extension lemma below \(s\). It gives a prepared state
\(z\) containing both marked states and a condition

\[
r\leq s,\operatorname{seal}_z
  \bigl(a_{f_\xi}\cup a_{f_\eta}\bigr).
\]

Then

\[
(r,z,f_\xi\cup f_\eta)
\]

extends both \(q_\xi\) and \(q_\eta\). Hence the thinned family is pairwise
compatible. \(\square\)

## The quotient forcing

The complete projection alone gives the ccc of the quotient, but the relative
twin lemma gives the stronger conclusion we need.

!!! theorem "Quotient Knaster theorem"

    \[
    P\Vdash Q_G\text{ is Knaster}.
    \]

**Proof.** Let \(p\in P\) force that

\[
\langle\dot q_\xi:\xi<\omega_1\rangle
\]

is a sequence in \(Q_G\). Choose \(p_\xi\leq p\) deciding

\[
\dot q_\xi=(r_\xi,y_\xi,f_\xi),
\]

and strengthen so that \(p_\xi\leq r_\xi\). Thus

\[
(p_\xi,y_\xi,f_\xi)
\]

is a quotient strengthening of the decided condition whenever
\(p_\xi\in G\).

Thin exactly as in the ground proof. Let \(p_*\) be the common Cohen root. The
petals of the \(p_\xi\)'s are pairwise disjoint, so

\[
p_*\Vdash
I=\{\xi:p_\xi\in G\}
\text{ is unbounded in }\omega_1.
\tag{14.1}
\]

Indeed, every extension of \(p_*\) meets only finitely many petals and is
compatible with some \(p_\xi\) arbitrarily far out.

If \(\xi,\eta\in I\), then \(p_\xi\cup p_\eta\in G\). By the dense form of the
twin-extension lemma, the set of Cohen conditions supporting a common prepared
extension of the two twins is dense below \(p_\xi\cup p_\eta\). The generic
filter \(G\) contains one such condition. Therefore the corresponding two
quotient conditions are compatible.

Thus \(p_*\) forces that the conditions indexed by the unbounded set \(I\) are
pairwise compatible. \(\square\)

!!! note "Where compatibility enters"

    The \(\Delta\)-system argument handles the explicit Cohen coordinates.
    Isomorphism of the lower-dimensional diagrams handles their overlaps. The
    twin-extension lemma supplies only the previously absent cross faces and
    triple interiors.

**Next:** [Density and the Generic Object](15-density-and-the-generic-object.md).
