# Codes and canonization

Let

$$
d:[\lambda]^n\longrightarrow\sigma,
\qquad
\sigma<\omega,
$$

let $A\in[\lambda]^{\omega_1}$, and let

$$
F:A\longrightarrow2^\omega
$$

be injective. Think of $F(\alpha)$ as a code for $\alpha$.

For

$$
a={\alpha_0<\cdots<\alpha_{n-1}}\in[A]^n,
$$

write

$$
F(a)=\bigl(F(\alpha_0),\ldots,F(\alpha_{n-1})\bigr).
$$

We say that $d$ is $F$-canonical on $A$ if, whenever $a,b\in[A]^n$ and $F(a)$ and $F(b)$ have the same ordered $\Delta$-similarity type, then

$$
d(a)=d(b).
$$

## Resolution levels

Fix an injection

$$
F:B\longrightarrow2^\omega.
$$

For $a\in[B]^{<\omega}$ and $m<\omega$, say that $a$ is **resolved at level $m$** if

$$
\alpha\longmapsto F(\alpha)\restriction m
$$

is one-to-one on $a$. Equivalently, by level $m$, all of the branches coding members of $a$ have separated.

Set

$$
\Delta_F(a)=\min\{m<\omega:a\text{ is resolved at level }m\}.
$$

For $m<\omega$, let

$$
I_m=\{a\in[B]^{<\omega}:a\text{ is resolved at level }m\}.
$$

Then

$$
I_m\subseteq I_{m+1}
$$

and

$$
[B]^{<\omega}=\bigcup_{m<\omega}I_m.
$$
