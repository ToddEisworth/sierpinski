# Tree Terminology and Conventions

## The binary tree

Let

\[
2^{<\omega}=\bigcup_{m<\omega}2^m.
\]

For \(s,t\in 2^{<\omega}\), write

\[
s\unlhd t
\]

if \(s\) is an initial segment of \(t\), and

\[
s\lhd t
\]

if \(s\unlhd t\) and \(s\neq t\).

The length of \(s\) is denoted by \(|s|\).

## Meet and splitting level

For \(s,t\in 2^{<\omega}\), let

\[
s\wedge t
\]

be their longest common initial segment.

For distinct \(s,t\),

\[
\Delta(s,t)=|s\wedge t|.
\]

The same notation is used for \(x,y\in 2^\omega\).

## Lexicographic order

For distinct \(s,t\in 2^{<\omega}\) which are incomparable under \(\unlhd\),

\[
s<_{\mathrm{lex}}t
\]

if

\[
s(\Delta(s,t))<t(\Delta(s,t)).
\]

The same convention is used on \(2^\omega\).

## Cones

For \(s\in 2^{<\omega}\), define

\[
[s]=\{x\in 2^\omega:s\unlhd x\}.
\]

## Leveled configurations

A finite set \(a\subseteq 2^{<\omega}\) is **leveled** if

\[
(\exists m<\omega)\;a\subseteq 2^m.
\]

An ordered leveled \(n\)-tuple is a tuple

\[
(s_0,\dots,s_{n-1})
\]

of distinct members of a common level \(2^m\).

## Level colorings

An \(n\)-dimensional **level coloring** is a map

\[
d:\bigcup_{m<\omega}[2^m]^n\longrightarrow r
\]

for some finite \(r\).

## Strong subtrees

A subtree \(S\subseteq 2^{<\omega}\) is **strong** if there is a strictly increasing sequence

\[
\ell_0<\ell_1<\cdots
\]

such that:

1. the \(k\)-th level of \(S\) is contained in \(2^{\ell_k}\);
2. if \(s\) is on the \(k\)-th level of \(S\), then extending each of \(s^\frown 0\) and \(s^\frown 1\) there is exactly one node on the \((k+1)\)-st level of \(S\).

The set

\[
L(S)=\{\ell_k:k<\omega\}
\]

is the **level set** of \(S\).

## Skew trees

A subtree \(T\subseteq 2^{<\omega}\) is **skew** if each ambient level contains at most one splitting node.
