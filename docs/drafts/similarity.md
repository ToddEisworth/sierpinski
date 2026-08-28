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



More explicitly, suppose $\alpha<\beta$ are splitting levels of $T$, and

$$
\{\nu_0,\ldots,\nu_{n-1}\}
\subseteq
T\cap 2^\beta
$$

is such that the restrictions

$$
\nu_0\restriction\alpha,\ldots,\nu_{n-1}\restriction\alpha
$$

are pairwise distinct. Enumerate both the upper and lower configurations in
lexicographic order. Then

$$
d(\nu_0,\ldots,\nu_{n-1})
=
d(\nu_0\restriction\alpha,\ldots,\nu_{n-1}\restriction\alpha).
$$

Thus, once the $n$ branches have separated, extending their ends farther up the
tree does not change the color.

This is the end-homogeneous consequence of the synchronized
Halpern--Läuchli theorem.




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

!!! lemma "Lemma [RT23]"

    If $X$ is a dense-in-itself subset of $2^{\omega}$ enumerated by
    $f:\kappa\rightarrow X$, then there is an $A\subseteq \kappa$ of
    order-type $\omega$ such that $f[A]$ is dense-in-itself.
    ---
    Proof:

       For each non-empty relatively open $U\subseteq X$ define

    $$
    \rho(U)=\sup\{\alpha+1:f(\alpha)\in U\},
    $$

    and choose $U$ so that $\delta=\rho(U)$ is minimal. This means every
    nonempty relatively open $V\subseteq U$ satisfies $\rho(V)=\delta$
    as well. The ordinal $\delta$ must be a limit. If not, then
    $\delta=\gamma+1$ and $f(\gamma)\in U$. Since $U$ has no isolated
    points, there is a non-empty relatively open $V\subseteq U$ avoiding
    $f(\gamma)$. Then $\rho(V)\leq\gamma<\delta$ and we have contradicted
    our choice of $U$.

    Now let $V_0,V_1,\dots$ enumerate a basis of nonempty open subsets of
    $U$ sot that each basis element appears infinitely often. Since
    $\rho(V_n)=\delta$ we can recursively choose

    $$
    \alpha_0<\alpha_1<\dots
    $$

    such that $f(\alpha_n)\in V_n$. Now let

    $$
    A=\{\alpha_n:n<\omega\}.
    $$
    
    This has order-type $\omega$, and the repetition of basic open sets
    ensures that $f[A]$ has no isolated points.
    An $n$-dimensional level coloring of $T$ is **end homogeneous** if whenever $\alpha<\beta$ are splitting levels of $T$ and we
    are given an $n$-tuple $\nu_0,\dots, \nu_{n-1}$ from level $\beta$ on which the projection to level $\alpha$ is one-to-one, then
   
    $$
    d(\nu_0,\dots, \nu_{n-1})=d(\nu_0\upharpoonright\alpha,\dots, \nu_{n-1}\upharpoonright \alpha).
    $$