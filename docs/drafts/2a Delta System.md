# Multi-dimensional &#916;-systems 

!!! lemma "Black Box Lemma"

    Let

    $$
    \mathbb P=\operatorname{Add}(\omega,\lambda),
    $$

    and assume

    $$
    \lambda\longrightarrow(\omega_1)^4_{2^{\aleph_0}}.
    $$

    Suppose

    $$
    \dot d:[\lambda]^2\longrightarrow r
    $$

    is a $\mathbb P$-name for a finite coloring. Then there are

    $$
    B\subseteq\lambda,\qquad \operatorname{otp}(B)=\omega_1,
    $$

    and countable sets

    $$
    b_s\subseteq\lambda\qquad(s\in[B]^{\le2})
    $$

    such that:

    **(CL1)** For every $s\in[B]^{\le2}$,

    $$
    s\subseteq b_s,
    $$

    and, if $s\in[B]^2$, then $\mathbb P\restriction b_s$ contains a maximal antichain deciding $\dot d(s)$.

    **(CL2)** If $s,t\in[B]^{\le2}$ and $|s|=|t|$, then $b_s$ and $b_t$ have the same order type, and the unique order isomorphism

    $$
    h_{s,t}:b_s\longrightarrow b_t
    $$

    sends $s$ onto $t$. Moreover, for $s,t\in[B]^2$,

    $$
    p\Vdash\dot d(s)=n
    \iff
    h_{s,t}(p)\Vdash\dot d(t)=n.
    $$

    **(CL3)** For all $s,t\in[B]^{\le2}$,

    $$
    b_s\cap b_t=b_{s\cap t}.
    $$

    **(CL4)** If $s_1\subseteq s_2$, $t_1\subseteq t_2$, and the order isomorphism $s_2\to t_2$ sends $s_1$ onto $t_1$, then

    $$
    h_{s_2,t_2}\restriction b_{s_1}
    =
    h_{s_1,t_1}.
    $$



[Z1] Jing Zhang, *Monochromatic Sumset without the Use of Large Cardinals*, **Fundamenta Mathematicae** 250 (2020), 243–252.

[Z2] Jing Zhang, *A Tail Cone Version of the Halpern–Läuchli Theorem at a Large Cardinal*, **The Journal of Symbolic Logic** 84 (2019), no. 2, 473–496.

[LH] Chris Lambie-Hanson, *Higher-dimensional Delta-systems*, **Order** 40 (2023), no. 1, 173–197.