# Strong Similarity


Our goal is to introduce some equivalence relations on leveled sets $a$ from $[2^{<\omega}]^n$. All of them are focused on capturing the branching behavior of the elements of $a$ in $2^{<\omega}$. 


Suppose first that  $\bar\nu=\langle\nu_0,\ldots,\nu_{n-1}\rangle$ and 
$\bar\eta=\langle\eta_0,\ldots,\eta_{n-1}\rangle$ enumerate $n$-element subsets of some common level $2^m$.  We say these tuples are 
**strongly similar** if

$$
i<j<n\Longrightarrow \Delta(\nu_i,\nu_j) = \Delta(\eta_i,\eta_j)
$$

(so corresponding pairs in the tuples branch at the same level) and  if

$$
\alpha=\Delta(\nu_{i},\nu_{j})=\Delta(\eta_i,\eta_j)
$$

then for every $k<n$, 

$$
\nu_k(\alpha) = \eta_k(\alpha)
$$

(so corresponding nodes pass to the same side of every split occuring in the configuration.)


Strongly similar $n$-tuples from $2^m$ have the same branching pattern in a strong sense.  This notion depends on the enumeration of the tuples, but for unordered level sets $a=\{\nu_0,\dots,\nu_{n-1}\}$ and $b = \{\eta_0,\dots,\eta_{n-1}\}$ we say that $a$ and $b$ are *strongly similar* if their lexicographically increasing enumerations are strongly similar.

 

!!! Definition Almost Homogeneous

      An $n$-dimensional level coloring $d$ of $2^{<\omega}$ is **almost homogeneous** on a subtree $T\subseteq 2^{<\omega}$ if whenever $m$ is a splitting level of $T$ and $a$ and $b$ are strongly similar in $[2^m]^n$, then $d(a)=d(b)$. Equivalently, on each splitting level of $T$,  the value of $d(a)$ depends only on the strong similarity type of $a$.


We now show that we can achieve almost homogeneous subtrees for end homogenous colors.

!!! Proposition 

      Let \(n<\omega\), let \(\sigma<\omega\), and let

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow \sigma
    $$

      be an \(n\)-dimensional level coloring. Suppose \(T\subseteq 2^{<\omega}\) is a perfect strong subtree with synchronized splitting levels and \(d\) is end homogeneous on \(T\).

      Then there is a perfect strong subtree

    $$
      S\subseteq T
    $$

      such that \(d\) is almost homogeneous on \(S\). Thus, whenever \(m\) is a splitting level of \(S\) and

    $$
      a,b\in[S\cap2^m]^n
    $$

      are strongly similar, we have

    $$
      d(a)=d(b).
    $$

      Equivalently, after passing to a further perfect strong subtree, the color of a leveled \(n\)-set depends only on its strong similarity type.

**Proof:**

We argue by induction on $n$. The case $n=1$ is immediate.

Suppose the result is known for $n$, and let $d$ be an end-homogeneous
$(n+1)$-dimensional coloring on $T$.

To each leveled $n$-tuple

$$
\bar\eta=\langle\eta_0,\ldots,\eta_{n-1}\rangle
$$

associate a finite code $D(\bar\eta)$ recording what happens when each
$\eta_i$ is allowed to split in both directions. More precisely, choose a
later common splitting level and record the values of $d$ on all relevant
$(n+1)$-element subsets of the resulting $2n$ extensions.

End homogeneity ensures that this code is independent of how far the chosen
extensions are continued. Since $d$ has finitely many colors, $D$ is itself
a finite-valued $n$-dimensional level coloring.

By the induction hypothesis, after passing to a perfect strong subtree

$$
S\subseteq T,
$$

the value of $D(\bar\eta)$ depends only on the strong similarity type of
$\bar\eta$.

Now let

$$
a,b\in[S\cap2^m]^{n+1}
$$

be strongly similar. Consider the last split occurring in their common
branching pattern. Collapsing the two branches created by that split gives
strongly similar $n$-configurations

$$
\bar\eta_a
\qquad\text{and}\qquad
\bar\eta_b.
$$

Hence

$$
D(\bar\eta_a)=D(\bar\eta_b).
$$

The sets $a$ and $b$ occupy the same entry in these identical extension
tables, so

$$
d(a)=d(b).
$$

End homogeneity allows us to ignore any additional extension beyond the
decisive splitting configuration.

Therefore $d$ is almost homogeneous on $S$.

$$\tag*{$\square$}$$

Combining the above with our previous discussion of end-homogeneity, we achieve the following version of the Halpern-Lauchli Theorem canonized for strong similarity.


!!! corollary 

    Let $n<\omega$ and let $\sigma<\omega$. Suppose

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
    $$

    is an $n$-dimensional level coloring of $2^{<\omega}$.

    Then there is a perfect strong subtree

    $$
    S\subseteq2^{<\omega}
    $$

    with synchronized splitting levels such that $d$ is almost homogeneous on $S$.

    Equivalently, whenever $m$ is a splitting level of $S$ and

    $$
    a,b\in[S\cap2^m]^n
    $$

    are strongly similar, then

    $$
    d(a)=d(b).
    $$
