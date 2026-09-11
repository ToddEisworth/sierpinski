# The skew-tree game

The game has length $\omega$. At round $k$, Player I plays

$$
(m_k,\mathcal P_k,T_k),
$$

where:

1. $\mathcal P_k$ is a coherent system on the full level $2^{m_k}$, deciding every ordered $n$-tuple;
2. $T_k$ is a finite skew tree whose maximal nodes lie in $2^{m_k}$;
3. for $k>0$, $m_k>m_{k-1}$ and $T_k$ end-extends $T_{k-1}$, with every old maximal node having two incompatible extensions in $T_k$;
4. if $x,y\in[\operatorname{Max}(T_k)]^n$ are $\Delta$-similar, then $\vec c(x)=\vec c(y)$;

5. for $k>0$, $\mathcal P_k$ extends Player II's preceding move; descendants of an already resolved tuple extend its deciding condition.

Player II responds with any coherent strengthening $\mathcal P_k'$ of the entire system, leaving the resolution and tree unchanged. Player I chooses the initial system and tree and wins by playing through all rounds.

!!! proposition "Winning strategy"

    Player I has a winning strategy.

**Proof.** The game is determined, since II wins only when I gets stuck after finitely many moves. Suppose II has a winning strategy $\tau$.

For each $m<\omega$, we will construct a coherent family $\mathcal R_m$ deciding every $n$-tuple from $2^m$ in every orientation. Thus, for each set of $n$ elements and each permutation of its vertex data, $\mathcal R_m$ contains a condition extending a member of the color-deciding antichain. We require $\mathcal R_{m+1}$ to extend $\mathcal R_m$, so all earlier decisions persist.

At the same time, we maintain a finite set $\Phi_m$ of finite partial plays following $\tau$. We require that $\Phi_m\subseteq\Phi_{m+1}$, that the empty play belongs to every $\Phi_m$, and that $\mathcal R_m$ extends the last reply by II in every play in $\Phi_m$.

We do this as follows. Start with the empty play. Given $\mathcal R_m$ and $\Phi_m$, extend $\mathcal R_m$ coherently to level $m+1$ and decide every new $n$-element subset in every orientation. Consider, in turn, every $y\in\Phi_m$ and every finite skew tree $T\subseteq 2^{\leq m+1}$ whose maximal nodes lie in $2^{m+1}$. If the current family together with $T$ is a legal move by I after $y$, add that move and $\tau$’s reply to $\Phi_{m+1}$, and replace the current family by $\tau$’s reply. After all such pairs have been considered, the resulting family is $\mathcal R_{m+1}$.

This induces a coloring

$$
c:\bigcup_{m<\omega}[2^m]^n\longrightarrow \sigma^{n!},
$$

where $c(x)$ records the colors decided by $\mathcal R_m$ for the $n!$ permutations of the vertex data on $x\in[2^m]^n$.

Apply the skew canonization theorem to obtain a perfect skew subtree $S\subseteq2^{<\omega}$ on which $c$ depends only on $\Delta$-similarity. The finite initial segments of $S$ then determine an infinite play following $\tau$ in which I always has a legal move, contradicting that $\tau$ is winning for II.

$$
\tag*{$\square$}
$$

