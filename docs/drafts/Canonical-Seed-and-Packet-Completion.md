# Cohen diagrams, canonical seeds, and packet completion for triples

## 1. The local objective

Work in the ground model. Let

\[
\mathbb P=\operatorname{Add}(\omega,\delta)
=\operatorname{Fn}(\delta\times\omega,2,{<}\omega),
\]

ordered by reverse inclusion: \(q\leq_{\mathbb P}p\) means \(q\supseteq p\). Fix a
\(\mathbb P\)-name

\[
\dot d:[B]^3\longrightarrow r,
\]

where \(r<\omega\) and \(B\subseteq\delta\) has order type \(\omega_1\).

The eventual goal is to define, in \(V^{\mathbb P}\), a ccc forcing \(\dot Q\) which
adds an uncountable \(W\subseteq B\) and a function

\[
H:\operatorname{Typ}_3\longrightarrow r
\]

such that

\[
\dot d(a)=H(\operatorname{tp}(F[a]))
\qquad(a\in[W]^3).
\]

The material below establishes the finite canonical seed and its packet tables. It
does not by itself prove the ccc theorem.

## 2. The Stage-B support system

For each finite \(s\subseteq B\), Stage B supplies a model \(N_s\) and its forcing
support

\[
b_s=N_s\cap\delta.
\]

Only the following properties of this system are used here.

### 2.1 Exact intersections

For finite \(s,t\subseteq B\),

\[
b_s\cap b_t=b_{s\cap t}.
\tag{2.1}
\]

Consequently,

\[
u\subseteq s\quad\Longrightarrow\quad b_u\subseteq b_s.
\tag{2.2}
\]

Put

\[
\mathbb P_s=\operatorname{Add}(\omega,b_s)
=\operatorname{Fn}(b_s\times\omega,2,{<}\omega).
\]

### 2.2 Isomorphisms

If \(s,t\subseteq B\) have the same cardinality, let

\[
\bar h_{s,t}:t\longrightarrow s
\]

be the order-preserving bijection. Stage B supplies an isomorphism, also denoted
by

\[
h_{s,t}:N_t\longrightarrow N_s,
\]

which induces

\[
h_{s,t}:b_t\longrightarrow b_s
\]

and hence

\[
h_{s,t}:\mathbb P_t\longrightarrow\mathbb P_s.
\]

These maps commute with passage to faces: if \(u\subseteq t\), then

\[
h_{s,t}[b_u]=b_{\bar h_{s,t}[u]},
\tag{2.3}
\]

and the restriction of \(h_{s,t}\) to \(b_u\) is the corresponding face map.
They also preserve the coloring name:

\[
h_{s,t}\bigl(\dot d(u)\bigr)
=\dot d\bigl(\bar h_{s,t}[u]\bigr)
\qquad(u\in[t]^3).
\tag{2.4}
\]

### 2.3 The branch code

Fix an injection

\[
F:B\longrightarrow2^\omega
\]

such that every basic cone contains \(\aleph_1\) points of \(F[B]\):

\[
\left|\{\alpha\in B:\eta\subseteq F(\alpha)\}\right|=\aleph_1
\qquad(\eta\in2^{<\omega}).
\tag{2.5}
\]

Since \(B\) has order type \(\omega_1\), the set in (2.5) is unbounded in \(B\).

## 3. Cohen finite diagrams

Let \(A\subseteq B\) be finite, and let \(\mathcal K\subseteq[A]^{\leq3}\) be
closed under taking subsets.

### 3.1 Coherent diagrams

A Cohen diagram on \(\mathcal K\) is a family

\[
\bar p=\langle p_s:s\in\mathcal K\rangle
\]

such that

\[
p_s\in\mathbb P_s
\tag{3.1}
\]

and

\[
p_s\restriction b_u=p_u
\qquad(u\subseteq s, u,s\in\mathcal K).
\tag{3.2}
\]

The diagram is equivariant when every designated isomorphism of its labelled
faces carries the condition on one face to the condition on the corresponding
face.

### 3.2 Assembly

For a finite coherent diagram, define

\[
c(\bar p)=\bigcup_{s\in\mathcal K}p_s.
\tag{3.3}
\]

This is a Cohen condition. Indeed, if \(s,t\in\mathcal K\), then by (2.1) and
(3.2),

\[
p_s\restriction(b_s\cap b_t)
=p_{s\cap t}
=p_t\restriction(b_s\cap b_t).
\]

Thus the functions in (3.3) agree wherever their domains overlap.

### 3.3 Boundaries and interiors

For \(s\in[A]^{\leq3}\), put

\[
b_s^\circ=b_s\setminus\bigcup_{u\subsetneq s}b_u.
\]

If \(s\neq t\), then

\[
b_s^\circ\cap b_t^\circ=\varnothing.
\tag{3.4}
\]

Indeed, \(b_s\cap b_t=b_{s\cap t}\), which is contained in the proper-face
boundary of both \(s\) and \(t\).

In particular, distinct triple interiors are disjoint. All interaction between
two triple conditions occurs on their common proper faces.

### 3.4 Boundary absorption

Suppose \(t\in[A]^3\), \(p_t\in\mathbb P_t\), and

\[
p_t\restriction b_u=p_u
\qquad(u\subsetneq t).
\]

Let \(\langle q_u:u\subsetneq t\rangle\) be coherent and satisfy

\[
q_u\supseteq p_u
\qquad(u\subsetneq t).
\]

Then

\[
q_t=p_t\cup\bigcup_{u\subsetneq t}q_u
\tag{3.5}
\]

is a condition extending \(p_t\). Hence, if \(p_t\) decides a statement, then
\(q_t\) makes the same decision.

### 3.5 Diagram extension

The finite-diagram extension relation is finer than ordinary Cohen extension.
An extension may strengthen old faces and add new faces, but every old
restriction equation and every designated transport equation must remain true.

The finite simultaneous-absorption lemma says that finitely many prescribed
face strengthenings may be inserted simultaneously provided that all their
restrictions and transported restrictions agree on every common support. In the
Cohen case, the resulting conditions are their unions.

## 4. Coherent and decisive systems

For \(n<\omega\), let

\[
I_n=
\left\{
s\in[B]^{<\omega}:
\alpha\neq\beta\in s
\Longrightarrow
F(\alpha)\restriction n\neq F(\beta)\restriction n
\right\}.
\]

If

\[
s=\{\alpha_0<\cdots<\alpha_{k-1}\},
\qquad
t=\{\beta_0<\cdots<\beta_{k-1}\},
\]

write \(s\equiv_F^n t\) when

\[
F(\alpha_i)\restriction n=F(\beta_i)\restriction n
\qquad(i<k).
\tag{4.1}
\]

### 4.1 The class \(R_n^{-}\)

A member \(x\in R_n^{-}\) is a family

\[
x=\langle p_s^x:s\in I_n\rangle
\]

such that

\[
p_s^x\in\mathbb P_s,
\tag{4.2}
\]

\[
p_s^x\restriction b_u=p_u^x
\qquad(u\subseteq s),
\tag{4.3}
\]

and

\[
h_{s,t}(p_t^x)=p_s^x
\qquad(s\equiv_F^n t).
\tag{4.4}
\]

Thus \(R_n^{-}\) consists of coherent, equivariant systems without a decision
requirement.

### 4.2 The class \(R_n\)

A member \(x\in R_n^{-}\) belongs to \(R_n\) when, for every
\(t\in I_n\cap[B]^3\), there is \(c_t^x<r\) such that

\[
p_t^x\Vdash\dot d(t)=c_t^x.
\tag{4.5}
\]

Thus \(R_n\) consists of the decisive systems.

### 4.3 Extension

If \(x\in R_n^{-}\) and \(y\in R_m^{-}\), where \(n\leq m\), write

\[
x\preccurlyeq y
\]

when \(y\) is the stronger system, namely

\[
p_t^y\supseteq p_s^x
\]

whenever \(s\in I_n\), \(t\in I_m\), and \(s\subseteq t\).

### 4.4 The extension facts

The following have been established by the Cohen finite-diagram calculus.

1. **Single-face absorption, \(D(\alpha)\).** If \(x\in R_n^{-}\),
   \(t\in I_n\), and \(q\in\mathbb P_t\) extends \(p_t^x\), there is
   \(y\in R_n^{-}\) such that

   \[
   x\preccurlyeq y
   \qquad\text{and}\qquad
   p_t^y=q.
   \]

   All copies required by (4.4) are strengthened simultaneously.

2. **Finite assembly, \(D(\beta)\).** The union of the conditions on all faces
   of a fixed finite set is a Cohen condition on the union of their supports.

3. **Persistence, \(D(\gamma)\).** If \(x\in R_n\), \(y\in R_n^{-}\), and
   \(x\preccurlyeq y\), then \(y\in R_n\). Old decisions persist under
   strengthening.

4. **Decisive lifting, \(D(\delta)\).** If \(x\in R_n^{-}\) and \(m>n\),
   there is \(y\in R_m\) such that \(x\preccurlyeq y\).

For \(D(\delta)\), there are only finitely many \(\equiv_F^m\)-classes of
triples. Choose one representative of each class, decide its color, and apply
\(D(\alpha)\) after each decision. Equivariance supplies the decisions on the
remaining members of the class.

## 5. Skew-tree combinatorics

### 5.1 Skew trees

A finite tree \(U\subseteq2^{<\omega}\) is skew if it is closed under initial
segments and, at each length, at most one node of \(U\) has two immediate
successors in \(U\). Its terminal set is denoted by \(L(U)\).

A strong embedding between finite skew trees preserves initial segments,
incomparability, the two successor directions, lexicographic order, and the
relative order of splitting levels. Unary padding may change the numerical
lengths of nodes.

The canonical tree \(T_k^*\) has \(2^k\) terminal nodes. To pass from
\(T_k^*\) to \(T_{k+1}^*\), list the terminal nodes of \(T_k^*\) in the
prescribed order and split them one at a time at \(2^k\) successive levels,
using unary padding on every other active branch. Thus exactly one node splits
at each new level.

### 5.2 Ordinary triple type

Let

\[
a=\{\alpha_0<\alpha_1<\alpha_2\}\in[B]^3.
\]

Let \(\pi_a\in S_3\) satisfy

\[
F(\alpha_{\pi_a(0)})
<_{\mathrm{lex}}
F(\alpha_{\pi_a(1)})
<_{\mathrm{lex}}
F(\alpha_{\pi_a(2)}).
\]

Put

\[
v_0=F(\alpha_{\pi_a(0)})\wedge F(\alpha_{\pi_a(1)}),
\]

\[
v_1=F(\alpha_{\pi_a(1)})\wedge F(\alpha_{\pi_a(2)}).
\]

For a skew triple, \(v_0\neq v_1\). Let \(\tau_a\in S_2\) satisfy

\[
v_{\tau_a(0)}\triangleleft v_{\tau_a(1)},
\]

where \(\triangleleft\) is the shortlex order on \(2^{<\omega}\). Define

\[
\operatorname{tp}(a)=(\pi_a,\tau_a).
\tag{5.1}
\]

Hence

\[
\operatorname{Typ}_3=S_3\times S_2
\]

has \(3!\cdot2!=12\) elements.

The finite-prefix similarity lemma says that, once \(m\) lies above all pairwise
splitting levels, two ordered skew triples have the same type (5.1) if and only
if their length-\(m\) prefix triples have the corresponding Shelah similarity
type for the lexicographic well-orders. Only the forward implication is needed
below.

### 5.3 Rooted continuation types

For \(j=1,2,3\), let \(\mathcal C_j\) be the finite set of rooted construction
types of \(j\) vertices that can occur in one canonical split. A rooted type
records the distinguished old faces, wing labels, vertex order, and the finite
splitting data used to identify those faces.

Formally, if \(a:i\to j\) is an increasing injection, there is a restriction map

\[
a^*:\mathcal C_j\longrightarrow\mathcal C_i,
\]

and

\[
(a\circ b)^*=b^*\circ a^*.
\tag{5.2}
\]

There is a forgetful map

\[
\operatorname{otp}:\mathcal C_3\longrightarrow\operatorname{Typ}_3
\tag{5.3}
\]

which forgets the roots and earlier splitting history.

Choose a finite skew tree \(U\), with a fixed ordering of \(L(U)\), containing a
representative of every member of \(\mathcal C_3\). Since \(\mathcal C_3\) is
finite, such a \(U\) is obtained by placing finite representatives in disjoint
cones and assigning distinct lengths to their splitting nodes. In particular,
every member of \(\operatorname{Typ}_3\) occurs among the terminal triples of
\(U\).

## 6. The canonization input

For each \(m<\omega\), use the lexicographic order as the fixed well-order
\(<_m^*\) of \(2^m\).

The exact external theorem used is Sh:288, Theorem 2.7(3): for every finite
\(s\) and every

\[
C:\bigcup_{m<\omega}[2^m]^3\longrightarrow s,
\]

there is \(T\in\operatorname{Per}^{\mathrm{fe}}(2^{<\omega})\) such that, on
every splitting level of \(T\), Shelah-similar triples receive the same
\(C\)-value.

No rooted version of this theorem is used. No prescribed branch or prescribed
vertex is retained by canonization.

## 7. The ambient canonical-seed lemma

### Lemma

For every \(p\in\mathbb P\), there are \(m<\omega\), \(y\in R_m\), a finite
\(A\in I_m\), and

\[
H:\operatorname{Typ}_3\longrightarrow r
\]

such that:

1. \(F[A]\restriction m\) realizes the fixed universal skew tree \(U\);
2. for every \(t\in[A]^3\),

   \[
   p_t^y\Vdash
   \dot d(t)=H(\operatorname{tp}(t));
   \tag{7.1}
   \]

3. \(p\) is compatible with

   \[
   c(y,A)=\bigcup_{s\in[A]^{\leq3}}p_s^y.
   \tag{7.2}
   \]

### Proof

#### Step 1: isolate the nonroot support of \(p\)

Let

\[
\operatorname{supp}(p)
=\{\gamma<\delta:(\gamma,k)\in\operatorname{dom}(p)
\text{ for some }k<\omega\}.
\]

Suppose that \(\gamma\in b_s\) for some finite \(s\subseteq B\). Define

\[
u_\gamma=
\bigcap\{s\in[B]^{<\omega}:\gamma\in b_s\}.
\tag{7.3}
\]

This intersection is attained. Fix \(s_0\) with \(\gamma\in b_{s_0}\). For each
\(\xi\in s_0\setminus u_\gamma\), choose \(s_\xi\) such that

\[
\gamma\in b_{s_\xi}
\qquad\text{and}\qquad
\xi\notin s_\xi.
\]

Then

\[
u_\gamma=s_0\cap
\bigcap_{\xi\in s_0\setminus u_\gamma}s_\xi,
\]

so (2.1) gives \(\gamma\in b_{u_\gamma}\). It follows from (2.2) that

\[
\gamma\in b_s
\quad\Longleftrightarrow\quad
u_\gamma\subseteq s.
\tag{7.4}
\]

Let

\[
E=\bigcup\{u_\gamma:
\gamma\in\operatorname{supp}(p),\
(\exists s\in[B]^{<\omega})\,\gamma\in b_s,\
u_\gamma\neq\varnothing\}.
\tag{7.5}
\]

This is a finite subset of \(B\). If \(A\subseteq B\setminus E\), then, for every
\(s\subseteq A\),

\[
\operatorname{supp}(p)\cap b_s
=\operatorname{supp}(p)\cap b_\varnothing.
\tag{7.6}
\]

#### Step 2: insert the root part of \(p\)

Put

\[
q=p\restriction b_\varnothing.
\]

Start with the empty system in some \(R_n^{-}\). Apply \(D(\alpha)\) at the empty
face to obtain \(x_n\in R_n^{-}\) with

\[
p_\varnothing^{x_n}\supseteq q.
\tag{7.7}
\]

Apply \(D(\delta)\) recursively to obtain

\[
x_m\in R_m
\qquad(m>n)
\]

such that

\[
x_n\preccurlyeq x_{n+1}\preccurlyeq x_{n+2}\preccurlyeq\cdots.
\tag{7.8}
\]

In particular,

\[
p_\varnothing^{x_m}\supseteq q
\qquad(m>n).
\tag{7.9}
\]

#### Step 3: define the tree coloring

Fix \(m>n\). For an ordered triple of distinct nodes

\[
\bar\eta=(\eta_0,\eta_1,\eta_2)\in(2^m)^3,
\]

choose

\[
\alpha_0<\alpha_1<\alpha_2
\]

such that

\[
F(\alpha_i)\restriction m=\eta_i
\qquad(i<3).
\tag{7.10}
\]

This is possible by (2.5). Let \(j_m(\bar\eta)<r\) be the value forced by

\[
p_{\{\alpha_0,\alpha_1,\alpha_2\}}^{x_m}.
\]

The value does not depend on the chosen \(\alpha_i\)'s: two choices give
\(\equiv_F^m\)-equivalent triples, and (2.4) and (4.4) carry one decision to the
other.

For \(a\in[2^m]^3\), write

\[
a=\{\eta_0^a<_{\mathrm{lex}}\eta_1^a
<_{\mathrm{lex}}\eta_2^a\}
\]

and define

\[
C_m(a)=
\left\langle
j_m(\eta_{\pi(0)}^a,
      \eta_{\pi(1)}^a,
      \eta_{\pi(2)}^a):
\pi\in S_3
\right\rangle.
\tag{7.11}
\]

Thus \(C_m\) takes values in the finite set \(r^{S_3}\). The six coordinates
are necessary because the increasing ordinal order of a triple need not agree
with the lexicographic order of its three tree nodes.

Give \(C_m\) arbitrary values for \(m\leq n\), and put

\[
C=\bigcup_{m<\omega}C_m.
\]

#### Step 4: canonize and select \(A\)

Apply Sh:288, Theorem 2.7(3), to \(C\). Obtain

\[
T\in\operatorname{Per}^{\mathrm{fe}}(2^{<\omega})
\]

on whose splitting levels \(C\) is constant on similarity classes.

Choose a splitting level \(m>n\) containing the terminal set

\[
Z=\{z_0,\ldots,z_{k-1}\}
\]

of a strong copy of \(U\), indexed according to the fixed ordering of \(L(U)\).
Using (2.5), choose recursively

\[
\alpha_0<\cdots<\alpha_{k-1}
\]

such that

\[
\alpha_i\in B\setminus E
\qquad\text{and}\qquad
F(\alpha_i)\restriction m=z_i.
\tag{7.12}
\]

Put

\[
A=\{\alpha_i:i<k\}
\qquad\text{and}\qquad
y=x_m.
\]

If \(t,t'\in[A]^3\) have the same ordinary type, the finite-prefix similarity
lemma shows that their prefix triples are Shelah-similar. Their \(S_3\)
coordinates select the same coordinate in (7.11). Hence

\[
c_t^y=c_{t'}^y.
\tag{7.13}
\]

Define

\[
H(\rho)=c_t^y
\]

for any \(t\in[A]^3\) of type \(\rho\). Every type occurs in \(U\), and (7.13)
shows that \(H\) is well defined. This proves (7.1).

#### Step 5: verify compatibility with \(p\)

By (3.3), \(c(y,A)\) is a Cohen condition. If a coordinate of \(p\) also occurs
in \(c(y,A)\), then it belongs to \(b_s\) for some \(s\subseteq A\). Since
\(A\cap E=\varnothing\), equation (7.6) places it in \(b_\varnothing\). On
\(b_\varnothing\), the condition \(c(y,A)\) extends
\(q=p\restriction b_\varnothing\) by (7.9). Therefore \(p\) and \(c(y,A)\)
agree on their common domain, and

\[
p\cup c(y,A)
\]

is their common Cohen extension.

This proves the lemma.

## 8. Packet completion

The packet-completion step introduces no new forcing construction. It extracts
finite continuation tables from the canonical seed.

### 8.1 Triple packets

For each \(\rho\in\mathcal C_3\), choose an order-preserving injection

\[
e_\rho:3\longrightarrow A
\]

whose range \(t_\rho\) realizes \(\rho\). Define

\[
D_3(\rho)=
\left\langle
p^y_{e_\rho[u]}:u\subseteq3
\right\rangle.
\tag{8.1}
\]

This is a complete coherent face diagram, and

\[
p^y_{t_\rho}\Vdash
\dot d(t_\rho)=H(\operatorname{otp}(\rho)).
\tag{8.2}
\]

### 8.2 Pair and vertex tables

For \(\sigma\in\mathcal C_2\), define

\[
D_2(\sigma)=
\left\{
(\rho,a,D_3(\rho)):
\rho\in\mathcal C_3,
\ a:2\to3\text{ increasing},
\ a^*(\rho)=\sigma
\right\}.
\tag{8.3}
\]

For \(\lambda\in\mathcal C_1\), define

\[
D_1(\lambda)=
\left\{
(\sigma,b,\rho,a,D_3(\rho)):
b:1\to2\text{ increasing},\quad
b^*(\sigma)=\lambda,\quad
(\rho,a,D_3(\rho))\in D_2(\sigma)
\right\}.
\tag{8.4}
\]

The objects \(D_1(\lambda)\) and \(D_2(\sigma)\) are finite lookup tables. They
are not forcing conditions and do not choose a color before the full rooted
triple type is known. When \(\rho\) is realized, it selects the entry
\(D_3(\rho)\).

### 8.3 Transport and absorption

Let \(t=\{\beta_0<\beta_1<\beta_2\}\) realize \(\rho\), and write

\[
t_\rho=\{\alpha_0<\alpha_1<\alpha_2\}.
\]

Transport the entire packet by the single Stage-B isomorphism which sends
\(\alpha_i\) to \(\beta_i\):

\[
D_3(\rho;t)=h_{t,t_\rho}[D_3(\rho)].
\tag{8.5}
\]

Because the Stage-B maps commute with face restrictions, this is coherent, and
its top forces

\[
\dot d(t)=H(\operatorname{otp}(\rho)).
\tag{8.6}
\]

If coherent proper-face conditions \(q_u\), \(u\subsetneq t\), extend the
corresponding faces of (8.5), then boundary absorption gives

\[
q_t=operatorname{top}(D_3(\rho;t))
\cup\bigcup_{u\subsetneq t}q_u.
\tag{8.7}
\]

This is a condition extending the decisive top, so it still forces (8.6).

Equations (8.1)--(8.7) are the packet-completion lemma. Once the canonical seed
has been obtained using a \(U\) universal for \(\mathcal C_3\), packet completion
is settled.

## 9. Interface with the remainder of the proof

The canonical seed and packet tables supply the following data to the repaired
game:

1. a fixed palette \(H:\operatorname{Typ}_3\to r\);
2. decisive witnesses \(D_3(\rho)\) for every rooted triple continuation;
3. the lower-dimensional lookup tables \(D_1,D_2\);
4. persistence of every installed decision under coherent proper-face
   strengthening.

A later working condition \(x\) has a finite protected set \(u_x\subseteq B\);
these are the vertices already committed to the generic set \(W\). It may also
have a finite excluded set \(z_x\subseteq B\), disjoint from \(u_x\). The
condition \(c(x)\in\mathbb P\) is the Cohen condition assembled from the
selected face diagram.

The next step is the prepared-output one-split lemma. Its input must require
Player II's proper-face changes to be coherent, equivariant, and to extend the
faces of the packet entries selected by the current continuation data. Its
remaining assertion is genuinely simultaneous: all packets chosen during one
split must be transported so that their prescriptions agree on every shared
face. Distinct triple interiors may then be inserted independently by (3.4),
and (8.7) preserves the palette.

Once the one-split lemma is proved, the remaining outline is:

1. iterate the one-split lemma in the canonical order defining
   \(T_k^*\to T_{k+1}^*\), obtaining Player I's winning strategy;
2. prove the finite twin-extension lemma for overlap-compatible structural
   twins;
3. define the working forcing and

   \[
   Q^*=\{(r,x):r\supseteq c(x)\};
   \]

4. prove promotion density, adding protected vertices above every prescribed
   bound;
5. prove Knaster by \(\Delta\)-system thinning, common refinement of the root
   diagrams, and the twin-extension lemma;
6. pass to the relative quotient and conclude that
   \(\mathbb P\Vdash\dot Q\) is ccc;
7. let \(W\) be the union of the protected sets in the generic filter and use
   promotion density to show \(|W|=\aleph_1\);
8. use the fixed palette to conclude

   \[
   \dot d(a)=H(\operatorname{tp}(F[a]))
   \qquad(a\in[W]^3),
   \]

   and hence

   \[
   |\dot d``[W]^3|\leq12.
   \]

### Proof-status boundary

The material through packet completion is established relative to the Stage-B
support system, the Cohen finite-diagram lemmas, \(D(\alpha)\)--\(D(\delta)\),
the finite-prefix similarity lemma, and Sh:288, Theorem 2.7(3). No rooted form
of Halpern--Läuchli is assumed.

The simultaneous one-split lemma and the later twin-extension and Knaster
arguments remain the next proof obligations. They should not be folded back
into, or treated as missing parts of, packet completion.
