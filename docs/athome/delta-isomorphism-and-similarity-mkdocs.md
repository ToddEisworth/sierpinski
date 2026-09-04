# \(\Delta\)-Isomorphism and \(\Delta\)-Similarity

This page uses the notation from [Tree Terminology and Conventions](tree-terminology-and-conventions.md).

## \(\Delta\)-isomorphism

Let

\[
\bar s=(s_0,\dots,s_{n-1})
\qquad\text{and}\qquad
\bar t=(t_0,\dots,t_{n-1})
\]

be ordered leveled \(n\)-tuples.

We say that \(\bar s\) and \(\bar t\) are **\(\Delta\)-isomorphic** if:

1. for all \(i,j<n\),

   \[
   \Delta(s_i,s_j)=\Delta(t_i,t_j);
   $$

2. for all \(i,j,k<n\) with \(k\notin\{i,j\}\),

   $$
   s_k\bigl(\Delta(s_i,s_j)\bigr)
   =
   t_k\bigl(\Delta(t_i,t_j)\bigr)
   $$

   whenever these values are defined.

Equivalently, the coordinate map \(s_i\mapsto t_i\) extends to an isomorphism of the finite meet trees which preserves the actual levels of all meets and the left/right data.

## \(\Delta\)-similarity

The tuples \(\bar s\) and \(\bar t\) are **\(\Delta\)-similar** if:

1. for all \(i,j,k,\ell<n\),

   $$
   \Delta(s_i,s_j)<\Delta(s_k,s_\ell)
   \iff
   \Delta(t_i,t_j)<\Delta(t_k,t_\ell);
   $$

2. for all \(i,j,k,\ell<n\),

   $$
   \Delta(s_i,s_j)=\Delta(s_k,s_\ell)
   \iff
   \Delta(t_i,t_j)=\Delta(t_k,t_\ell);
   $$

3. corresponding splitting events have the same left/right data.

Equivalently, the coordinate map \(s_i\mapsto t_i\) extends to an isomorphism of the finite meet trees which preserves the relative order of meet levels and the left/right data, but not necessarily the numerical meet levels.

Thus

\]
\Delta\text{-isomorphic}
\Longrightarrow
\Delta\text{-similar}.
\[
## Ordered versions

When the indexing of the tuple is part of the structure, we speak of **ordered \(\Delta\)-isomorphism** and **ordered \(\Delta\)-similarity**.

Thus the comparison is always made coordinatewise:

\]
s_i\longmapsto t_i.
\[
## Skew configurations

Suppose

\]
x_0<_{\mathrm{lex}}\cdots<_{\mathrm{lex}}x_{n-1}
\[
lie in a skew tree.

For \(i<n-1\), put

\]
b_i=x_i\wedge x_{i+1}.
\[
Since the tree is skew, the heights \(|b_i|\) are distinct. Hence there is a unique permutation

\]
\tau\in S_{n-1}
\[
such that

\]
|b_{\tau(0)}|
<
|b_{\tau(1)}|
<
\cdots
<
|b_{\tau(n-2)}|.
\[
The permutation \(\tau\) determines the \(\Delta\)-similarity type of the skew configuration.

## Ordered skew type

Suppose the same points also carry an external order. Let

\]
\sigma\in S_n
\[
record the external order relative to the lexicographic enumeration

\]
x_0<_{\mathrm{lex}}\cdots<_{\mathrm{lex}}x_{n-1}.
\[
Then

\]
(\sigma,\tau)
\[
determines the **ordered \(\Delta\)-similarity type**.

Hence the number of ordered skew \(\Delta\)-similarity types is

\]
n!(n-1)!.
\[
## Relation to \(\Delta\)-isomorphism

For a skew configuration, the ordered \(\Delta\)-isomorphism type is obtained from the ordered \(\Delta\)-similarity type by also recording the actual splitting levels.

Schematically,

\]
\text{ordered }\Delta\text{-isomorphism type}
=
(\sigma,\tau,\text{actual splitting levels}),
\[
while

\]
\text{ordered }\Delta\text{-similarity type}
=
(\sigma,\tau).
$$

## Terminology

Our usage is:

- **\(\Delta\)-isomorphic**: actual splitting levels are preserved;
- **\(\Delta\)-similar**: only the relative order and equality pattern of splitting levels is preserved.

In older terminology, the first corresponds to Shelah's **strong similarity**, while the second corresponds to Shelah's **similarity** and, in the skew setting, to the modern strong-similarity notion used by Sauer and Džamonja--Larson--Mitchell.
