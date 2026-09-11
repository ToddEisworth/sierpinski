# The &#916;-system

Let

$$
\mathbb P=\operatorname{Add}(\omega,\lambda)
$$

and let $\dot d$ be a $\mathbb P$-name for a coloring of $[\lambda]^n$ into finitely many colors. Assuming

$$
\lambda\longrightarrow(\omega_1)^{2n}_{2^{\aleph_0}},
$$

Zhang's argument gives a set $B\subseteq\lambda$ of order type $\omega_1$ and countable sets

$$
b_s\subseteq\lambda \qquad (s\in[B]^{\leq n})
$$

with the following properties:

1. $s\subseteq b_s$, and for every $a\in[B]^n$, the forcing $\mathbb P\restriction b_a$ contains a maximal antichain deciding $\dot d(a)$.
2. If $|s|=|t|$, the canonical order isomorphism $h_{s,t}:b_s\to b_t$ sends $s$ onto $t$ and induces an isomorphism between the corresponding forcing notions. For $n$-sets, it also preserves the forced color.
3. For all $s,t\in[B]^{\leq n}$,

    $$
    b_s\cap b_t=b_{s\cap t}.
    $$

4. The maps $h_{s,t}$ commute with restriction to smaller faces.

Under GCH, $\lambda = \aleph_{2n+1}$ satisfies the assumption.

Just as in Lecture 2,  every decision about the color of an $n$-set can be made locally and copied coherently to any other $n$-set.

For $s\in[B]^{\leq n}$, write

$$
\mathbb P_s=\mathbb P\restriction b_s.
$$

The poset $\mathbb P_\emptyset$ is common to every $\mathbb P_s$. We first force with $\mathbb P_\emptyset$ and replace each $\mathbb P_s$ by its quotient over the resulting generic filter. From now on, we assume that the common base poset is trivial and so the sets $b_{\{\alpha\}}$ for $\alpha\in B$ are disjoint.
