# 5. Canonical Seeds

## Type complexes at a fixed height

Fix \(m<\omega\). A finite set \(s\subseteq B\) is **\(m\)-resolved** if its
\(F\)-codes have distinct restrictions to \(m\). Among sets of size at most
three there are only finitely many ordered strong similarity types at height
\(m\).

The **type complex** \(U_m\) consists of these types, ordered by taking faces.
Thus a triple type in \(U_m\) has three pair types, three vertex types, and the
empty type below it.

Canonical support isomorphisms identify all realizations of a fixed member of
\(U_m\).

## Seeds

!!! definition "Canonical seed"

    A canonical seed at height \(m\) is a coherent assignment

    \[
    \sigma\longmapsto p^m_\sigma
    \qquad(\sigma\in U_m)
    \]

    satisfying:

    1. \(p^m_\sigma\) lives on the abstract support belonging to \(\sigma\);
    2. restriction to a face agrees with the condition assigned to that face;
    3. canonical copies of \(p^m_\sigma\) give the conditions for all actual
       realizations of \(\sigma\); and
    4. if \(\rho\) is a triple type, then \(p^m_\rho\) decides the color of a
       representative triple.

Write \(C_m(\rho)<r\) for the value decided by \(p^m_\rho\).

The seed is **prepared** if it also records the coherent face data and unused
cones required for a subsequent finite extension.

## Existence

!!! lemma "Canonical seed lemma"

    Every coherent assignment on the proper faces of \(U_m\) has a prepared
    canonical extension in which every triple type is decisive.

**Proof.** Enumerate the finitely many triple types as

\[
\rho_0,\ldots,\rho_{N-1}.
\]

Suppose the types before \(\rho_i\) have been treated. Realize \(\rho_i\) by an
actual triple \(t_i\). The already fixed proper-face conditions form a single
boundary condition on \(b_{t_i}\). Strengthen it to a condition deciding

\[
\dot d(t_i)=C_m(\rho_i).
\]

Use finite absorption to propagate any strengthened boundary data through the
existing diagram. Then copy the resulting full-simplex condition to every
realization of \(\rho_i\) using the canonical support isomorphisms.

Commutativity with face restrictions preserves coherence. Distinct interiors
can intersect only on their proper faces, where agreement has already been
arranged. After finitely many steps every triple type is decisive. A final
finite absorption step supplies the preparation data. \(\square\)

## Equivariance

If \(t,t'\) realize the same ordered strong similarity type \(\rho\), then

\[
p^m_{t'}=h_{t',t}(p^m_t)
\]

and both conditions decide the same color \(C_m(\rho)\). This is the first
canonization: decisions depend on ordered strong similarity, not on the
particular ordinals realizing the type.

!!! note "Output"

    At every finite resolution height we can choose a coherent, decisive, and
    canonically copyable system of representatives. The choice may be made
    relative to previously fixed lower-dimensional data.

**Next:** [Packet Completion and Finite Capture](06-packet-completion-and-finite-capture.md).
