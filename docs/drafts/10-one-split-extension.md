# 10. The One-Split Extension Lemma

## Statement

!!! lemma "Relative one-split extension"

    Let \(x\) be a prepared position. Suppose Player II supplies a coherent
    strengthening of its proper-face data and a finite Cohen condition \(r\)
    compatible with the current sealed packet. Then Player I can construct a
    prepared position \(y\) such that:

    1. \(x\sqsubseteq_\Sigma y\);
    2. \(T_y\) performs the next permitted skew split;
    3. the new diagram absorbs Player II's strengthening;
    4. there is a Cohen condition \(r'\leq r\) sealing all represented triples
       in \(y\); and
    5. every triple in \(y\) is decided according to the fixed palette \(H\).

    The split may be placed in any currently permitted \(B\)-rich cone and
    above any prescribed finite resolution height.

## Proof

### Absorb the boundary data

Use finite absorption to propagate Player II's proper-face strengthening
through the current diagram. Treat the restrictions of \(r\) to the relevant
supports in the same way. Since Player II's move is coherent, these
prescriptions agree on all intersections.

All previously decisive triple conditions remain decisive with their old
values.

### Choose a fresh branch

Let \(C\) be the unused cone designated by preparation. The condition \(r\) and
the current diagram mention only finitely many coordinates and exclude only
finitely many members of \(B\). Choose

\[
\alpha\in B
\]

whose code lies in \(C\), avoids these finite obstructions, and is above any
prescribed ordinal bound.

Lengthen the terminal nodes until \(F(\alpha)\) is separated from the old
branches, and place the new splitting event at the next permitted skew level.
No old meet or splitting relation is changed.

### Extend the interpretation system

Raise the resolution beyond all newly visible splitting levels. Apply the
resolution-extension lemma to copy the old interpretation system to the new
height and to incorporate the strengthened lower-dimensional data.

The prepared face tables supply coherent boundaries for the new vertex, edge,
and mixed-triple faces. These tables were chosen so that each new triple type
has an interior deciding the value prescribed by \(H\).

### Capture the new packet

There are only finitely many triples involving the newly introduced branch.
Apply packet completion to all of them simultaneously. Exact intersections
show that the new interiors meet the old diagram only through already coherent
proper faces.

Take a common Cohen extension \(r'\leq r\) of the completed finite packet. A
final finite absorption step restores all preparation requirements for the next
round. The resulting position \(y\) has the required properties. \(\square\)

## Promotion form

The same argument may be iterated finitely many times. Hence, given a prepared
position \(x\), a finite kept set \(a\), \(r\leq\operatorname{seal}_x(a)\), a
bound \(\xi<\omega_1\), and \(k<\omega\), every \(s\leq r\) has an extension
\(r'\leq s\) supporting a prepared extension \(y\) such that

\[
\operatorname{rank}(T_y)\geq k
\]

and \(y\) contains a new kept point \(\alpha>\xi\).

This relative promotion statement is the density lemma used by the forcing.

**Next:** [The Winning Strategy](11-winning-strategy.md).
