# The Halpern-Lauchli Theorem

We will assume the following version of the Halpern-Lauchli Theorem:

!!! theorem "The Halpern-Lauchli Theorem"

	Let $r<\omega$, let $\sigma<\omega$, and let
	$U_0,\ldots,U_{r-1}$ be perfect strong subtrees of $2^{<\omega}$ having the same splitting levels. Suppose
    
    $$
    d:\bigcup_{\ell\in L} \prod_{i<r}\left(U_i\cap 2^\ell\right)\longrightarrow \sigma,
    $$

	where $L$ is their common set of splitting levels.

	Then there are perfect strong subtrees

	$$
	V_i\subseteq U_i
	\qquad(i<r)
	$$

	and an infinite set $L'\subseteq L$ such that $L'$ is the set of splitting levels of $V_i$ for all $i<r$, and
	there is a color $\varsigma<\sigma$ such that

	$$
	d(\nu_0,\ldots,\nu_{r-1})=\varsigma
	$$

	whenever $\ell\in L'$ and

	$$
	\nu_i\in V_i\cap 2^\ell
	\qquad(i<r).
	$$



Thus, these $V_i\subseteq U_i$ share a common set $L'$ of splitting levels, and  the restriction of $d$ to $\bigcup_{\ell\in L'}\prod_{i<r}(V_i\cap 2^ell)$ is constant with value $\varsigma$.
This is the form of the Halpern-Lauchli Theorem appearing in [Sh288] as Theorem 2.7(1)--(2).  Shelah attributes (1) (the theorem without reference to common splitting levels in the final trees)  to Halpern and Lauchli, notes that Laver obtained the improvement show here, and that Pincus observed that the original Halpern--Lauchli proof can be modified to obtain (2).  Halpern-Lauchli is easier to say, but it should really be known as the HLLMP theorem (including Milliken; see the reference below).


## References

- [Sh288] S. Shelah, *Strong Partition Relations Below the Power Set: Consistency -- Was Sierpiński Right? Vol. II*

- [HL] J. D. Halpern and H. Läuchli, “A Partition Theorem,” *Transactions of the American Mathematical Society* **124** (1966), 360–367.  

- [M] K. R. Milliken, “A Ramsey Theorem for Trees,” *Journal of Combinatorial Theory, Series A* **26** (1979), no. 3, 215–237.  
  
- [T] Todorcevic, Stevo. *Introduction to Ramsey Spaces*. Annals of Mathematics Studies, vol. 174. Princeton, NJ: Princeton University Press, 2010.