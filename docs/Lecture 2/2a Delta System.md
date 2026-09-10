# Multi-dimensional &#916;-systems a la Zhang

Assume

- $\mathbb{P}=\operatorname{Add}(\omega,\lambda)$ where $\lambda\longrightarrow(\omega_1)^4_{2^{\aleph_0}}$.

- $\dot d$ is a $\mathbb{P}$-name for a function from $[\lambda]^2$ to $\sigma<\omega$

Then there are

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


The point here is that decisions about the coloring on $B$ for a pair can be made locally and then copied out to other pairs.

## Vocabulary

For each $s\in [B]^{\leq 2}$ we get a corresponding poset $\mathbb{P}_s$ consisting of conditions in $\mathbb{P}$ whose support is in $b_s$, and by our assumptions if $|s|=|t|$ then order-preserving bijection from $b_s$ to $b_t$ induces an isomorphism between $\mathbb{P}_s$ and $\mathbb{P}_t$, and these isomorphisms commute with restriction to smaller supports.

The poset $\mathbb{P}_\emptyset$ is fixed.  The **vertex posets** $\mathbb{P}_{\{\alpha\}}$ are all isomorphic, as are all of the **segment posets** $\mathbb{P}_s$ for $s\in [B]^2$. If $\alpha_0$ and $\alpha_1$ are the first two elements of $B$, then the four posets corresponding to $\emptyset$, $\{\alpha_0\}$, $\{\alpha_1\}$, and $\{\alpha_0,\alpha_1\}$ form a representative diamond configuration: the fixed base poset, two copies of the vertex poset, and a copy of the segment poset incorporating them both.  (Note that the use of "the" here is justified, as all such posets are isomorphic in our setup.)

Note as well that we can first force with the base poset \(\mathbb P_\emptyset\) and work in the resulting extension. Replacing each \(\mathbb P_s\) by its quotient over the base generic factors out the common data. We therefore assume from now on that the base poset is trivial and suppress it from the notation.


Finally, for a pair ${\alpha,\beta}\in[B]^2$, let

$$
b_{\alpha\beta}^{\circ}
=
b_{\{\alpha,\beta\}}
\setminus
\bigl(b_{\{\alpha\}}\cup b_{\{\beta\}}\bigr).
$$

The poset consisting of conditions supported on $b_{\alpha\beta}^{\circ}$ is the **interior poset** for the segment ${\alpha,\beta}$. After factoring out the base poset, we have

$$
\mathbb P_{\{\alpha,\beta\}}
\cong
\mathbb P_{\{\alpha\}}
\times
\mathbb P_{\{\beta\}}
\times
\mathbb P_{\alpha\beta}^{\circ}.
$$

Thus a segment condition consists of two vertex conditions together with an interior condition.



   
                                                                           

  






## References

[Z1] Jing Zhang, *Monochromatic Sumset without the Use of Large Cardinals*, **Fundamenta Mathematicae** 250 (2020), 243–252.

[Z2] Jing Zhang, *A Tail Cone Version of the Halpern–Läuchli Theorem at a Large Cardinal*, **The Journal of Symbolic Logic** 84 (2019), no. 2, 473–496.

[LH] Chris Lambie-Hanson, *Higher-dimensional Delta-systems*, **Order** 40 (2023), no. 1, 173–197.