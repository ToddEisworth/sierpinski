# 9. The Prepared-Position Game

## Purpose of the game

The game produces finite skew-tree positions that are simultaneously

- extendible after arbitrary coherent lower-dimensional strengthening;
- canonized by the fixed palette \(H\); and
- suitable for later twin amalgamation.

The interpretation sequence is constructed during the play. It is not fixed in
advance.

## Positions

A position \(x\) contains

\[
x=(T_x,m_x,\bar p^{\,x},H,\mathcal D_x),
\]

where

- \(T_x\) is an allowed finite skew tree;
- \(m_x\) resolves its terminal front;
- \(\bar p^{\,x}\) is a prepared interpretation system at height \(m_x\);
- \(H\) is the fixed ordered-similarity palette; and
- \(\mathcal D_x\) is the finite collection of prepared face tables and unused
  cones required for the next split.

Every represented triple \(t\) satisfies

\[
p_t^x\Vdash
\dot d(t)=H\bigl(\operatorname{simtp}_{\mathrm{ord}}(F[t])\bigr).
\tag{9.1}
\]

## A round of play

The game has length \(\omega\).

1. **Player I** plays a prepared position \(x_n\). Except at the first move,
   this position must extend the data supplied by Player II in the preceding
   round. The skew-tree ranks must tend to infinity.

2. **Player II** chooses a finite coherent strengthening of the proper-face
   data of \(x_n\). Player II may also prescribe an additional finite Cohen
   condition that must be protected.

Player II does not change the tree, the palette \(H\), or an already decided
triple color. The proper-face strengthening is required to respect all overlap
and copying maps.

## Legal responses

A response by Player I is legal if it

- absorbs Player II's face data and finite protection;
- extends the interpretation system to a greater resolution;
- carries out the next permitted skew splitting event;
- seals every new and mixed triple according to \(H\);
- preserves all old decisions; and
- ends in another prepared position.

Player I wins if a legal response is available at every finite stage.

## Structural extension

For later forcing applications, we retain prepared ending states rather than
literal play histories. Write

\[
x\sqsubseteq_\Sigma y
\]

when \(y\) is a structural extension of \(x\) arising from legal moves according
to a strategy \(\Sigma\): the old tree is preserved, old face conditions are
strengthened, and old decisions remain unchanged.

This distinction is important. A common extension of two twin states need not
literally end-extend both play transcripts; it contains canonical copies of
both finite states and satisfies their structural requirements.

!!! note "Central task"

    To prove that Player I wins, it suffices to show that every prepared
    position admits a legal response after every legal move by Player II. This
    is the one-split extension lemma.

**Next:** [The One-Split Extension Lemma](10-one-split-extension.md).
