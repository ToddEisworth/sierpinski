# 1. Proof Roadmap

## The setting

Let

\[
P=\operatorname{Add}(\omega,\delta),
\]

ordered so that stronger conditions are smaller. Thus \(p\leq q\) means that
\(p\) extends \(q\) as a finite partial function. Let \(B\) have order type
\(\omega_1\), and let

\[
F:B\longrightarrow 2^\omega
\]

be one-to-one, with uncountably many points of \(F[B]\) in every basic open
set that is used in the construction. Fix a \(P\)-name

\[
\dot d:[B]^3\longrightarrow r,
\]

where \(r<\omega\).

Our goal is to define a \(P\)-name \(\dot Q\) such that

1. \(P\Vdash\dot Q\) is Knaster;
2. \(P*\dot Q\) adds an uncountable \(A\subseteq B\); and
3. for a fixed map \(H\) on ordered similarity types,

\[
d(t)=H\bigl(\operatorname{simtp}_{\mathrm{ord}}(F[t])\bigr)
\qquad(t\in[A]^3).
\]

There are at most \(3!2!=12\) ordered similarity types of triples on a skew
binary tree.

## Structure of the proof

The proof has three layers.

### Finite forcing diagrams

A higher-dimensional \(\Delta\)-system supplies supports \(b_s\), canonical
isomorphisms between them, and exact intersections

\[
b_s\cap b_t=b_{s\cap t}.
\]

These properties allow us to treat a finite family of Cohen conditions as a
coherent diagram indexed by faces of finite simplices. Compatible diagrams can
be united, strengthened, and completed.

### Interpretation and the skew-tree game

At each finite resolution height, the canonical isomorphisms produce decisive
conditions indexed by ordered **strong** similarity types. Finite capture then
seals any finite family of triples simultaneously.

The game builds these interpretation systems while also lengthening a skew
tree. Its invariant is stronger: on the tree being constructed, the decisions
already depend only on ordered similarity type. The one-split extension lemma
gives Player I a winning strategy. Its relative form permits arbitrary finite
Cohen information to be protected during an extension.

### The auxiliary forcing

A condition consists of

- a finite prepared position from the winning strategy;
- a finite set of kept points of \(B\); and
- a Cohen condition sealing all triples from those points.

Twin positions can be amalgamated because their lower-dimensional diagrams
agree on overlaps. The winning strategy supplies the missing cross faces, and
finite capture fills the cross-triple interiors. This yields the Knaster
property. Relative one-point extension gives the density needed to make the
generic kept set uncountable.

!!! note "Logical status"

    The construction of the higher-dimensional support system and the finite
    interpretation machinery are the inputs. Everything after the winning
    strategy is an ordinary forcing argument.

**Next:** [Codes and Similarity Types](02-codes-and-similarity-types.md).
