# The Knaster amalgamation

!!! proposition "Knaster"

```
The forcing $\mathbb Q^*$ is Knaster.
```

**Proof.** Let

$$
(p_\xi,a_\xi),\qquad a_\xi=(s_\xi,y_\xi,f_\xi)
\quad(\xi<\omega_1),
$$

be conditions in $\mathbb Q^*$. For $u\in[B]^{\leq n}$, write

$$
b_u^\circ=b_u\setminus\bigcup_{v\subsetneq u}b_v.
$$

Enlarge $s_\xi$ to a finite set $w_\xi\subseteq B$ by including every endpoint of every $u\in[B]^{\leq n}$ for which

$$
\operatorname{supp}(p_\xi)\cap b_u^\circ\neq\varnothing.
$$

The sets $b_u^\circ$ are pairwise disjoint, so $w_\xi$ is finite.

Using the $\Delta$-system lemma and the canonical isomorphisms, thin the family so that:

1. the sets $w_\xi$ form a $\Delta$-system with root $w_*$;

2. $s_\xi\cap s_\zeta=s_*$ for $\xi<\zeta$;

3. the conditions $p_\xi$ have $\Delta$-system supports and agree on their common support;

4. all $y_\xi$ are the same finite play, and the order isomorphism $\rho_{\xi,\zeta}:s_\xi\to s_\zeta$ fixes $s_*$ and preserves the codes:

   $$
   f_\zeta(\rho_{\xi,\zeta}(\alpha))=f_\xi(\alpha);
   $$

5. under the canonical identifications, the local parts of $p_\xi$ and $p_\zeta$ agree.

Here we use that there are only countably many finite abstract plays and finite Cohen patterns.

Fix $\xi<\zeta$ and set

$$
p=p_\xi\cup p_\zeta.
$$

By (3), $p$ is a Cohen condition. Moreover, if

$$
u\subseteq s_\xi\cup s_\zeta
$$

is not contained in either $s_\xi$ or $s_\zeta$, then

$$
\operatorname{supp}(p)\cap b_u^\circ=\varnothing.
$$

Indeed, if $p_\xi$ met $b_u^\circ$, then every element of $u$ would belong to $w_\xi$. Any element of $u\cap(s_\zeta\setminus s_*)$ would then belong to

$$
w_\xi\cap w_\zeta=w_*,
$$

a contradiction. The argument for $p_\zeta$ is symmetric.

By (4) and (5), the local parts of $p$ give a coherent strengthening of the system at the end of the common play. Use this as II's next move. I's strategy responds at a higher level with a tree in which every old maximal node has split.

Let $s^*=s_\xi\cup s_\zeta$. For $\alpha\in s_*$, assign one descendant of its old code. If

$$
\alpha\in s_\xi\setminus s_*,
\qquad
\rho_{\xi,\zeta}(\alpha)\in s_\zeta\setminus s_*,
$$

assign them two incompatible descendants of their common old code. This defines an injective coding $f^*$ of $s^*$ into the new maximal nodes. Let $a^*$ be the resulting finite approximation.

The new system extends both old systems, so its certificate extends the old certificates on all subsets contained in one side. It also supplies a decision for every mixed $n$-element subset of $s^*$. The interior of each new mixed face is disjoint from $p$, while its proper-face data agree with $p$. Hence

$$
q=p\cup\operatorname{cert}(a^*)
$$

is a Cohen condition, and

$$
(q,a^*)\leq(p_\xi,a_\xi),(p_\zeta,a_\zeta).
$$

Thus every two conditions in the thinned uncountable family are compatible. $\square$
