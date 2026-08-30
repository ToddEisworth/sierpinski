# 6. Packet Completion and Finite Capture

## Packets

Let \(a\subseteq B\) be finite and resolved at height \(m\). For every
\(s\in[a]^{\leq3}\), copy the seed condition belonging to the ordered strong
similarity type of \(s\) onto the actual support \(b_s\). Denote the result by

\[
p_s^{m,a}.
\]

The family

\[
\mathcal P_m(a)=\langle p_s^{m,a}:s\in[a]^{\leq3}\rangle
\]

is the **packet on \(a\)**.

More generally, if \(x\) is a prepared interpretation system resolving a
nonempty \(a\), write

\[
\operatorname{seal}_x(a)
=
\bigcup_{s\in[a]^{\leq3}}p_s^x.
\tag{6.1}
\]

This is the **seal of \(a\) in \(x\)**.
For the empty marked set, put

\[
\operatorname{seal}_x(\varnothing)=1_P.
\]

By commutativity of the copying maps, this is a coherent diagram. In
particular, two copied triple conditions agree on every common lower face.

## Completing a packet

!!! lemma "Packet completion"

    Suppose coherent conditions have been prescribed on all proper faces of
    the triples from \(a\). Assume that these conditions extend the
    corresponding seed boundaries. Then there is a coherent strengthening

    \[
    \langle q_s:s\in[a]^{\leq3}\rangle
    \]

    in which every triple interior is decisive and has the color assigned by
    its seed type.

**Proof.** First use finite absorption to incorporate all prescribed vertex and
edge data simultaneously. Enumerate the triples from \(a\). At each step copy
the decisive representative belonging to the triple's strong similarity type,
strengthen it over the already fixed boundary, and propagate any resulting
face strengthening through the finite diagram. Exact intersections ensure that
the new interior meets the old diagram only in its boundary. \(\square\)

## Finite capture

!!! theorem "Finite capture"

    If \(a\subseteq B\) is finite and resolved at height \(m\), there is one
    Cohen condition \(q_a\) such that, for every \(t\in[a]^3\),

    \[
    q_a\Vdash
    \dot d(t)=C_m\bigl(\operatorname{sstp}_m(F[t])\bigr).
    \]

**Proof.** Complete the packet on \(a\), and put

\[
q_a=\bigcup_{s\in[a]^{\leq3}}q_s.
\]

The diagram-union lemma shows that \(q_a\in P\). Since \(q_a\) extends every
triple component, it makes all the required decisions. \(\square\)

## Relative capture

The form used later is relative to finite Cohen information. Let \(r\in P\) be
compatible with the current packet. Treat \(r\) as protected data, absorb its
restrictions to the relevant faces, and then complete the packet. This gives

\[
q\leq r,q_a.
\tag{6.2}
\]

When new vertices are being chosen, the finitely many coordinates mentioned by
\(r\) can first be avoided. The density of \(F[B]\) in the permitted cones then
provides fresh vertices for which the required packet is compatible with
\(r\).

!!! note "Output"

    Any finite resolved family of triples can be sealed simultaneously, and
    the construction can be performed below prescribed compatible Cohen
    information.

**Next:** [Strong-Similarity Interpretation Sequences](07-strong-similarity-interpretation-sequences.md).
