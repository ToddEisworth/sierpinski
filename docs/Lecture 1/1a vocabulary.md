# Vocabulary

##  Basic Terms

We lay out our notation for some standard concepts, mostly trying to stay consistent with [T].

The full binary tree is

$$
2^{<\omega}=\bigcup_{m<\omega}2^m,
$$

and $2^m$ is level $m$. 

For $s,t\in 2^{<\omega}$, we write $s\unlhd t$ if $s$ is an initial segment of $t$, and $s\lhd t$ if $s$ is a proper initial segment of $t$.     We write $|s|$ for the length of $s$, so node $s$ lies on level $|s|$.

By a **tree**, we mean a meet-closed set \(T\subseteq 2^{<\omega}\), ordered by the inherited initial-segment relation \(\unlhd\), having a least element, such that every \(t\in T\) has two incompatible extensions in \(T\).

For $t\in T$, the **height of $t$ in $T$** is

$$
\operatorname{ht}_T(t)=\left|\{s\in T:s\lhd t\}\right|.
$$

The **$m$th level of $T$** is

$$
T(m)=\{t\in T:\operatorname{ht}_T(t)=m\}.
$$

Thus, the level of a node in $T$ is determined by its position in the tree $T$, whereas its length $|t|$ is its level in the ambient tree $2^{<\omega}$. These need not be the same. In particular, a node on level $m$ of $T$ may have length greater than $m$.

If $S$ and $T$ are trees, we say that $S$ is a **subtree** of $T$ if $S\subseteq T$ and the tree order on $S$ is the restriction of the tree order on $T$.

This definition is very general. Note that it does not require that $S$ is closed under initial segments of $T$, nore does it require that a level of $S$ is contained in some level of $T$.  We won't need the full generality, however, and the following gets us a more organized concept.



Suppose $S$ is a subtree of $T$ and there is a strictly increasing sequence

$$
\ell_0<\ell_1<\ell_2<\cdots
$$

such that

$$
S(n)\subseteq T(\ell_n)
$$

for every $n<\omega$. We call $\{\ell_n:n<\omega\}$ the **level set of $S$ in $T$**.  

We say that a subtree $S$ of $T$ is a **strong subtree** of $T$ if $S$ has a level set in $T$ and whenever $s\in S(n)$ and $t$ is an immediate successor of $s$ in $T$, then there is exactly one node of $S(n+1)$ extending $t$.  

Thus, a strong subtree preserves the branching pattern of the larger tree on the subtree's level set.









## References

  
- [T] Todorcevic, Stevo. *Introduction to Ramsey Spaces*. Annals of Mathematics Studies, vol. 174. Princeton, NJ: Princeton University Press, 2010.