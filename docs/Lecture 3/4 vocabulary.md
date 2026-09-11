# Coherent decisions and permutation data


For $a\in[B]^{\leq n}$, define its interior by

$$
b_a^\circ=b_a\setminus\bigcup_{u\subsetneq a}b_u.
$$

An **interior condition** for $a$ is a condition supported in $b_a^\circ$.

A finite family is **coherent** if its conditions agree on common faces under the canonical identifications. Its union is then a Cohen condition.

!!! lemma "Finite extension lemma"

    Any finite coherent family can be coherently strengthened so that every required $n$-face, in every ordering of its vertices, has a condition deciding its color. Earlier decisions are preserved.

**Proof.** 

List the required decisions. For each one, take a common extension with a member of the local maximal antichain. Copy its face restrictions to the corresponding faces and strengthen the conditions already chosen. Repeat finitely many times. $\square$

For an unordered $n$-set $x$ of nodes and $\pi\in S_n$, place the vertex data according to $\pi$ and choose a condition deciding a color $c_\pi(x)$. Set

$$
\vec c(x)=\langle c_\pi(x):\pi\in S_n\rangle\in\sigma^{n!}.
$$

Different permutations may use different interiors. For triples, $\vec c(x)$ is a six-tuple. Strengthening does not change it.
