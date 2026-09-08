# &#916;-Congruence

Our goal is to introduce some equivalence relations on level $n$-tuples and $n$-sets from $2^{<\omega}$ intended to capture the branching behavior of finite configurations in $2^{<\omega}$. 



!!! Definition "$\Delta$-congruence"

    Let $a,b\in[2^m]^n$, and let $h:a\to b$ be the unique
    lexicographic order-preserving bijection.

    We say that $a$ and $b$ are **$\Delta$-congruent** if, for all distinct
    $s,t\in a$,

    $$
    \Delta(s,t)=\Delta(h(s),h(t)),
    $$

    and whenever

    $$
    \alpha=\Delta(s,t),
    $$

    then, for every $u\in a$,

    $$
    u(\alpha)=h(u)(\alpha).
    $$

    Thus, corresponding pairs split at the same levels, and at each splitting
    level the corresponding nodes lie on the same side of the split.






**Note:** In [Sh:288] this is called *strong similarity*, but that terminology is at odds with more recent work. Our use of *congruence* captures the idea that the actual splitting levels matter.




!!! definition "Almost homogeneous"

    An $n$-dimensional level coloring $d$ of $2^{<\omega}$ is **almost homogeneous** on a subtree $T\subseteq 2^{<\omega}$ if the value of $d(a)$ depends only on the $\Delta$-congruence type of $a$. 

We now show that almost homogeneous subtrees can be obtained from end-homogeneous colorings.

!!! proposition

    Let $n<\omega$, let $\sigma<\omega$, and let

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
    $$

    be an $n$-dimensional level coloring. Suppose $T\subseteq2^{<\omega}$ is a strong subtree of $2^{<\omega}$ and $d$ is end homogeneous on $T$.

    Then $T$ has a strong subtree $S$ such that $d$ is almost homogeneous on $S$. 

**Proof.** 

We argue by induction on $n$. The case $n=1$ is immediate.

Suppose the result is known for $n$, and let $d$ be an end-homogeneous $(n+1)$-dimensional coloring on $T$.  We want to define an $n$-dimensonal coloring $D$ to which we can apply our induction hypothesis.  

Given a set $a\in [T(\ell)]^k$, since $T$ is a strong subtree of $2^{<\omega}$ we know that every node of $a$ has exactly two extensions in $T(\ell+1)$.  The value of $D_k(a)$ should be a function mapping a subset of $[2k]^{n+1}$ to $\sigma$ that codes the value of $d$ on every possible extension of $a$ to an $n+1$-element subset of $T(\ell+1)$.  (This is vacuous if $2k<n+1$.)  

Repeated applications of our induction hypothesis and the end-homogeneous version of Halpern-Lauchli produces a strong subtree $S$ of $T$ such that for each $k\leq n$, the coloring $D_k$ is almost homogeneous on $S$.

!!! claim  "Claim: $d$ is almost homogeneous on $S$."

Suppose then that $a$ and $b$ are $\Delta$-congruent members of $[S(m)]^{n+1}$ for some $m$.
Let $j<m$ be maximal such that the set of predecessors of $a$ in $S(j)$ has size
$k<n+1$. Since $a$ and $b$ are $\Delta$-congruent, the corresponding set of
predecessors of $b$ in $S(j)$ also has size $k$, and these two $k$-sets are
$\Delta$-congruent.

On the next level of $S$, the members of $a$ have become distinct. Restricting
them further to the next level of $T$ above $S(j)$ gives an $(n+1)$-element
extension recorded by $D_k$; the same is true for $b$. Moreover, $\Delta$-congruence
ensures that the two extensions occupy corresponding entries of the two codes.

Since $D_k$ is almost homogeneous on $S$, the two codes agree. Hence the
corresponding extensions have the same $d$-color. Finally, end homogeneity of $d$
implies that extending these configurations up to $a$ and $b$ does not change
their colors. Therefore

$$
d(a)=d(b).
$$

$$
\tag*{$\square$}
$$

Combining this proposition with the preceding end-homogeneity result gives the following version of the Halpern--L\"auchli theorem canonized up to $\Delta$-similarity.

!!! corollary

    Let $n<\omega$ and let $\sigma<\omega$. Suppose

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
    $$

    is an $n$-dimensional level coloring of $2^{<\omega}$. Then there is strong subtree

    $$
    S\subseteq2^{<\omega}
    $$

   such that $d$ is almost homogeneous on $S$. 