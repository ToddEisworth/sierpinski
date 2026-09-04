# &#916;-Similarity

Our goal is to introduce equivalence relations on level $n$-tuples and $n$-sets from $2^{<\omega}$. These relations capture the branching behavior of finite configurations in $2^{<\omega}$.  Be warned that there quite a notational clash between the material in [Sh:288] and more standard modern usage of the term "strong similarity", and Shelah's usage seems to change depending on which version of the paper you look at.  I will not try to reconcile things, and instead go with the following conventions:


!!! Definition "$\Delta$-isomorphic"

Two (ordered) $n$-tuples

$$
\bar\nu=\langle\nu_0,\ldots,\nu_{n-1}\rangle
\qquad\text{and}\qquad
\bar\eta=\langle\eta_0,\ldots,\eta_{n-1}\rangle
$$

from some common level $2^m$ in $2^{<\omega}$ are **$\Delta$-isomorphic** if

$$
i<j<n\Longrightarrow
\Delta(\nu_i,\nu_j)=\Delta(\eta_i,\eta_j)
$$

(so corresponding pairs in the tuples branch at the same level),  and if

$$
\alpha=\Delta(\nu_i,\nu_j)=\Delta(\eta_i,\eta_j),
$$

then, for every $k<n$,

$$
\nu_k(\alpha)=\eta_k(\alpha).
$$

Thus, at each split the corresponding nodes branch the same way.

We say that sets  

$$
a=\{\nu_0,\ldots,\nu_{n-1}\}
\qquad\text{and}\qquad
b=\{\eta_0,\ldots,\eta_{n-1}\},
$$

from some level $2^m$ are $\Delta$-isomorphic if they are $\Delta$-isomorphic $n$-tuples in their natural lexicographic order. 


!!! definition "Almost homogeneous"

    An $n$-dimensional level coloring $d$ of $2^{<\omega}$ is **almost homogeneous** on a subtree $T\subseteq 2^{<\omega}$ if, whenever $m$ is a splitting level of $T$ and $a,b\in[T\cap 2^m]^n$ are $\Delta$-similar, then $d(a)=d(b)$. Equivalently, on each splitting level of $T$, the value of $d(a)$ depends only on the $\Delta$-similarity type of $a$.

We now show that almost homogeneous subtrees can be obtained from end-homogeneous colorings.

!!! proposition

    Let $n<\omega$, let $\sigma<\omega$, and let

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
    $$

    be an $n$-dimensional level coloring. Suppose $T\subseteq2^{<\omega}$ is a perfect strong subtree with synchronized splitting levels and $d$ is end homogeneous on $T$.

    Then there is a perfect strong subtree

    $$
    S\subseteq T
    $$

    such that $d$ is almost homogeneous on $S$. Thus, whenever $m$ is a splitting level of $S$ and

    $$
    a,b\in[S\cap2^m]^n
    $$

    are $\Delta$-similar, we have

    $$
    d(a)=d(b).
    $$

    Equivalently, after passing to a further perfect strong subtree, the color of a leveled $n$-set depends only on its $\Delta$-similarity type.

**Proof.** We argue by induction on $n$. The case $n=1$ is immediate.

Suppose the result is known for $n$, and let $d$ be an end-homogeneous $(n+1)$-dimensional coloring on $T$.

To each leveled $n$-tuple

$$
\bar\eta=\langle\eta_0,\ldots,\eta_{n-1}\rangle
$$

associate a finite code $D(\bar\eta)$ recording what happens when each $\eta_i$ is allowed to split in both directions. More precisely, choose a later common splitting level and record the values of $d$ on all relevant $(n+1)$-element subsets of the resulting $2n$ extensions.

End homogeneity ensures that this code is independent of how far the chosen extensions are continued. Since $d$ has finitely many colors, $D$ is itself a finite-valued $n$-dimensional level coloring.

By the induction hypothesis, after passing to a perfect strong subtree

$$
S\subseteq T,
$$

the value of $D(\bar\eta)$ depends only on the ordered $\Delta$-similarity type of $\bar\eta$.

Now let

$$
a,b\in[S\cap2^m]^{n+1}
$$

be $\Delta$-similar. Consider the last split occurring in their common branching pattern. Collapsing the two branches created by that split gives ordered $\Delta$-similar $n$-configurations

$$
\bar\eta_a
\qquad\text{and}\qquad
\bar\eta_b.
$$

Hence

$$
D(\bar\eta_a)=D(\bar\eta_b).
$$

The sets $a$ and $b$ occupy the same entry in these identical extension tables, so

$$
d(a)=d(b).
$$

End homogeneity allows us to ignore any additional extension beyond the decisive splitting configuration. Therefore $d$ is almost homogeneous on $S$. $\square$

Combining this proposition with the preceding end-homogeneity result gives the following version of the Halpern--L\"auchli theorem canonized up to $\Delta$-similarity.

!!! corollary

    Let $n<\omega$ and let $\sigma<\omega$. Suppose

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
    $$

    is an $n$-dimensional level coloring of $2^{<\omega}$. Then there is a perfect strong subtree

    $$
    S\subseteq2^{<\omega}
    $$

    with synchronized splitting levels such that $d$ is almost homogeneous on $S$. Equivalently, whenever $m$ is a splitting level of $S$ and

    $$
    a,b\in[S\cap2^m]^n
    $$

    are $\Delta$-similar, then

    $$
    d(a)=d(b).
    $$
