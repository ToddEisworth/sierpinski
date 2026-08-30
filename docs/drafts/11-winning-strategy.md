# 11. The Winning Strategy

## Initial preparation

By the initial-preparation lemma, choose an \(H\)-invariant prepared position
containing representatives for every ordered similarity type of triples that
can occur in the skew templates. Fix its palette

\[
H:\operatorname{Typ}^{\mathrm{ord}}_3\longrightarrow r.
\]

The palette is never changed later. Subsequent interpretation systems may
refine the conditions, but persistence preserves their decided values.

## Strategy

!!! theorem "Winning-strategy theorem"

    Player I has a winning strategy \(\Sigma\) in the prepared-position game.

**Proof.** Suppose a finite legal play has ended with a prepared position
\(x_n\), and Player II has supplied a legal proper-face strengthening together
with finite Cohen protection.

Apply the relative one-split extension lemma. It produces a prepared position
\(x_{n+1}\) that

- absorbs Player II's move;
- performs the next prescribed skew split;
- seals every new triple according to \(H\); and
- protects all old decisions.

Use this construction as Player I's response. By induction it defines a legal
response after every finite history. Following the prescribed enumeration of
splitting events produces completed templates of unbounded rank. Therefore
Player I never loses and \(\Sigma\) is winning. \(\square\)

## Building interpretations during the play

At stage \(n\), only a finite initial segment of the interpretation sequence is
needed. After Player II's move is known, the resolution-extension lemma builds
the next system and absorbs the new face data. Thus no global interpretation
sequence has to anticipate all possible plays.

Incompatible histories may lead to different later interpretation systems.
Each history nevertheless preserves the same support isomorphisms, the same
old decisions, and the same palette \(H\).

## Consequences used by the forcing

Let \(\mathcal Y_\Sigma\) be the collection of finite prepared states produced
by \(\Sigma\), ordered by structural extension. The strategy gives:

1. **lengthening:** every state has extensions of arbitrarily large skew-tree
   rank;
2. **promotion:** a fresh point of \(B\) above any prescribed bound can be
   introduced;
3. **relative extension:** both operations can be performed below any finite
   compatible Cohen condition; and
4. **persistence:** all old triple decisions continue to satisfy the same
   palette \(H\).

The remaining local issue is amalgamation: two isomorphic prepared states must
have a common structural extension. This is supplied by the twin-extension
lemma.

**Next:** [The Twin-Extension Lemma](12-twin-extension.md).
