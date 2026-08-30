# 2. Codes and Similarity Types

## Coding the ordinals

Fix an injection

\[
F:B\longrightarrow 2^\omega.
\]

For distinct \(\alpha,\beta\in B\), write

\[
\Delta(\alpha,\beta)
=
\left|F(\alpha)\wedge F(\beta)\right|,
\]

where \(x\wedge y\) is the longest common initial segment of \(x\) and \(y\).
We assume that every basic open set used by the construction contains
uncountably many members of \(F[B]\). Consequently, after finitely many points
or Cohen coordinates have been excluded, a new point can still be chosen in
any permitted cone.

A basic cone \([\eta]\subseteq2^\omega\) with this property is called
**\(B\)-rich**.

!!! definition "Resolution"

    A finite set \(a\subseteq B\) is **resolved at height \(m\)** if the strings

    \[
    \{F(\alpha)\restriction m:\alpha\in a\}
    \]

    are pairwise distinct.

Once \(a\) is resolved, its finite meet structure is visible below \(m\).

## Strong similarity

Let \(a,b\subseteq B\) be finite and carry their increasing enumerations from
the order on \(B\). They have the same **ordered strong similarity type at
height \(m\)** if the bijection carrying the \(i\)-th member of \(a\) to the
\(i\)-th member of \(b\) preserves

- the initial-segment and meet relations among their \(F\)-codes;
- lexicographic order;
- the actual lengths of all relevant meets; and
- the common resolution height \(m\).

We write

\[
a\equiv^{m}_{\mathrm{str}} b.
\]

The equivalence class of \(a\) is denoted

\[
\operatorname{sstp}_m(F[a]).
\]

Strong similarity is the natural equivalence relation for the forcing
isomorphisms: once the exact splitting levels are fixed, canonical support
isomorphisms carry one resolved configuration to the other.

## Similarity

Two ordered finite configurations have the same **ordered similarity type** if
the corresponding bijection preserves their finite meet tree, lexicographic
order, and the relative ordering and equality pattern of the splitting events,
but not their numerical levels. Write

\[
\operatorname{simtp}_{\mathrm{ord}}(F[a])
\]

for this type.

Thus strong similarity remembers the precise splitting levels, while
similarity remembers only the combinatorial shape.

For an unordered triple of branches in a skew binary tree, there are two meet
patterns: either the left pair or the right pair separates last. Comparing the
order on \(B\) with lexicographic order contributes a permutation in \(S_3\).
Hence there are at most

\[
2\cdot 3!=12
\]

ordered similarity types of triples.

## The two canonization levels

The support isomorphisms first give conditions whose decisions depend on
ordered strong similarity. The skew-tree game then arranges a fixed palette

\[
H:\operatorname{Typ}^{\mathrm{ord}}_3\longrightarrow r
\]

such that every triple retained by the construction is decided according to
its ordered similarity type. The auxiliary forcing preserves this palette; it
does not perform an additional canonization.

**Next:** [The Higher-Dimensional Delta-System](03-higher-dimensional-delta-system.md).
