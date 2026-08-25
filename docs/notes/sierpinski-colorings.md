# Sierpinski Colorings


Sierpiński [S33] proved that there is a coloring of pairs of reals with two colors such that both colors appear on every uncountable set. His proof compares a fixed well-ordering of the reals with the usual order, coloring a pair according to whether the two orders agree or disagree. In fact, both colors already appear on any set containing a copy of $\mathbb Z$, since otherwise the well-order would agree or disagree uniformly with the usual order on that copy, which is impossible.  As noted by many people, his idea yields the following result for higher dimensions:

!!! theorem "Sierpinski's Theorem in Higher Dimensions"

    For each $n\geq 1$ there is a function
    $d:[2^\omega]^n\rightarrow n!(n-1)!$ such that $d$ assumes all values
    on $[X]^n$ whenever $X\subseteq 2^\omega$ is dense-in-itself.

Proof:

The proof involves three orders: a well-ordering $\prec$ of $2^{\omega}$,
the lexicographic ordering $<_{\mathrm{lex}}$ on $2^{\omega}$, and the
shortlex order $\triangleleft$ on $2^{<\omega}$. This latter order is
defined by

$$
s\triangleleft t\iff |s|<|t|,\text{ or }(|s|=|t|\text{ and }s<_{\mathrm{lex}}t),
$$

so it compares finite sequences first by length, and then using the
lexicographic order as a tie-breaker.

Given $a\in[2^\omega]^n$, we write $a$ in lexicographically increasing
order as

$$
x_0<_{\mathrm{lex}}\cdots<_{\mathrm{lex}}x_{n-1}
$$

and by comparing consecutive entries, we derive an $n-1$-tuple

$$
(x_0\wedge x_1,\dots,x_{n-2}\wedge x_{n-1})
    =(y_0,\dots,y_{n-2})
$$

where each $y_i\in 2^{<\omega}$. Note that these entries are pairwise
distinct because our tree is binary.

From these two tuples $(x_0,\dots,x_{n-1})$ and
$(y_0,\dots,y_{n-2})$ we derive two (unique) permutations
$\sigma_a\in S_n$ and $\tau_a\in S_{n-1}$: $\sigma_a$ is the permutation
of $n$ that rearranges the $n$-tuple into $\prec$-increasing order, and
$\tau_a$ is the permutation of $n-1$ that arranges the $n-1$-tuple into
$\triangleleft$-increasing order. Thus,

$$
x_{\sigma_a(0)}\prec\cdots\prec x_{\sigma_a(n-1)},
$$

and

$$
y_{\tau_a(0)}\triangleleft\cdots\triangleleft y_{\tau_a(n-2)}.
$$

Our coloring $d$ is defined (modulo a bijection between
$S_n\times S_{n-1}$ and $n!(n-1)!$) by

$$
d(a)=(\sigma_a,\tau_a)\in S_n\times S_{n-1}.
$$

We now show that for every dense-in-itself $X\subseteq2^\omega$, the
restriction $d\upharpoonright[X]^n$ realizes each of the
$n!(n-1)!$ possible values. We borrow the following lemma taken from [RT23].

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

Note that a countable metrizable space without isolated points is
homeomorphic to $\mathbb{Q}$, so this shows us that $X$ contains a copy
of $\mathbb{Q}$ enumerated in order-type $\omega$. By our lemma, it
suffices to prove that for any $\prec$-increasing
$A=\{a_k:k<\omega\}\subseteq X$ with no isolated points, for each
$(\sigma,\tau)\in S_n\times S_{n-1}$ there is an $a\in[A]^n$ such that
$\sigma_a=\sigma$ and $\tau_a=\tau$.

The first step is to construct a $<_{\mathrm{lex}}$-increasing sequence
$\langle u_0,\dots,u_{n-1}\rangle$ of pairwise incomparable nodes in
$2^{<\omega}$ such that $[u_i]\cap A\neq\emptyset$ and, letting
$b_i=u_i\wedge u_{i+1}$ for $i<n-1$, we have

$$
b_{\tau(0)}\triangleleft\dots\triangleleft b_{\tau(n-2)}.
$$

If we choose $a_i\in A\cap[u_i]$ for each $i<n$, then
$a_i\wedge a_{i+1}=b_i$ for $i<n-1$, and so $\tau_a=\tau$ where
$a=\{a_i:i<n\}\in[A]^n$.

We do this by a repeated splitting argument. The point is the permutation
$\tau$ encodes a “splitting pattern” in a binary tree of height $n$ in
which each level has exactly one splitting node. The following example shows
how this works; it will be useful to keep this picture in mind later when we look
at Shelah's forcing construction.

??? example

    For example, suppose $\langle2,0,3,1\rangle$ is our $\tau\in S_4$.
    This determines a sequence of splits as follows:

    $$
    \{0,1,2,3,4\}
    \rightarrow \{0,1,2\mid3,4\}
    \rightarrow \{0\mid1,2\mid3,4\}
    \rightarrow \{0\mid1,2\mid3\mid4\}
    \rightarrow \{0\mid1\mid2\mid3\mid4\}.
    $$

    Note at stage $i$ of the process, we insert a split between $\tau(i)$
    and $\tau(i)+1$. This results in a binary branching tree as follows:

    ![Splitting tree for the permutation 2,0,3,1](../images/split-pattern-2031.svg)

    Thus, $\langle2,0,3,1\rangle$ codes the abstract splitting pattern

    ![Abstract splitting pattern for the permutation 2,0,3,1](../images/split-pattern-2031-abstract.svg)

    It is also straightforward to pass from splitting patterns to coding
    permutations.For example, the abstract splitting pattern

    ![A second abstract splitting pattern](../images/split-pattern-1203-abstract.svg)

    is realized by the splits

    ![Realization of the second splitting pattern](../images/split-pattern-1203.svg)

    Thus, the splitting pattern is coded by the permutation
    $\langle1,2,0,3\rangle$.


!!! corollary

    $$
    2^{\aleph_0}\nrightarrow[\aleph_1]^n_{n!(n-1)!}.
    $$

## References

- [RT23] **D. Raghavan and S. Todorčević.** “Galvin’s problem in higher dimensions.”
  *Proceedings of the American Mathematical Society* **151** (2023), no. 7,
  3103–3110. [DOI: 10.1090/proc/16386](https://doi.org/10.1090/proc/16386)

- [S33] **W. Sierpiński.** “Sur une problème de la théorie des relations.”
  *Annali della Scuola Normale Superiore di Pisa*, Series 2, **2** (1933),
  239–242.