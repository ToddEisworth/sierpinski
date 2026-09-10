# Splitting Conditions


!!! lemma "Splitting lemma"

    There are colors $i,j<\sigma$ and a vertex condition $p$ such that densely below $p$, every vertex condition $q$ can be split into extensions $q^0,q^1\leq q$ with the following property: there are interior conditions completing $(q^0,q^1)$ to a segment condition forcing color $i$, and completing $(q^1,q^0)$ to a segment condition forcing color $j$.

    The same interior conditions continue to work after further strengthening $q^0$ and $q^1$.



Note that this is formulated in terms of our basic diamond configuration, but the needed properties are preserved by the isomorphims.

----



**Proof by Exhaustion**

For $i,j<\sigma$, let $D_{i,j}$ be the set of vertex conditions admitting the stated split.

The union of the $D_{i,j}$ is dense. Given a vertex condition $q$, split it into incompatible extensions $q^0,q^1$. Place these on the two vertex faces and extend to a segment condition deciding some color $i$. Retain its interior condition and strengthen $q^0,q^1$ to its vertex projections. Now reverse the two vertices and repeat, obtaining an interior condition deciding some color $j$. The first decision survives these further vertex extensions.

Since there are only finitely many pairs $(i,j)$, an exhaustion argument gives $p$ and $(i,j)$ such that $D_{i,j}$ is dense below $p$. Persistence under further vertex extensions follows because the vertex and interior supports are disjoint. $\square$