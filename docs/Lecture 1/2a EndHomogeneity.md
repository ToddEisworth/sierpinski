# End-homogeneity



An $n$-dimensional level coloring of $T$ is **end homogeneous** if whenever $\alpha<\beta$ are splitting levels of $T$ and we
are given an $n$-tuple $\nu_0,\dots, \nu_{n-1}$ from level $\beta$ on which the projection to level $\alpha$ is one-to-one, then

$$
d(\nu_0,\dots, \nu_{n-1})=d(\nu_0\upharpoonright\alpha,\dots, \nu_{n-1}\upharpoonright \alpha).
$$

The interpretation is simple: once we reach a point in the tree at which the members of the tuple have been separated, then extending their ends farther up the tree does not change the color.  This is essentially the ``level-tree analogue'' of continuity for colorings of $[2^\omega]^n$.


### End-homogeneous canonization

!!! Theorem "End-homogeneous canonization"

    Let $n<\omega$ and let $\sigma<\omega$. Suppose

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
    $$

    is an $n$-dimensional level $\sigma$-coloring of $2^{<\omega}$.

    Then there is a strong subtree

    $$
    T\subseteq 2^{<\omega}
    $$

    such that $d$ is **end homogeneous** on $T$.



---
**Proof:**

We construct $T$ by a fusion argument. 

Suppose $F$ is a finite set of nodes on a common level and as well as a family $\{U_\eta:\eta\in F\}$ of strong subtrees of $2^{<\omega}$ such that

- $U_\eta$ has root $\eta$, and

- the trees $U_\eta$ have a common infinite set of splitting levels.


Given $a = \{\eta_0,\dots,\eta_{n-1}\}\in [F]^n$, we know the sets $U_{\eta_0},\dots, U_{\eta_{n-1}}$ are pairwise disjoint, and hence $d$ induces a coloring of their level product:

$$
(\nu_0,\ldots,\nu_{n-1})
\longmapsto
d(\nu_0,\ldots,\nu_{n-1}).
$$

We apply the Halpern--Läuchli theorem to this product, and this gives us for each $i<n$ a strong subtree $U_{\eta_i}^*$ of $U_{\eta_i}$ and a single color $\varsigma<\sigma$ such that

- the trees $U_{\eta_i}^*$ share a common infinite set of splitting levels, and

- $d(\nu_0,\ldots, \nu_{n-1})=\varsigma$ whenever the $\nu_i$ are chosen from a common splitting level of the corresponding subtrees.




We now iterate this through some enumeration of the finitely many members of $[F]^n$. Since the homogeneity survives further thinning, we can make sure that at each stage our strong subtrees have the same splitting levels.
At the conclusion of this process, for each $\eta\in F$ we have a strong subtree $V_\eta\subseteq U_\eta$ so that

- the trees $V_\eta$ have a common infinite set $L$ of splitting levels, and

- for each $a\in [F]^n$ there is a color $\varsigma_a$ such that 

$$
d(\{\nu_\eta:\eta\in a\})=\varsigma_a
$$

whenever $\ell\in L$ and

$$
v_\eta\in V_\eta\cap 2^\ell
$$


We now carry out the fusion.

Let $F_0=\{\emptyset\}$. Suppose $F_k$ has been constructed, with $|F_k|=2^k$, and for each $\eta\in F_k$ we have a strong subtree $U_\eta$ rooted at $\eta$, all with the same splitting levels.

For each $\eta\in F_k$, take the two immediate successors of $\eta$ in $U_\eta$, and let $R$ be the set of all these nodes. Thus $|R|=2^{k+1}$. Above each $\rho\in R$, take the corresponding cone in $U_\eta$.

Apply the finite stabilization argument to $R$ and these cones. We obtain strong subtrees $V_\rho$, $\rho\in R$, with common splitting levels, such that for every $a\in[R]^n$, the color of a choice of one node from each $V_\rho$, $\rho\in a$, is constant on their common splitting levels.

Choose one such splitting level, and for each $\rho\in R$ choose a node

$$
\eta_\rho\in V_\rho
$$

on that level. Set

$$
F_{k+1}=\{\eta_\rho:\rho\in R\},
$$

and continue above $\eta_\rho$ inside $V_\rho$.

Then $|F_{k+1}|=2^{k+1}$, and each member of $F_k$ has exactly two successors in $F_{k+1}$, one on each side. Continuing in this way gives a strong subtree

$$
T=\bigcup_{k<\omega}F_k.
$$

Moreover, when $F_k$ is constructed, every $n$-set from $F_k$ has its color fixed under all later level extensions.

Now let $j<k$, and let

$$
\{\nu_0,\dots,\nu_{n-1}\}\subseteq F_k
$$

have distinct restrictions to the level of $F_j$. Put

$$
\eta_i=\nu_i\restriction\ell_j,
$$

so that $\eta_i\in F_j$. By the stabilization used in constructing $F_j$,

$$
d(\nu_0,\dots,\nu_{n-1})
=
d(\eta_0,\dots,\eta_{n-1}).
$$

Hence $d$ is end homogeneous on $T$.

$$
\tag*{$\square$}
$$
