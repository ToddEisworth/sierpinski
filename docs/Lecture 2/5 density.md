# A Density Lemma

### Lemma

For every \(\gamma<\sup B\), the set

$$
D_\gamma
=
\{(p,s)\in\mathbb Q^*:s\cap(B\setminus\gamma)\neq\emptyset\}
$$

is dense in \(\mathbb Q^*\).

**Proof.** Fix \((p,s)\in\mathbb Q^*\). If \(s=\emptyset\), choose \(\beta\in B\setminus\gamma\) whose vertex support avoids \(\operatorname{supp}(p)\), and add a splittable vertex condition at \(\beta\).

Suppose \(s\neq\emptyset\), and choose \(\alpha\in s\). Choose

$$
\beta\in B\setminus\gamma
$$

above \(s\) so that the new vertex and segment interiors avoid \(\operatorname{supp}(p)\). This is possible by (CL3), since \(p\) has finite support.

Apply the splitting lemma to the vertex condition at \(\alpha\). Place one resulting extension at \(\alpha\) and a copy of the other at \(\beta\); strengthen them further, if necessary, so that both are splittable. The splitting lemma supplies the two oriented interior conditions for \(\{\alpha,\beta\}\).

For each \(\delta\in s\setminus\{\alpha\}\), copy the segment data for \(\{\alpha,\delta\}\) to \(\{\beta,\delta\}\). If the order of the vertices is reversed, use the spare interior condition instead. Persistence ensures that these copied decisions remain valid after strengthening the vertex conditions.

The new interiors are mutually disjoint and avoid \(\operatorname{supp}(p)\), so their union with \(p\) is a Cohen condition \(q\). Then

$$
(q,s\cup\{\beta\})\leq(p,s)
$$

and belongs to \(D_\gamma\). \(\square\)

Consequently, the quotient generic union is unbounded in \(B\), hence uncountable. Its pairs receive only the colors \(i\) and \(j\).
