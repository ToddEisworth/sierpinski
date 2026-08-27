# The Ambient Seed-Density Lemma

## 1. Assumptions

Fix

\[
P=\operatorname{Add}(\omega,\delta),
\]

ordered so that \(q\leq p\) means that \(q\) extends \(p\), and fix a
\(P\)-name

\[
\dot d:[B]^3\longrightarrow r,
\qquad r<\omega.
\]

We use the following data from the preceding sections.

### 1.1 Supports and isomorphisms

For every \(s\in[B]^{\leq 3}\), there is a countable support

\[
b_s\subseteq\delta,
\]

and

\[
b_s\cap b_t=b_{s\cap t}.
\tag{1.1}
\]

Whenever \(s\) and \(t\) have the same Stage-B type, there is an
isomorphism

\[
h_{s,t}:P_{b_t}\longrightarrow P_{b_s}
\]

which commutes with restrictions and satisfies

\[
h_{s,t}(\dot d(t))=\dot d(s).
\tag{1.2}
\]

### 1.2 Coding map

There is an injection

\[
F:B\longrightarrow2^\omega
\]

such that, for every \(\eta\in2^{<\omega}\),

\[
\bigl|\{\alpha\in B:\eta\trianglelefteq F(\alpha)\}\bigr|=\aleph_1.
\tag{1.3}
\]

For each \(m<\omega\), fix the order \(<^*_m\) on \(2^m\) used in the
definition of Shelah similarity.

### 1.3 Coherent decisive systems

For \(m<\omega\), let

\[
I_m=\left\{s\in[B]^{\leq3}:
\alpha\neq\beta\in s\Longrightarrow
F(\alpha)\restriction m\neq F(\beta)\restriction m
\right\}.
\]

A member \(x\in R_m\) supplies conditions

\[
\langle p_s^x:s\in I_m\rangle
\]

such that

\[
p_s^x\restriction b_{s\cap t}
=p_t^x\restriction b_{s\cap t},
\tag{1.4}
\]

\[
s\equiv_F^m t
\Longrightarrow
h_{s,t}(p_t^x)=p_s^x,
\tag{1.5}
\]

and every triple component decides the coloring:

\[
\forall s\in I_m\cap[B]^3\ \exists j_s<r\
\bigl(p_s^x\Vdash\dot d(s)=j_s\bigr).
\tag{1.6}
\]

We assume the following relative form of the extension facts proved by the
Cohen finite-diagram calculus.

**Relative coherent-decision property.** For every \(p\in P\), there are
systems \(x_m\in R_m\), for all sufficiently large \(m\), such that whenever
\(A\subseteq B\) is finite and \([A]^{\leq3}\subseteq I_m\), the finite
assembly

\[
c(x_m,A)=\bigcup_{s\in[A]^{\leq3}}p_s^{x_m}
\tag{1.7}
\]

is compatible with \(p\).

In the Cohen case, this is the \(p\)-relative form of simultaneous
absorption followed by decision extension: all face extensions are made
compatibly with \(p\), and only finitely many faces are assembled in (1.7).

### 1.4 Triple types and the universal finite pattern

The set of ordinary triple types is

\[
\operatorname{Sim}_3=S_3\times S_2.
\]

Hence

\[
|\operatorname{Sim}_3|=12.
\]

Fix a finite labeled skew tree \(U\) such that every member of
\(\operatorname{Sim}_3\) is realized by a triple of terminal nodes of \(U\).

### 1.5 Canonization

We use Sh:288, Theorem 2.7(3), in the following form. If

\[
c:\bigcup_{m<\omega}[2^m]^3\longrightarrow r,
\]

then there is a synchronized perfect tree \(T\subseteq2^{<\omega}\) such
that, on every splitting level of \(T\), Shelah-similar triples receive the
same \(c\)-color.

We also use the finite skew-embedding fact proved in the skew-tree section:
some splitting level of \(T\) contains a labeled copy of \(L(U)\).

## 2. Statement

**Ambient Seed-Density Lemma.** For every \(p\in P\), there exist

- a finite set \(A\subseteq B\) whose \(F\)-pattern realizes \(U\);
- a coherent decisive diagram
  \[
  \bar q=\langle q_s:s\in[A]^{\leq3}\rangle;
  \]
- a function
  \[
  H:\operatorname{Sim}_3\longrightarrow r;
  \]
- a condition \(p'\in P\);

such that

\[
p'\leq p,
\tag{2.1}
\]

\[
p'\leq c(\bar q),
\tag{2.2}
\]

and, for every \(t\in[A]^3\),

\[
q_t\Vdash
\dot d(t)=H\bigl(\operatorname{tp}(F[t])\bigr).
\tag{2.3}
\]

Thus conditions carrying a finite canonical seed are dense in \(P\).

## 3. Proof

Fix \(p\in P\), and choose systems \(x_m\in R_m\), for all sufficiently
large \(m\), witnessing the relative coherent-decision property.

### 3.1 Define the level coloring

Let \(m\) be sufficiently large and let

\[
\eta_0<^*_m\eta_1<^*_m\eta_2
\]

be distinct members of \(2^m\). By (1.3), choose

\[
\alpha_0<\alpha_1<\alpha_2
\]

in \(B\) such that

\[
\eta_i\trianglelefteq F(\alpha_i)
\qquad(i<3).
\tag{3.1}
\]

Put \(s=\{\alpha_0,\alpha_1,\alpha_2\}\). By (1.6), there is a unique
\(j<r\) such that

\[
p_s^{x_m}\Vdash\dot d(s)=j.
\]

Define

\[
c(\{\eta_0,\eta_1,\eta_2\})=j.
\tag{3.2}
\]

This is independent of the chosen \(\alpha_i\). Two choices give triples
\(s,t\in I_m\) with

\[
s\equiv_F^m t.
\]

By (1.5),

\[
h_{s,t}(p_t^{x_m})=p_s^{x_m},
\]

and (1.2) shows that the two conditions decide the same member of \(r\).
Therefore (3.2), over all sufficiently large \(m\), defines

\[
c:\bigcup_m[2^m]^3\longrightarrow r.
\]

Define \(c\) arbitrarily on the finitely many omitted initial levels.

### 3.2 Apply canonization and extract the palette

Apply the canonization theorem to \(c\), obtaining a synchronized perfect
tree \(T\). Choose a splitting level \(m\) of \(T\) and a labeled set

\[
E\subseteq T\cap2^m
\]

which realizes \(L(U)\).

For each \(\rho\in\operatorname{Sim}_3\), choose

\[
e_\rho\in[E]^3
\]

of type \(\rho\), and define

\[
H(\rho)=c(e_\rho).
\tag{3.3}
\]

This is well defined. If two triples in \([E]^3\) have the same ordinary
type, the skew-tree analysis identifies them as Shelah-similar; canonization
therefore gives them the same \(c\)-color. Consequently,

\[
c(e)=H(\operatorname{tp}(e))
\qquad(e\in[E]^3).
\tag{3.4}
\]

### 3.3 Realize the finite pattern in \(B\)

Enumerate \(E\) in the order \(<^*_m\) as

\[
E=\{\eta_0<^*_m\cdots<^*_m\eta_{k-1}\}.
\]

Using (1.3), choose

\[
\alpha_0<\cdots<\alpha_{k-1}
\]

such that

\[
\eta_i\trianglelefteq F(\alpha_i)
\qquad(i<k).
\tag{3.5}
\]

Let

\[
A=\{\alpha_i:i<k\}.
\]

The ordering in (3.5), together with the fact that all \(\eta_i\) lie on
one level, ensures that the labeled \(F\)-pattern of \(A\) is the labeled
pattern \(U\).

Set

\[
q_s=p_s^{x_m}
\qquad(s\in[A]^{\leq3}).
\tag{3.6}
\]

Equations (1.4) and (1.5) show that \(\bar q\) is coherent and equivariant.
By the definition of \(c\), (3.4), and (3.5), every \(t\in[A]^3\) satisfies

\[
q_t\Vdash
\dot d(t)=H\bigl(\operatorname{tp}(F[t])\bigr).
\]

### 3.4 Put the seed below the ambient condition

By the relative coherent-decision property,

\[
c(\bar q)=\bigcup_{s\in[A]^{\leq3}}q_s
\]

is compatible with \(p\). Hence

\[
p'=p\cup c(\bar q)
\tag{3.7}
\]

is a Cohen condition. It satisfies

\[
p'\leq p
\qquad\text{and}\qquad
p'\leq c(\bar q).
\]

This proves the lemma.

## 4. Role in the remaining construction

The lemma is applied once below an arbitrary ambient Cohen condition. It
produces:

1. a fixed palette
   \[
   H:\operatorname{Sim}_3\to r;
   \]
2. a finite representative of every one of the \(12\) ordinary triple
   types;
3. coherent forcing conditions witnessing the value prescribed by \(H\) on
   those representatives.

Packet completion enlarges this finite diagram to the rooted face packets
required by the first one-split. Thereafter the one-split lemma must preserve
the invariant

\[
q_t\Vdash
\dot d(t)=H\bigl(\operatorname{tp}(F[t])\bigr)
\]

for every terminal triple \(t\). Old decisions persist under strengthening;
new and mixed triples are handled by transporting the prepared witnesses and
completing them over their already fixed proper faces.

No later stage changes \(H\), and no later application of the canonization
theorem is required.

## 5. Logical boundary

The Ambient Seed-Density Lemma depends on the relative coherent-decision
property in Section 1.3. It does not prove that property. In the Cohen
development, that property must already have been established from finite
simultaneous absorption and decision extension.

Likewise, the lemma produces the initial witnesses for \(H\); the assertion
that the same palette survives every permitted future lower-face
strengthening belongs to the prepared one-split lemma.
