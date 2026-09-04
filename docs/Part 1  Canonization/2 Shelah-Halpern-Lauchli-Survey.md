# The Halpern-Lauchli Theorem




##  Basic Terms

We lay out our notation for some standard concepts.  First, the full binary tree is

$$
2^{<\omega}=\bigcup_{m<\omega}2^m,
$$

and $2^m$ is level $m$. 

For $s,t\in 2^{<\omega}$, we write $s\unlhd t$ if $s$ is an initial segment of $t$, and $s\lhd t$ if $s$ is a proper
initial segment of $t$.     We write $|s|$ for the length of $s$, so node $s$ lies on level $|s|$.

A **level subset** of the tree is just a subset of $2^m$ for some fixed $m$.  Similarly, a level $n$-tuple will be a $n$-tuple of *distinct* elements of some $2^m$ (so no repeats allowed).  Thus, a level $n$-tuple enumerates a level subset of the tree of size $n$.  The distinction will be important for us, so we reserve the use of "tuple" for settings where order is important.


## Strong embeddings

Given rooted binary trees $S$, $T\subseteq 2^{<\omega}$, a  **strong embedding** is an injection

\[
e:S\rightarrow T
\]

for which there is a strictly increasing level map $\lambda$ from the levels of $S$ to the levels of $T$ such that 

- the root of $S$ is sent to the root of $T$,

- levels are respected:  $|e(s)|=\lambda(|s|)$,

- meets are preserved:   $e(s\wedge t)= e(s)\wedge e(t)$, and

- branching directions are preserved:  whenever $s\lhd t$ then $e(t)(|e(s)|)=t(|s|)$.  Equivalently, if $s^\frown i\unlhd t$ then $e(s)^\frown i\unlhd e(t)$.

The image $e[S]$ is called a **strong copy** of $S$ in $T$. It preserves the relative arrangement of the levels, all meets, and all left-right branching directions even though
the distances between successive levels may be stretched by the embedding.


??? example  "Example: Picturing a strong embedding"

      ![strong embedding](../images/strong-embedding-height-4(2).svg)
      




## Common level sets

Strong subtrees

\[
S_0,\dots,S_{d-1}
\]

have a **common level set** if

\[
L(S_0)=\cdots=L(S_{d-1}).
\]

If their common level set is

\[
L=\{\ell_k:k<\omega\},
\]

then for each \(k<\omega\) the **\(k\)-th level product** is

\[
\prod_{i<d}\bigl(S_i\cap 2^{\ell_k}\bigr).
\]

The full level product is

\[
\bigcup_{k<\omega}
\prod_{i<d}\bigl(S_i\cap 2^{\ell_k}\bigr).
\]

Let \(S,T\subseteq 2^{<\omega}\) be trees. An injection $e:S\longrightarrow T$

is a **strong embedding** if the following hold.

* **Tree order is preserved:** $s\subseteq t\Longleftrightarrow e(s)\subseteq e(t).$

* **Levels are preserved up to a common reindexing:** there is a strictly increasing map $h:\{\lg(s):s\in S\}\longrightarrow\omega$

   such that $\lg(e(s))=h(\lg(s))$ for every $s\in S$.

* **Left/right branching is preserved:** whenever \(\lg(s)<\lg(t)\), we have $e(t)\bigl(\lg(e(s))\bigr)=t(\lg(s))$.


The image \(e[S]\) is called a **strong copy** of \(S\) in \(T\).

Equivalently, condition (3) says that if \(t\) extends \(s^\frown\langle i\rangle\), then \(e(t)\) lies on the \(i\)-side of \(e(s)\) at the level in the ambient tree corresponding to \(s\).

A subtree \(T'\subseteq T\) is called a **strong subtree** if it is the range of a strong embedding into \(T\).

In particular, a strong copy of \(2^{<\omega}\) is obtained by choosing an increasing sequence of levels $\ell_0<\ell_1<\ell_2<\cdots$ and realizing the \(k\)-th level of the abstract binary tree inside level \(\ell_k\) of the ambient tree, while preserving the full left/right branching pattern.


 






## Meet and splitting level

For \(s,t\in 2^{<\omega}\), let $s\wedge t$ denote their longest common initial segment. If $s$ and $t$ are incomparable, we define

$$
\Delta(s,t)=|s\wedge t| =\min\{m: s(m)\neq t(m)\}.
$$

We use the same notation for branches $x$ and $y$ in $2^\omega$.



For a subtree $T\subseteq 2^{<\omega}$, let $\operatorname{sp}(T)$ be the set of splitting nodes of $T$, that is those $\eta\in T$ such that both $\eta^\frown\langle 0\rangle$ and $\eta^\frown\langle 1\rangle$ are in $T$.  The **splitting levels** of $T$ are defined by

$$
\operatorname{SP}(T)
=
\{\lg(\eta):\eta\in\operatorname{sp}(T)\}.
$$

A subtree $T$ is **perfect** if every node of $T$ has two incomparable
extensions in $T$; that is, for every $s\in T$ there are incomparable
$t_0,t_1\in T$ such that

$$
s\unlhd t_0
\qquad\text{and}\qquad
s\unlhd t_1.
$$










## Strong Embeddings


Let \(S,T\subseteq 2^{<\omega}\) be trees. An injection $e:S\longrightarrow T$

is a **strong embedding** if the following hold.

* **Tree order is preserved:** $s\subseteq t\Longleftrightarrow e(s)\subseteq e(t).$

* **Levels are preserved up to a common reindexing:** there is a strictly increasing map $h:\{\lg(s):s\in S\}\longrightarrow\omega$

   such that $\lg(e(s))=h(\lg(s))$ for every $s\in S$.

* **Left/right branching is preserved:** whenever \(\lg(s)<\lg(t)\), we have $e(t)\bigl(\lg(e(s))\bigr)=t(\lg(s))$.


The image \(e[S]\) is called a **strong copy** of \(S\) in \(T\).

Equivalently, condition (3) says that if \(t\) extends \(s^\frown\langle i\rangle\), then \(e(t)\) lies on the \(i\)-side of \(e(s)\) at the level in the ambient tree corresponding to \(s\).

A subtree \(T'\subseteq T\) is called a **strong subtree** if it is the range of a strong embedding into \(T\).

In particular, a strong copy of \(2^{<\omega}\) is obtained by choosing an increasing sequence of levels $\ell_0<\ell_1<\ell_2<\cdots$ and realizing the \(k\)-th level of the abstract binary tree inside level \(\ell_k\) of the ambient tree, while preserving the full left/right branching pattern.


!!! definition "$\operatorname{Per}_{\mathrm{fe}}(2^{<\omega})$"

      A tree $T\in\operatorname{Per}_{\mathrm{fe}}(2^{<\omega})$ has the property that splitting is determined by the level: if one node of $T\cap 2^m$ splits immediately in $T$, then every node of $T\cap 2^m$ splits immediately in $T$.

Equivalently, $T$ is a strong copy of the full binary tree whose branching takes place on a set of selected levels. We can also define a canonical collapse map $\operatorname{clp}_T:\operatorname{sp}(T)\longrightarrow 2^{<\omega}$  which preserves both the tree order and the lexicographic order.

!!! definition "$\operatorname{Per}_{\mathrm{uq}}(2^{<\omega})$"

      A tree $T\in\operatorname{Per}_{\mathrm{uq}}(2^{<\omega})$ has at most one splitting node on each level.  We will call such a tree **skew** or **uniquely branching**.
      Thus the splitting events of a skew tree are canonically ordered by their heights. 




## The Halpern-Lauchli Theorem

The classical finite-dimensional Halpern--Lauchli theorem can be stated in the following form.

!!! theorem "HLLMP theorem"

      Let $n<\omega$, let $\sigma<\omega$, and let $d:\bigcup_{m<\omega}(2^m)^n\longrightarrow\sigma$ be a finite coloring of level products.  Then there are perfect strong subtrees $T_0,\ldots,T_{n-1}\subseteq 2^{<\omega}$,  an increasing sequence $k_0<k_1<k_2<\cdots$, and a color $c<\sigma$ such that $\operatorname{SP}(T_i)=\{k_0,k_1,k_2,\ldots\}$ for every $i<n$, and, for every $\ell<\omega$, $d(\nu_0,\ldots,\nu_{n-1})=c$ whenever $\nu_i\in T_i\cap 2^{k_\ell}$ for $i<n$.


The essential point for what follows is not merely that the level product is homogeneous, but that the coordinate trees have the **same branching levels**.

This is the form appearing in [Sh288] as Theorem 2.7(1)--(2).  Shelah attributes (1) to Halpern and Lauchli, the strengthened synchronization in (2) to Laver, and notes that Pincus observed that the original Halpern--Lauchli proof can be modified to obtain (2).  Halpern-Lauchli is easier to say, but it should really be known as the HLLMP theorem.


## References

- [Sh288] S. Shelah, *Strong Partition Relations Below the Power Set: Consistency -- Was Sierpiński Right? Vol. II*

- [HL] J. D. Halpern and H. Läuchli, “A Partition Theorem,” *Transactions of the American Mathematical Society* **124** (1966), 360–367.  

- [M] K. R. Milliken, “A Ramsey Theorem for Trees,” *Journal of Combinatorial Theory, Series A* **26** (1979), no. 3, 215–237.  
  