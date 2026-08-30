# 4. Finite Diagram Calculus

## Coherent diagrams

Let \(a\subseteq B\) be finite, and let

\[
I(a)=[a]^{\leq3}.
\]

This is a downward-closed finite face complex. A **coherent diagram on \(a\)** is
a family

\[
\bar p=\langle p_s:s\in I(a)\rangle
\]

such that

\[
p_s\in P_s
\]

and, whenever \(u\subseteq s\),

\[
p_s\restriction(b_u\times\omega)=p_u.
\tag{4.1}
\]

The conditions indexed by sets of size \(0,1,\) and \(2\) are the
**lower-dimensional data**. Conditions indexed by triples are the
**interiors**.

## Compatible union

!!! lemma "Diagram union"

    If \(\bar p\) is a coherent finite diagram, then

    \[
    \bigcup_{s\in I(a)}p_s
    \]

    is a condition in \(P\).

**Proof.** Suppose a coordinate \(\xi\) belongs to the domains of \(p_s\) and
\(p_t\). Exact intersections give

\[
\xi\in(b_s\cap b_t)\times\omega
=(b_{s\cap t}\times\omega).
\]

By coherence,

\[
p_s(\xi)=p_{s\cap t}(\xi)=p_t(\xi).
\]

Thus the union is a function. It is finite because the diagram is finite.
\(\square\)

The same proof applies to two diagrams that agree on every common face. This is
the compatibility fact later used for twins.

## Propagating a strengthening

!!! lemma "Finite absorption"

    Let \(\bar p\) be coherent, let \(w\in I(a)\), and suppose

    \[
    q\leq p_w,
    \]

    Then \(\bar p\) has a coherent strengthening \(\bar p'\) with
    \(p'_w\leq q\). Finitely many coherent face strengthenings may be absorbed
    simultaneously.

**Proof.** For \(u\in I(a)\), define

\[
p'_u
=
p_u\cup
\bigl(q\restriction(b_{u\cap w}\times\omega)\bigr).
\]

The two terms agree on their common domain because \(q\leq p_w\) and the old
diagram is coherent. If \(u\subseteq v\), exact intersections give

\[
p'_v\restriction(b_u\times\omega)=p'_u.
\]

For \(u=w\), we obtain \(p'_w=q\). Thus \(\bar p'\) is the required coherent
strengthening. Iterate this construction to absorb finitely many
strengthenings; strengthening preserves every earlier color decision.
\(\square\)

## Extending the index complex

If \(a\subseteq a'\) and a coherent diagram is given on \(I(a)\), its old data
may first be copied to the corresponding faces of \(I(a')\). New proper faces
are then chosen coherently, and new triple interiors are filled last. Because
the complex is finite, this can be performed one face at a time.

!!! lemma "Finite diagram extension"

    A coherent diagram on \(I(a)\), together with coherent prescriptions on
    finitely many new faces of \(I(a')\), extends to a coherent diagram on all
    of \(I(a')\), provided each new triple interior can be completed over its
    prescribed boundary.

The next two files supply exactly this completion property for decisive triple
conditions.

**Next:** [Canonical Seeds](05-canonical-seeds.md).
