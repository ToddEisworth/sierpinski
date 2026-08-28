# End-homogeneity

## Vocabulary 

Let $T\subseteq 2^{<\omega}$, let $n<\omega$, and let $\sigma$ be a cardinal.

An **$n$-dimensional level $\sigma$-coloring of $T$** is a function

$$
d:
\bigcup_{m<\omega}[T\cap 2^m]^n
\longrightarrow
\sigma.
$$

Thus $d$ assigns a color below $\sigma$ to each $n$-element subset of $T$
whose members all lie on the same level.

When $\sigma$ is understood, we simply call $d$ an
**$n$-dimensional level coloring** of $T$.


A direct application of the Halpern-Läuchli to a coloring of a finite power of a tree produces, in general, different strong subtrees in the different coordinates.
Thus, if we start with a $n$-dimensional level coloring $d$ of some

$$
T^n = T\times\cdots\times T
$$

then Halpern-Läuchli gives strong subtrees 

$$
T_0,\dots, T_{n-1}\subseteq T
$$

such that the corresponding level product is monochromatic.

For us, the goal will be to find a single perfect strong subtree $S\subseteq T$ such that whenever 

$$
a = \{\nu_0,\dots,\nu_{n-1}\}
$$

is an $n$-element subset of some level of $S$, the value $d(a)$ depends only the branching pattern of the nodes in $a$, in a sense we will make precise shortly.  The proof will consist of a sequence of refinements.


## End-homogeneity


An $n$-dimensional level coloring of $T$ is **end homogeneous** if whenever $\alpha<\beta$ are splitting levels of $T$ and we
are given an $n$-tuple $\nu_0,\dots, \nu_{n-1}$ from level $\beta$ on which the projection to level $\alpha$ is one-to-one, then

$$
d(\nu_0,\dots, \nu_{n-1})=d(\nu_0\upharpoonright\alpha,\dots, \nu_{n-1}\upharpoonright \alpha).
$$

The interpretation is simple: once we reach a point in the tree where the members of the tuple have been separated, then extending their ends farther up the tree will not change the color.

### End-homogeneous canonization

!!! Theorem "End-homogeneous canonization"

    Let $n<\omega$ and let $\sigma<\omega$. Suppose

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
    $$

    is an $n$-dimensional level $\sigma$-coloring of $2^{<\omega}$.

    Then there is a perfect strong subtree

    $$
    T\subseteq 2^{<\omega}
    $$

    with synchronized splitting levels such that $d$ is **end homogeneous** on $T$.



---
**Proof:**

We construct a strong subtree $T$ by fusion.  The point of the
construction is that, before declaring a finite front to be a splitting
level of $T$, we first stabilize the color of every $n$-element subset
of that front under all subsequent end extensions.

Suppose $F$ is a finite set of nodes on a common level and, for each
$\eta\in F$, we have a perfect strong tree $U_\eta$ above $\eta$.
Assume that the trees $U_\eta$ have a common infinite set of splitting
levels.

Fix

$$
a=\{\eta_0,\ldots,\eta_{n-1}\}\in[F]^n.
$$

The cones $U_{\eta_0},\ldots,U_{\eta_{n-1}}$ are pairwise disjoint.
Hence $d$ induces a coloring of their level product by

$$
(\nu_0,\ldots,\nu_{n-1})
\longmapsto
d(\nu_0,\ldots,\nu_{n-1}).
$$

Apply the synchronized Halpern--Läuchli theorem to this product.
We obtain strong subtrees of the $U_{\eta_i}$, with a common infinite
set of splitting levels, and a color $c_a<\sigma$ such that

$$
d(\nu_0,\ldots,\nu_{n-1})=c_a
$$

whenever the $\nu_i$ are chosen from a common splitting level of the
corresponding subtrees.

There are only finitely many members of $[F]^n$.  We therefore repeat
this procedure finitely many times, once for each $a\in[F]^n$.
At each step we pass to further strong subtrees.  Previously obtained
homogeneity is preserved under further thinning.  We may also thin the
remaining coordinate trees so that all of the trees continue to have
the same splitting levels.

Consequently we obtain, for every $\eta\in F$, a perfect strong subtree

$$
V_\eta\subseteq U_\eta
$$

such that the $V_\eta$ have a common infinite set $L$ of splitting
levels and, for every $a\in[F]^n$, there is a color $c_a$ satisfying

$$
d(\{\nu_\eta:\eta\in a\})=c_a
$$

whenever $\ell\in L$ and

$$
\nu_\eta\in V_\eta\cap 2^\ell
\qquad(\eta\in a).
$$

We now carry out the fusion.

Suppose a finite front $R_k$ of size $2^k$ has been constructed,
together with synchronized perfect trees above its members.  Apply the
preceding finite stabilization procedure to $R_k$.  Choose a common
splitting level $\ell_k$ of the resulting trees and, for each
$\rho\in R_k$, choose one node

$$
\eta_\rho\in V_\rho\cap2^{\ell_k}.
$$

Let

$$
F_k=\{\eta_\rho:\rho\in R_k\}.
$$

For every $a\in[R_k]^n$, if

$$
a^*=\{\eta_\rho:\rho\in a\}\in[F_k]^n,
$$

then, by the choice of $\ell_k$,

$$
d(a^*)=c_a.
$$

Moreover this value is now permanent: at every later common splitting
level, every choice of one extension above each member of $a^*$ still
has color $c_a$.  Thus

$$
d(\{\nu_\eta:\eta\in a^*\})=d(a^*)
$$

for all subsequent synchronized end extensions of $a^*$.

Each member of $F_k$ lies at a splitting level.  Choose one extension
on each of its two sides, all on a common later level, to form the next
raw front $R_{k+1}$.  Continue recursively.

The fronts

$$
F_0,F_1,F_2,\ldots
$$

form the levels of a perfect strong subtree $T\subseteq2^{<\omega}$,
with synchronized splitting levels

$$
\ell_0<\ell_1<\ell_2<\cdots.
$$

It remains to verify end homogeneity.  Let $\ell_j<\ell_k$ be splitting
levels of $T$, and let

$$
\{\nu_0,\ldots,\nu_{n-1}\}\subseteq T\cap2^{\ell_k}
$$

have pairwise distinct restrictions to $\ell_j$.  Put

$$
\eta_i=\nu_i\restriction\ell_j.
$$

When the front $F_j=T\cap2^{\ell_j}$ was constructed, the color of the
$n$-set

$$
\{\eta_0,\ldots,\eta_{n-1}\}
$$

was stabilized under every subsequent synchronized end extension.
Hence

$$
d(\nu_0,\ldots,\nu_{n-1})
=
d(\eta_0,\ldots,\eta_{n-1}).
$$

Since distinct binary sequences preserve their lexicographic order
under extension, the order requirement in the definition of end
homogeneity is automatic for the lexicographic orders.

Therefore $d$ is end homogeneous on $T$.

$$
\tag*{$\square$}
$$

---

