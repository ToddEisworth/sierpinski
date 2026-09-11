## The forcing

Fix a winning strategy $\Sigma$ for Player I. A finite approximation is a triple

$$
a=(s^a,y^a,f^a),
$$

where:

* $s^a\in[B]^{<\omega}$;
* $y^a$ is a finite play in which I follows $\Sigma$, ending with a move $(m^a,\mathcal P^a,T^a)$;
* $f^a:s^a\to\operatorname{Max}(T^a)$ is injective.

Copy $\mathcal P^a$ onto the supports associated with $s^a$. For each $u\in[s^a]^n$, use the orientation determined by $f^a\restriction u$. The union of the selected conditions is denoted by $\operatorname{cert}(a)$.

A condition in $\mathbb Q^*$ is a pair $(p,a)$ such that

$$
p\in\mathbb P
\qquad\text{and}\qquad
p\leq\operatorname{cert}(a).
$$

Set

$$
(q,b)\leq(p,a)
$$

if $q\leq p$, $y^b$ extends $y^a$, $s^a\subseteq s^b$, and

$$
f^a(\alpha)\subseteq f^b(\alpha)
\qquad(\alpha\in s^a).
$$

The set $s^a$ is a finite approximation to the uncountable set we are adjoining, while $f^a$ assigns its elements finite binary codes lying in the skew tree. The certificate transfers the decisions made by $\mathcal P^a$ to the corresponding ordinals, and the condition $p$ places those decisions into the Cohen generic.

In the generic extension, the unions of the sets $s^a$ and maps $f^a$ produce a set $H\subseteq B$ and an injective map

$$
f:H\longrightarrow [S],
$$

where $S$ is skew. The color of an $n$-element subset of $H$ depends only on the ordered $\Delta$-similarity type of its image under $f$. Thus at most

$$
n!(n-1)!
$$

colors occur on $[H]^n$.
