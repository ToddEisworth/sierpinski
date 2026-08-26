# Assembling Cohen conditions

Recall that $\mathbb{P}=\operatorname{Fn}(\lambda, 2, <\omega)$ is the standard forcing adjoining $\lambda$ Cohen reals. 
 For $b\subseteq\lambda$, we let

$$
\mathbb{P}(b)=\operatorname{Fn}(b\times\omega,2,{<}\omega),
$$

ordered as usual, so $q\leq p$ if and only if $q\supseteq p$.
If $b\subseteq c$ and $p\in\mathbb{P}(c)$, we write
$p\restriction b$ for $p\restriction(b\times\omega)$.

!!! definition "Exact Support System"

    Let $(W,\leq_W)$ be a finite partial order. An **exact support system**
    on $W$ is a sequence $\bar b=\langle b_w:w\in W\rangle$ of subsets of $\lambda$ satisfying:

    1. if $u\leq_W v$, then $b_u\subseteq b_v$;

    2. for all $u,v\in W$,

    $$b_u\cap b_v=\bigcup\left\{b_z:z\in W,\ z\leq_W u,\ z\leq_W v\right\}.$$

    Put $B_{\bar b}=\bigcup_{w\in W}b_w$.

!!! definition "Complete $\bar{b}$-diagrams"

    Suppose that $\bar b$ is an exact support system on $W$. A
    **complete $\bar b$-diagram** is a sequence

    $$
    \bar p=\langle p_w:w\in W\rangle
    $$

    such that:

    1. $p_w\in\mathbb{\mathbb{P}}(b_w)$ for every $w\in W$;
    2. whenever $u\leq_W v$,

    $$
    p_v\restriction b_u=p_u.
    $$


!!! definition "$\mathbb{P}[\bar{b}]$"
    Finally, define $\mathbb{P}[\bar b]$ to be the set of complete $\bar b$-diagrams with the natural coordinate-wise ordering:

    $$
    \bar q\leq\bar p
    \quad\Longleftrightarrow\quad
    (\forall w\in W)\,[q_w\leq p_w].
    $$

The following lemma tells us that this isn't changing the forcing at all:

<a id="lem-cohen-normalization"></a>

!!! lemma "Lemma"

    If $\bar p\in\mathbb{P}[\bar b]$, then the union  $N(\bar p)=\bigcup_{w\in W}p_w$
    is a condition in $\mathbb{P}(B_{\bar b})$ satisfying 

    $$
    N(\bar p)\restriction b_w=p_w
    $$
    
    for all $w\in W$.   Moreover, the map
    
    $$
    N:\mathbb{P}[\bar b]\longrightarrow\mathbb{P}(B_{\bar b})
    $$
    
    is an isomorphism, whose inverse is
    
    $$
    p\longmapsto\langle p\restriction b_w:w\in W\rangle.
    $$
    ---

    **Proof:**

    Suppose that $(\xi,n)$ belongs to both $\operatorname{dom}(p_u)$ and
    $\operatorname{dom}(p_v)$. By exactness of the support system, there is
    $z\leq_W u,v$ such that $\xi\in b_z$. Coherence gives

    $$
    p_u(\xi,n)=p_z(\xi,n)=p_v(\xi,n).
    $$

    Thus $N(\bar p)$ is a function. It is finite because $W$ and all the
    $p_w$ are finite. The restriction equation follows from coherence. The
    remaining assertions are immediate.

This tells us that $\mathbb{P}[\bar{b}]$ is not some new sort of forcing, and  we should picture a
condition $\bar{p}\in\mathbb{P}[\bar{b}]$ as a Cohen condition from $\mathbb{P}(B_\bar{b})$  that has been assembled
using $W$ as a guide.  This view has $W$ as the assembly pattern, $b_w$ as the support attached to $w\in W$, $p_w$ as the piece of our condition attached
to this support, and then the order on $W$ tells us which pieces of $\bar{p}$ are contained in/extend which other pieces of $\bar{p}$.  Expressing $\bar{p}$ in this 
manner does not add new forcing information, and it is adding organizational information instead.




<a id="lem-finite-coherent-strengthening"></a>

!!! lemma "Finite coherent strengthening"

Let $\bar p\in\mathbb{C}[\bar b]$, let $A\subseteq W$, and suppose that
$q_a\in\mathbb{C}(b_a)$, for $a\in A$, satisfy

$$
p_a\leq q_a
\qquad(a\in A)
\tag{S1}
$$

and

$$
q_a\restriction(b_a\cap b_{a'})
=
q_{a'}\restriction(b_a\cap b_{a'})
\qquad(a,a'\in A).
\tag{S2}
$$

Then

$$
q=N(\bar p)\cup\bigcup_{a\in A}q_a
$$

belongs to $\mathbb{C}(B_{\bar b})$. Consequently,

$$
r_w=q\restriction b_w
\qquad(w\in W)
$$

defines $\bar r\in\mathbb{C}[\bar b]$ such that

$$
\bar p\leq\bar r
\quad\text{and}\quad
q_a\leq r_a\quad(a\in A).
$$

??? proof

Condition (S2) shows that the conditions $q_a$, $a\in A$, are pairwise
compatible. Fix $a\in A$ and $v\in W$. If $\xi\in b_a\cap b_v$, then
by exactness of the support system there is $z\leq_W a,v$ with
$\xi\in b_z$. Since

$$
p_a\restriction b_z=p_z=p_v\restriction b_z
$$

and $p_a\leq q_a$, the conditions $q_a$ and $p_v$ agree on their common
domain. Hence the displayed union defining $q$ is a condition. Its
restrictions form the required complete diagram.

<a id="cor-one-coordinate-extension"></a>

!!! corollary "One-coordinate extension"

If $\bar p\in\mathbb{C}[\bar b]$, $w\in W$, and
$p_w\leq q_w\in\mathbb{C}(b_w)$, then there is
$\bar r\in\mathbb{C}[\bar b]$ such that

$$
\bar p\leq\bar r
\quad\text{and}\quad
q_w\leq r_w.
$$

!!! definition

A subposet $V\subseteq W$ is **support-closed** if

$$
b_u\cap b_v=
\bigcup\{b_z:z\in V,\ z\leq_W u,\ z\leq_W v\}
$$

for all $u,v\in V$. Put $B_V=\bigcup_{v\in V}b_v$.

<a id="lem-restriction-enlargement"></a>

!!! lemma "Restriction and enlargement"

If $V\subseteq W$ is support-closed, then restriction induces a complete
projection

$$
\rho_V:\mathbb{C}[\bar b]\longrightarrow
\mathbb{C}[\bar b\restriction V].
$$

Every $\bar p\in\mathbb{C}[\bar b\restriction V]$ has a canonical
extension to $W$, namely

$$
p_w=N(\bar p)\restriction b_w
\qquad(w\in W).
$$

??? proof

Under the normalization isomorphisms, $\rho_V$ is the usual restriction
map

$$
\mathbb{C}(B_{\bar b})\longrightarrow\mathbb{C}(B_V).
$$

The assertions therefore follow from the standard complete embedding

$$
\mathbb{C}(B_V)\lessdot\mathbb{C}(B_{\bar b}).
$$

<a id="lem-common-refinement-amalgamation"></a>

!!! lemma "Amalgamation over a common refinement"

For $\ell<2$, let $\bar b^\ell$ be an exact support system on a finite
partial order $W_\ell$, and put

$$
B_\ell=\bigcup_{w\in W_\ell}b_w^\ell.
$$

Suppose that the two systems have a common support-closed subdiagram on
$V$, with total support $B_V$, and that

$$
B_0\cap B_1=B_V.
\tag{A1}
$$

Let $\bar p^\ell\in\mathbb{C}[\bar b^\ell]$. If
$q_V\in\mathbb{C}(B_V)$ satisfies

$$
N(\bar p^\ell)\restriction B_V\leq q_V
\qquad(\ell<2),
\tag{A2}
$$

then

$$
r=N(\bar p^0)\cup N(\bar p^1)\cup q_V
$$

is a condition in $\mathbb{C}(B_0\cup B_1)$ extending both normalized
diagrams.

??? proof

By (A1), the only coordinates on which the two normalized conditions can
overlap belong to $B_V$. On those coordinates they are both extended by
$q_V$, by (A2). Their union is therefore a Cohen condition.

!!! definition

An **isomorphism of support systems**
$(\sigma,\pi):(W,\bar b)\to(W',\bar b')$ consists of an order
isomorphism $\sigma:W\to W'$ and a bijection
$\pi:B_{\bar b}\to B_{\bar b'}$ such that

$$
\pi[b_w]=b'_{\sigma(w)}
\qquad(w\in W).
$$

For $p\in\mathbb{C}(B_{\bar b})$, define $\pi_*p$ by

$$
(\pi_*p)(\pi(\xi),n)=p(\xi,n).
$$

<a id="lem-cohen-transport"></a>

!!! lemma "Transport"

An isomorphism of support systems induces an isomorphism

$$
\pi_*:\mathbb{C}[\bar b]\longrightarrow\mathbb{C}[\bar b']
$$

satisfying

$$
\pi_*(p\restriction b_w)
=
(\pi_*p)\restriction b'_{\sigma(w)}.
\tag{T}
$$

The action extends recursively to names, and for every forcing formula
$\varphi$,

$$
p\Vdash_{\mathbb{C}(B_{\bar b})}\varphi(\dot\tau)
\quad\Longleftrightarrow\quad
\pi_*p\Vdash_{\mathbb{C}(B_{\bar b'})}
\varphi(\pi_*\dot\tau).
$$

??? proof

The first assertion follows directly from the definition, and (T)
follows from $\pi[b_w]=b'_{\sigma(w)}$. The assertion about names and
the forcing relation follows by induction on names and formulas.

<a id="cor-persistence-decisions"></a>

!!! corollary "Persistence of decisions"

Suppose that $b\subseteq B$, $p\in\mathbb{C}(b)$, and $\dot\tau$ is a
$\mathbb{C}(b)$-name. If

$$
p\Vdash_{\mathbb{C}(b)}\varphi(\dot\tau),
$$

then every $q\in\mathbb{C}(B)$ with $p\leq q$ satisfies

$$
q\Vdash_{\mathbb{C}(B)}\varphi(\dot\tau).
$$

The corresponding assertion is preserved under the isomorphisms of
[Transport](#lem-cohen-transport).

<a id="lem-diagram-knaster"></a>

!!! lemma "Knaster and relative Knaster"

For every exact finite support system $\bar b$, the forcing
$\mathbb{C}[\bar b]$ is Knaster. If $W$ has a minimum element $0_W$, then

$$
\mathbb{C}(b_{0_W})\lessdot\mathbb{C}[\bar b],
$$

and

$$
\Vdash_{\mathbb{C}(b_{0_W})}
``\mathbb{C}[\bar b]/\dot G_{0_W}\text{ is Knaster}.''
$$

??? proof

By [Normalization](#lem-cohen-normalization), it suffices to consider
$\mathbb{C}(B_{\bar b})$. A $\Delta$-system argument, followed by
thinning so that all conditions agree on the root, shows that this
forcing is Knaster. Since $b_{0_W}\subseteq B_{\bar b}$,

$$
\mathbb{C}(B_{\bar b})
\cong
\mathbb{C}(b_{0_W})\times
\mathbb{C}(B_{\bar b}\setminus b_{0_W}).
$$

Consequently, the quotient is forcing-equivalent to
$\mathbb{C}(B_{\bar b}\setminus b_{0_W})$, which is Knaster.

Simplex orders

For a finite set $a$ and $m\leq |a|$, define

$$
\Sigma_m(a)={s\subseteq a:|s|\leq m},
$$

ordered by inclusion. We refer to $|s|$ as the rank of $s$; thus a
triple has rank $3$ and geometric dimension $2$.

Suppose that

$$
\bar b=\langle b_s\in\Sigma_m(a)\rangle
$$

satisfies

$$
s\subseteq t\Longrightarrow b_s\subseteq b_t
\quad\text{and}\quad
b_s\cap b_t=b_{s\cap t}.
\tag{SI}
$$

Since $s\cap t$ is the greatest lower bound of $s$ and $t$, condition (SI)
implies exactness of the support system. Thus all the preceding results apply
to simplex orders.

For a finite vertex set $a$, the order $\Sigma_2(a)$ is the face poset of the
complete graph on $a$. A complete diagram indexed by $\Sigma_2(a)$ consists
of one base condition, one condition for each vertex, and one condition for
every pair of vertices. This is the finite diagram underlying the pair
construction.

<a id="cor-proper-face-strengthening"></a>

!!! corollary "Proper-face strengthening"

Let $t\in\Sigma_m(a)$, and let

$$
\partial t=\{s:s\subsetneq t\}.
$$

Suppose that $\bar p$ is a complete diagram on
$\{s:s\subseteq t\}$ and that

$$
\bar q=\langle q_s:s\in\partial t\rangle
$$

is a complete diagram satisfying $p_s\leq q_s$ for every
$s\in\partial t$. Then there is a complete diagram $\bar r$ on
$\{s:s\subseteq t\}$ such that

$$
\bar p\leq\bar r
\quad\text{and}\quad
q_s\leq r_s\quad(s\in\partial t).
$$

One may take

$$
r_u=
\left(
  N(\bar p)\cup\bigcup_{s\in\partial t}q_s
\right)\restriction b_u
\qquad(u\subseteq t).
$$

In particular, every forcing decision made by $p_t$ persists in $r_t$.

For $m=2$, the proper-face data consist of the base and the two vertex
conditions. For $m=3$, they consist of the base, the three vertex conditions,
and the three pair conditions.
Proper-face strengthening is the formal
statement that a finite coherent strengthening of the proper-face data can be
incorporated without changing any decision already made by the top-face
condition.