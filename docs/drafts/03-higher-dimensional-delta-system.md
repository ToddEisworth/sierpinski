# 3. The Higher-Dimensional Delta-System

## The support family

For each \(s\in[B]^{\leq3}\), fix a support \(b_s\subseteq\delta\). Put

\[
P_s=\{p\in P:\operatorname{dom}(p)\subseteq b_s\times\omega\}.
\]

The supports are obtained by the higher-dimensional \(\Delta\)-system and
model-thinning argument. We use the following properties.

!!! proposition "Support-system properties"

    The family \(\langle b_s:s\in[B]^{\leq3}\rangle\) may be chosen so that:

    1. if \(u\subseteq s\), then \(b_u\subseteq b_s\);
    2. for all \(s,t\in[B]^{\leq3}\),

       \[
       b_s\cap b_t=b_{s\cap t};
       \]

    3. canonically isomorphic index sets \(s,t\) induce an isomorphism

       \[
       h_{s,t}:P_t\longrightarrow P_s;
       \]

    4. the maps \(h_{s,t}\) commute with restriction to faces; and
    5. the isomorphisms carry the relevant coloring names to their
       counterparts.

Property 2 is the exact-intersection property. It is stronger than merely
saying that the supports form an ordinary \(\Delta\)-system.

## Construction

Choose a sufficiently large regular \(\chi\) and arrange elementary models

\[
N_s\prec H(\chi)
\qquad(s\in[B]^{\leq3})
\]

by the higher-dimensional \(\Delta\)-system lemma. Thin \(B\) so that models
with the same index size have the same collapse type and

\[
N_s\cap N_t\cap\delta=N_{s\cap t}\cap\delta.
\]

Set \(b_s=N_s\cap\delta\), after applying the fixed closure operation required
by the forcing. The collapse maps between isomorphic models induce the maps
\(h_{s,t}\). Their uniqueness on the common collapsed structure makes them
commute with face restrictions. By placing \(P\), \(\dot d\), and all relevant
names in the models before thinning, the same maps preserve the coloring
names. This gives Properties 1--5.

## Commutativity

Suppose \(u\subseteq t\), and let \(v\subseteq s\) be the image of \(u\) under
the canonical bijection from \(t\) to \(s\). Then

\[
h_{s,t}(p)\restriction b_v
=
h_{v,u}(p\restriction b_u)
\qquad(p\in P_t).
\tag{3.1}
\]

Consequently, copying a simplex condition and then taking a face gives the same
result as first taking the face and then copying it.

The same compatibility holds for compositions:

\[
h_{s,t}\circ h_{t,u}=h_{s,u}
\]

whenever the three canonical maps are defined.

## Invariance of the coloring name

If \(t\) and \(t'\) are canonically isomorphic triples, then the induced forcing
isomorphism identifies their color names:

\[
h_{t',t}(\dot d(t))=\dot d(t').
\tag{3.2}
\]

Thus, if \(p\in P_t\) decides

\[
p\Vdash\dot d(t)=i,
\]

then its canonical copy decides the same value for \(t'\):

\[
h_{t',t}(p)\Vdash\dot d(t')=i.
\]

## Why the higher-dimensional form is needed

Two copied triple conditions need not have disjoint supports. Their intersection
is precisely the support belonging to their common face. Therefore compatibility
of triple interiors reduces to agreement of their vertex, edge, and empty-face
data. The commuting isomorphisms guarantee that these lower-dimensional data
are copied consistently.

!!! note "Output"

    We henceforth treat the support system, exact intersections, commuting
    maps, and name invariance as fixed background data.

**Next:** [Finite Diagram Calculus](04-finite-diagram-calculus.md).
