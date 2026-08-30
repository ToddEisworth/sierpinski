# 8. Skew-Tree Templates

## Finite skew trees

A **finite skew tree of rank \(k\)** is the image of a strong embedding

\[
e:2^{\leq k}\longrightarrow 2^{<\omega}
\]

that preserves initial segments, the two immediate-successor directions, and
lexicographic order, and whose branching nodes occur at pairwise distinct
ambient levels. Nonbranching extensions may be inserted between successive
branching levels.

Fix, for every \(k\), a prescribed abstract template \(T_k^*\) listing these
branching events in their permitted order. An **allowed finite skew tree** is a
strong copy of some \(T_k^*\). An allowed extension lengthens terminal nodes and
performs the next prescribed splitting events without changing the old meet
structure.

The union of an increasing sequence of allowed templates of unbounded rank is
a strong skew copy of \(2^{<\omega}\).

## Separated sets on a front

Let \(T\) be resolved at height \(m\), and put

\[
B_T=\{\alpha\in B:F(\alpha)\restriction m
\text{ lies on the terminal front of }T\}.
\]

A finite \(a\subseteq B_T\) is **separated by \(T\)** if distinct members of
\(a\) occupy distinct terminal nodes. Every triple from a separated set has its
meet configuration displayed by \(T\).

## The similarity palette

Let \(\operatorname{Typ}^{\mathrm{ord}}_3\) be the finite set of ordered
similarity types of triples in a skew tree. Fix a map

\[
H:\operatorname{Typ}^{\mathrm{ord}}_3\longrightarrow r.
\]

A prepared tree position is **\(H\)-invariant** if every represented triple
\(t\) is sealed by a condition forcing

\[
\dot d(t)=H\bigl(\operatorname{simtp}_{\mathrm{ord}}(F[t])\bigr).
\tag{8.1}
\]

This requirement removes dependence on the numerical splitting levels. Two
strongly different triples with the same ordered similarity type receive the
same value from \(H\).

## Prepared positions

A **prepared position** consists of

- an allowed finite skew tree \(T\);
- a prepared interpretation system at a height resolving \(T\);
- the fixed palette \(H\);
- coherent lower-dimensional tables for the next permitted split; and
- an unused \(B\)-rich cone in which that split can be realized.

Preparation is a finite extension property: after a coherent strengthening of
the proper faces, the position can be lengthened through the next prescribed
split and prepared again.

We use the finite tree Ramsey theorem in the following form: for every finite
coloring of ordered strong triple types and every target rank \(k\), a
sufficiently large finite skew template contains a rank-\(k\) subtemplate on
which the color of a triple depends only on its ordered similarity type.

!!! lemma "Initial preparation"

    There are a palette \(H\) and an \(H\)-invariant prepared position.

**Proof.** Use a sufficiently large finite skew template and color each
represented triple by the value assigned to its ordered strong similarity type
by a canonical seed. Finite tree canonization gives a skew subtemplate on which
this finite coloring depends only on ordered similarity type. Call the resulting
map \(H\). Packet completion supplies simultaneous decisive conditions, and a
final finite absorption step prepares the position for its next split.
\(\square\)

!!! note "Output"

    The tree templates specify the global combinatorial shape, while the
    interpretation systems supply the local forcing decisions. The game joins
    these two structures.

**Next:** [The Prepared-Position Game](09-the-game.md).
