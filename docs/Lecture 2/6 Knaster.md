# Property K

!!! Theorem  $\mathbb{Q}^*$ is Knaster.


**Proof.** Take an uncountable family

$$
\{(p_\xi,s_\xi):\xi<\omega_1\}\subseteq\mathbb Q^*,
$$

and choose the spare interior conditions witnessing membership in $\mathbb Q^*$.

By standard $\Delta$-system thinning, assume:

* the $s_\xi$ form a $\Delta$-system and have the same finite pattern;
* the canonical maps between them preserve all vertex, segment, and spare interior data;
* the Cohen conditions $p_\xi$ have $\Delta$-system supports and agree on their common support;
* every new cross-segment interior between two different petals avoids both Cohen supports.

Fix $\xi<\zeta$. Then

$$
p_\xi\cup p_\zeta
$$

is a Cohen condition. We extend the finite system to $s_\xi\cup s_\zeta$. 


For a cross pair whose vertices occupy different positions, copy the corresponding old segment data, using the spare interior condition if the orientation is reversed. For a cross pair whose vertices occupy the same position, apply the splitting lemma to their common vertex condition. Strengthen the resulting vertex conditions further, if necessary, so that they remain splittable.

The new interior conditions lie on mutually disjoint cross-segment interiors and avoid $\operatorname{supp}(p_\xi)\cup\operatorname{supp}(p_\zeta)$. Hence all the chosen data have a common Cohen extension $q$. Old decisions and spare decisions persist under the vertex strengthenings, so

$$
(q,s_\xi\cup s_\zeta)\in\mathbb Q^*
$$

and extends both original conditions. Thus every two conditions in the thinned uncountable family are compatible, and $\mathbb Q^*$ is Knaster. $\square$
