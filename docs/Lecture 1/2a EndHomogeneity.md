# End-homogeneity

Fix $n<\omega$ and a finite set of colors $r$. An **$n$-dimensional level coloring** of a tree $T$ is a function

$$
d:\bigcup_{m<\omega}[T(m)]^n\longrightarrow r.
$$

If $a\in[T(m)]^n$ and $k<m$, let $a\upharpoonright_T k$ be the set of predecessors in $T(k)$ of the members of $a$.

We say that $d$ is **end homogeneous on $T$** if whenever $k<m$ and
$a\in[T(m)]^n$ are such that

$$
\left|a\upharpoonright_T k\right|=n,
$$

then

$$
d(a)=d(a\upharpoonright_T k).
$$

End homogeneity says that once the \(n\) nodes are distinct, extending them to a higher common level does not change their color. Thus the color is already determined at any earlier level where their predecessors are distinct.

!!! Theorem "Halpern--Läuchli, end-homogeneous form."

    For every finite $n,r$ and every $n$-dimensional level coloring

    $$
    d:\bigcup_{m<\omega}[2^m]^n\longrightarrow r,
    $$

    there is a strong subtree $T\subseteq 2^{<\omega}$ such that $d$ is end homogeneous on $T$.

(This is denoted $\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{eht}}(\omega,n,r)$ in [Sh 288].)


- [Sh:288] **S. Shelah.** “Strong partition relations below the power set:
  consistency; was Sierpiński right? II.”
  In *Sets, Graphs and Numbers (Budapest, 1991)*,
  Colloquia Mathematica Societatis János Bolyai **60**,
  North-Holland, 1992, 637–668. 