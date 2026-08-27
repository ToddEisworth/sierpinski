# Halpern--Lauchli and similarity types

This note isolates the tree-theoretic material from Section 2 of Shelah's [Sh:288].  Its purpose is expository: to pass from the classical Halpern--Lauchli theorem to Shelah's canonization statement, Theorem 2.7(3), and then to identify the finite similarity types that occur on a skew binary tree.


### Trees, subtrees, and perfect trees

We lay out our notation for some standard concepts.  First, the full binary tree is

$$
2^{<\omega}=\bigcup_{m<\omega}2^m
$$

and for $s,t\in 2^{<\omega}$, we write

$$
s\unlhd t
$$

if $s$ is an initial segment of $t$, and $s\lhd t$ if $s$ is a proper
initial segment of $t$.




A **subtree** of $2^{<\omega}$ is a set $T\subseteq 2^{<\omega}$, regarded
as a tree with the inherited initial-segment order. We do not require a
subtree to be downward closed.

A subtree $T$ is **downward closed** if

$$
t\in T,\ s\unlhd t\quad\Longrightarrow\quad s\in T.
$$

Two nodes $s,t\in T$ are **incomparable** if neither $s\unlhd t$ nor
$t\unlhd s$.

 
For $\eta\in 2^{<\omega}$, write $\lg(\eta)$ for its length.  If $\eta,\nu\in 2^{<\omega}$, define

$$
\Delta(\eta,\nu)
=
\min\{i:\eta(i)\neq \nu(i)\text{ or }i=\lg(\eta)\text{ or }i=\lg(\nu)\}.
$$

Thus, for two incomparable nodes, $\Delta(\eta,\nu)$ is their first coordinate of disagreement, and the boundary data is just 

$$
\Delta(\eta,\eta)=\lg(\eta).
$$

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










!!! Definition "Strong Embeddings"
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


## Special formats

### Level-synchronized perfect trees

A tree $T\in\operatorname{Per}_{\mathrm{fe}}(2^{<\omega})$ has the property that splitting is determined by the level: if one node of $T\cap 2^m$ splits immediately in $T$, then every node of $T\cap 2^m$ splits immediately in $T$.

Equivalently, $T$ is a strong copy of the full binary tree whose branching takes place on a set of selected levels.  Shelah defines a canonical collapse map

$$
\operatorname{clp}_T:\operatorname{sp}(T)\longrightarrow 2^{<\omega}
$$

which preserves both the tree order and the lexicographic order.

### Skew perfect trees

A tree $T\in\operatorname{Per}_{\mathrm{uq}}(2^{<\omega})$ has at most one splitting node on each level.  We will call such a tree **skew**.

Thus the splitting events of a skew tree are canonically ordered by their heights. 




## Halpern--Lauchli 

The classical finite-dimensional Halpern--Lauchli theorem can be stated in the following form.

!!! theorem "Halpern--Lauchli theorem"

      Let $n<\omega$, let $\sigma<\omega$, and let $d:\bigcup_{m<\omega}(2^m)^n\longrightarrow\sigma$ be a finite coloring of level products.  Then there are perfect strong subtrees $T_0,\ldots,T_{n-1}\subseteq 2^{<\omega}$,  an increasing sequence $k_0<k_1<k_2<\cdots$, and a color $c<\sigma$ such that

$$
\operatorname{SP}(T_i)=\{k_0,k_1,k_2,\ldots\}
$$

for every $i<n$, and, for every $\ell<\omega$,

$$
d(\nu_0,\ldots,\nu_{n-1})=c
$$

whenever

$$
\nu_i\in T_i\cap 2^{k_\ell}
\qquad(i<n).
$$

The essential point for what follows is not merely that the level product is homogeneous, but that the coordinate trees have the **same branching levels**.

This is the form appearing in Sh:288, Theorem 2.7(1)--(2).  Shelah attributes (1) to Halpern and Lauchli, the strengthened synchronization in (2) to Laver, and notes that Pincus observed that the original Halpern--Lauchli proof can be modified to obtain (2).

## 4. End homogeneity

Halpern--Lauchli gives complete homogeneity on a product of several strong trees.  Shelah next repackages this as a canonization property inside one tree.

Fix, for each $m<\omega$, a well-order $<^*_m$ of $2^m$.

A coloring

$$
d\in\operatorname{Col}^n_\sigma(T)
$$

is **end homogeneous** for $\langle <^*_m:m<\omega\rangle$ if the following holds.

Suppose $\alpha<\beta$ are splitting levels of $T$, and

$$
\nu_0,\ldots,\nu_{n-1}\in T\cap 2^\beta
$$

have pairwise distinct restrictions to level $\alpha$.  Assume moreover that the $<^*$-ordering of the tuple is already determined at level $\alpha$:

$$
\nu_i<^*_\beta\nu_j
\quad\Longleftrightarrow\quad
\nu_i\restriction\alpha<^*_\alpha\nu_j\restriction\alpha
$$

for all $i,j<n$.  Then

$$
d(\nu_0,\ldots,\nu_{n-1})
=
d(\nu_0\restriction\alpha,\ldots,\nu_{n-1}\restriction\alpha).
$$

The interpretation is simple: once the members of the tuple have separated and their relative order has stabilized, extending their ends farther up the tree does not change the color.

Shelah denotes the corresponding partition principle by

$$
\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{eht}}(\omega,n,\sigma).
$$

If the sequence $\langle <^*_m:m<\omega\rangle$ is fixed in advance, he writes

$$
\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{ehtn}}(\omega,n,\sigma).
$$

The shared-level form of Halpern--Lauchli is what makes this end-homogeneity possible: one repeatedly treats the possible extensions of already separated nodes as coordinates in a level product.

Shelah records a useful strengthened form in Claim 2.6(6).  After the appropriate thinning, if

$$
\eta_0<^*_\alpha\cdots<^*_\alpha\eta_{n-1}
$$

are nodes at a splitting level $\alpha$, and for each $i<n$ we choose two extensions

$$
\eta_i\triangleleft\nu_i^1,\nu_i^2\in T\cap 2^\beta,
$$

then

$$
d(\nu_0^1,\ldots,\nu_{n-1}^1)
=
d(\nu_0^2,\ldots,\nu_{n-1}^2).
$$

Thus, over a fixed resolved lower configuration, the color is independent of the choice of later ends.

## 5. Strong similarity

End homogeneity removes dependence on irrelevant terminal extensions.  Shelah's next equivalence relation records the finite information that remains.

Let

$$
\bar\nu=\langle\nu_0,\ldots,\nu_{n-1}\rangle,
\qquad
\bar\eta=\langle\eta_0,\ldots,\eta_{n-1}\rangle
$$

be tuples from $2^{<\omega}$.

They are **strongly similar**, with respect to $\langle <^*_m:m<\omega\rangle$, if the following conditions hold.

1. Corresponding terminal levels are equal:

   $$
   \lg(\nu_i)=\lg(\eta_i)
   \qquad(i<n).
   $$

2. Corresponding splitting coordinates are equal:

   $$
   \operatorname{sp}(\nu_i,\nu_j)
   =
   \operatorname{sp}(\eta_i,\eta_j)
   \qquad(i,j<n).
   $$

3. The local order and left/right information at every relevant splitting coordinate agrees.  More explicitly, if

   $$
   \alpha=\operatorname{sp}(\nu_{i_1},\nu_{i_2})
   $$

   and $\alpha\leq\lg(\nu_{i_3}),\lg(\nu_{i_4})$, then

   $$
   \nu_{i_3}\restriction\alpha<^*_\alpha
   \nu_{i_4}\restriction\alpha
   \quad\Longleftrightarrow\quad
   \eta_{i_3}\restriction\alpha<^*_\alpha
   \eta_{i_4}\restriction\alpha,
   $$

   and

   $$
   \nu_{i_3}(\alpha)=\eta_{i_3}(\alpha).
   $$

Strong similarity therefore remembers the **actual numerical locations** of all relevant levels.

A coloring is **almost homogeneous** on a subtree $T_1$ if it is constant on every strong-similarity class of leveled tuples in $T_1$.

Shelah denotes the corresponding principle by

$$
\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{aht}}(\omega,n,\sigma),
$$

or by $\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{ahtn}}$ when the orders $<^*_m$ are fixed in advance.

Claim 2.6(1), and its fixed-order form 2.6(1A), show that end homogeneity can be upgraded to almost homogeneity.  The proof is by induction on $n$: the lower-dimensional coloring records enough information about the possible ways in which the next branching event can occur, and end homogeneity makes that finite record independent of the particular later extensions.

## 6. Similarity

Strong similarity is deliberately rigid.  Ordinary **similarity** forgets the actual level numbers and keeps only their finite order pattern.

Let

$$
\bar\nu^a=\langle\nu_0^a,\ldots,\nu_{n-1}^a\rangle,
\qquad
\bar\nu^b=\langle\nu_0^b,\ldots,\nu_{n-1}^b\rangle.
$$

They are **similar** if, for every choice of indices $i_1,i_2,i_3,i_4<n$, the following truth values are the same for $t=a$ and $t=b$.

1. Relative terminal heights:

   $$
   \lg(\nu_{i_1}^t)<\lg(\nu_{i_2}^t).
   $$

2. Relative splitting heights:

   $$
   \operatorname{sp}(\nu_{i_1}^t,\nu_{i_2}^t)
   <
   \operatorname{sp}(\nu_{i_3}^t,\nu_{i_4}^t).
   $$

3. Local order and left/right information.  If

   $$
   \alpha_t=
   \operatorname{sp}(\nu_{i_1}^t,\nu_{i_2}^t)
   $$

   and the other two nodes reach level $\alpha_t$, then the corresponding truth value

   $$
   \nu_{i_3}^t\restriction\alpha_t<^*_{\alpha_t}
   \nu_{i_4}^t\restriction\alpha_t
   \quad\text{and}\quad
   \nu_{i_3}^t(\alpha_t)=0
   $$

   is the same in the two tuples.

Thus:

- strong similarity preserves the actual splitting levels;
- similarity preserves only the relative order of the splitting levels, together with the same finite branching and order data.

A coloring is **homogeneous** on $T_1$ if it is constant on similarity classes of leveled tuples in $T_1$.  Shelah writes

$$
\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{ht}}(\omega,n,\sigma)
$$

and, with the orders fixed in advance,

$$
\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{htn}}(\omega,n,\sigma).
$$

This is canonization rather than monochromaticity: the color may vary, but only as the finite similarity type varies.

## 7. From Halpern--Lauchli to Shelah's Theorem 2.7(3)

Shelah summarizes the route immediately before Theorem 2.7.

1. Halpern--Lauchli gives Theorem 2.7(1).
2. Laver's strengthening gives Theorem 2.7(2), in which the coordinate trees have exactly the same splitting set.
3. From this synchronized product theorem one obtains

   $$
   \operatorname{Pr}^{\mathrm{fe}}_{\mathrm{ehtn}}(\omega,n,r)
   $$

   for every finite $r$.
4. Claim 2.6 upgrades end homogeneity to strong-similarity canonization.
5. At $\omega$, one then thins the infinite set of splitting levels so that the actual numerical locations of finitely many relevant splitting levels no longer matter; only their relative order remains.  This is an ordinary finite Ramsey thinning of the level set.  In Shelah's terminology, in the nice $\mu=\omega$ version the auxiliary orders cause no additional obstruction.

The result is Theorem 2.7(3):

### Shelah's canonized Halpern--Lauchli theorem

For every $n<\omega$ and every finite $\sigma$,

$$
\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{htn}}(\omega,n,\sigma)
$$

holds.

Equivalently, after fixing the auxiliary orders $\langle<^*_m:m<\omega\rangle$, every finite coloring

$$
d:\bigcup_{m<\omega}[2^m]^n\longrightarrow\sigma
$$

admits a level-synchronized perfect subtree

$$
T\in\operatorname{Per}_{\mathrm{fe}}(2^{<\omega})
$$

such that, on the splitting levels of $T$, the color of an $n$-element leveled configuration depends only on its similarity type.

Shelah does not present the passage from 2.7(2) to 2.7(3) as a separate long proof; he explicitly describes the resulting end-homogeneity and homogeneity statements as easy consequences of the shared-level version together with Claim 2.6.  The preceding list makes the canonization steps explicit.

## 8. Why skew trees make the finite types transparent

We now pass from a level-synchronized perfect tree to a perfect skew subtree, using Fact 2.5(1).

Take $n$ distinct branches through a skew binary tree.  Their finite meet-closure is a finite rooted binary tree with

- $n$ terminal branches, and
- exactly $n-1$ branching nodes.

Because the ambient tree is skew, these $n-1$ branching nodes occur at distinct levels.  Hence they are naturally ranked from first split to last split.

The similarity type has two independent pieces of finite information.

### 8.1 The ranked planar branching pattern

Begin with one unresolved branch.  At the first splitting event there is only one branch that can split.  After that split there are two current branches; at the second splitting event, either one may split.  After $j-1$ splitting events there are $j$ current branches, and the next splitting event chooses one of those $j$ branches.

Thus the number of possible ranked planar branching patterns is

$$
1\cdot 2\cdot 3\cdots(n-1)=(n-1)!.
$$

This is exactly the information carried by the relative order of the splitting coordinates together with the left/right tree structure.

### 8.2 The external ordering of the $n$ points

In applications to Sierpiński colorings, the $n$ points also carry an external linear order: for example, an ordinal order or a fixed well-order of the reals.  The tree itself gives a left-to-right lexicographic order on the $n$ terminal branches.

The external order may appear in any of the $n!$ possible orders relative to the left-to-right tree order.  Equivalently, there is a permutation

$$
\pi\in S_n
$$

recording where the externally ordered points occur among the lexicographically ordered branches.

Therefore the total number of types is

$$
n!\,(n-1)!.
$$

For example:

$$
2!1!=2,
$$

which recovers the two pair types underlying the classical Sierpiński coloring, while

$$
3!2!=12,
$$

so triples have twelve types.

## 9. Relation with the $\tau$-data of Sierpiński colorings

The usual Sierpiński type attached to a finite set of reals records precisely the same two kinds of information:

1. how the external well-order of the points is related to their left-to-right order in the binary tree;
2. the order in which the relevant first-disagreement coordinates occur.

On a skew tree, no two distinct branching events occur at the same level.  Consequently the second item is exactly a ranked planar binary-tree pattern.  The $\tau$-data therefore packages the same combinatorial information as Shelah's **similarity type**.

The distinction with strong similarity is important.  Strong similarity would also remember the actual integers at which the disagreements occur.  The Sierpiński type, like Shelah's ordinary similarity, retains only the finite relative pattern.

This is why Theorem 2.7(3) is the natural Halpern--Lauchli statement to place after a discussion of Sierpiński colorings: it says that an arbitrary finite coloring can be thinned to a perfect binary configuration on which the color is controlled by exactly this finite tree type.

## 10. Source map

The relevant portions of Sh:288 are:

- Definition 2.1: $\operatorname{Per}$, $\operatorname{Per}_{\mathrm{fe}}$, $\operatorname{Per}_{\mathrm{uq}}$, splitting nodes and splitting levels;
- Definition 2.2: leveled colorings, end homogeneity, strong similarity, similarity, almost homogeneity, and homogeneity;
- Definition 2.3: the principles $\operatorname{Pr}_{\mathrm{eht}}$, $\operatorname{Pr}_{\mathrm{aht}}$, $\operatorname{Pr}_{\mathrm{ht}}$ and their $\mathrm{fe}$ and fixed-order variants;
- Fact 2.5(1): thinning to a perfect skew tree;
- Claim 2.6: passage from end homogeneity to strong-similarity canonization and the special simplifications at $\mu=\omega$;
- Theorem 2.7(1)--(2): Halpern--Lauchli with synchronized splitting levels;
- Theorem 2.7(3): $\operatorname{Pr}^{\mathrm{fe}}_{\mathrm{htn}}(\omega,n,\sigma)$ for finite $\sigma$;
- Remark 3.2(1): Shelah's later count is expressed as $n!$ times the number of skew strong-similarity types.

For the classical Sierpiński count, Galvin--Shelah explicitly note that the standard construction generalizes to $n$-sets with $n!(n-1)!$ colors.

## References

- [Sh288] S. Shelah, *Strong Partition Relations Below the Power Set: Consistency -- Was Sierpiński Right? Vol. II*
