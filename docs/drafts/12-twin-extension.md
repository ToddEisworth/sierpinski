# 12. The Twin-Extension Lemma

## Twins

Two marked prepared positions \((x_0,a_0)\) and \((x_1,a_1)\) are **twins** if

1. \(a_0\cap a_1=a_*\) is their common root;
2. the canonical order-preserving bijection

   \[
   h:a_0\longrightarrow a_1
   \]

   fixes \(a_*\);
3. their finite skew trees, prepared tables, and interpretation data have the
   same structural type under \(h\);
4. the two diagrams agree on every face contained in \(a_*\); and
5. both use the same palette \(H\).

The corresponding petal supports are disjoint outside their prescribed
lower-dimensional intersections.

## Compatibility of the old diagrams

!!! lemma "Overlap lemma"

    The union of the two old diagrams of twin positions is a Cohen condition.

**Proof.** Let \(p_s^0\) and \(p_t^1\) be components from the two diagrams, and
suppose a coordinate \(\zeta\) belongs to both domains. Exact intersections
give

\[
\zeta\in b_s\cap b_t=b_{s\cap t}.
\]

The face \(s\cap t\) is lower-dimensional and lies in the common root data.
Coherence and twinness therefore give

\[
p_s^0(\zeta)=p_{s\cap t}(\zeta)=p_t^1(\zeta).
\]

Thus the union is a function. \(\square\)

No cross triple has yet been assigned an interior. Its absence creates missing
data, not a conflict.

## Relative amalgamation

!!! lemma "Twin-extension lemma"

    Let \((x_0,a_0)\) and \((x_1,a_1)\) be twins. Suppose \(r_i\) seals the marked
    packet of \(x_i\), and let \(s\leq r_0,r_1\). Then there are a prepared state
    \(z\) and a Cohen condition \(r\leq s\) such that

    \[
    (x_i,a_i)\sqsubseteq_\Sigma(z,a_0\cup a_1)
    \qquad(i=0,1),
    \]

    and \(r\) seals every triple from \(a_0\cup a_1\).

**Proof.** Protect \(s\) and take the compatible union of the old diagrams.
Pairs occupying different old terminal slots already split within the common
finite template. Pairs occupying corresponding copies of the same terminal
slot may split later. Lengthen the tree until all such pairs are resolved,
performing the required splitting events in their prescribed skew order.

At each event apply the relative one-split lemma. First complete the new vertex
and edge data, and then use packet completion to fill every newly created cross
triple. Each cross triple receives the value prescribed by \(H\) for its
ordered similarity type. There are only finitely many missing faces, so the
process terminates in a prepared state \(z\). The relative construction gives
a final seal \(r\leq s\). \(\square\)

## Dense form

For fixed twins, the set of Cohen conditions supporting a common prepared
extension is dense below every common extension of their old seals. This
quantifier is what allows a Cohen generic filter to contain a common twin
extension.

**Next:** [The Auxiliary Forcing](13-the-auxiliary-forcing.md).
