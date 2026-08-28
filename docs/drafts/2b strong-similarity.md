# Strong Similarity


We have seen how end-homogeneity removes dependence on irrelevant terminal extensions.  Shelah's next equivalence relation records the finite information that remains.

We say that two $n$-tuples $\bar\nu=\langle\nu_0,\ldots,\nu_{n-1}\rangle$ and 
$\bar\eta=\langle\eta_0,\ldots,\eta_{n-1}\rangle$ from some level $2^m$ are 
**strongly similar** if

$$
i<j<n\Longrightarrow \Delta(\nu_i,\nu_j) = \Delta(\eta_i,\eta_j)
$$

(so corresponding pairs in the tuples branch at the same location) and 

$$
\alpha=\Delta(\nu_{i},\nu_{j})=\Delta(\eta_i,\eta_j)
$$

then for every $k<n$, 

$$
\nu_k(\alpha) = \eta_k(\alpha)
$$

(so corresponding nodes pass to the same side of every split occuring in the configuration.)


Thus strongly similar $n$-tuples from $2^m$ have the same branching pattern in a strong sense. 

A coloring is **almost homogeneous** on a subtree $T_1$ if it is constant on every strong-similarity class of leveled tuples in $T_1$.



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