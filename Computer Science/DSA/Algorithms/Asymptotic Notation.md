---
tags:
  - cs/algo
---
### Big-O
> [!tip] Big-O
> The algorithm will never asymptotically[^1] be **worse** than this

This upper bound $O(f(n))$ grows **at most** as fast as $f(n)$. So for an equation like:
$$
T(n) = 3n^{2} + 7n + 10
$$
The term $n^{2}$ eventually dominates (kinds reminds me of calculus, tbh) bc there's some constant $C$ such that, for sufficiently large $n$:
$$
T(n) \leq C \cdot n^{2}
$$

---
### Big-Omega
> [!tip] Big-Omega
> The algorithm will never asymptotically be **better** than this

This lower bound $\Omega(f(n))$ grows **at least** as fast as $f(n)$. For example for the same function $T(n)$:
$$
T(n) = \Omega(n^{2})
$$
bc the following criteria is satisfied at one point or another:
$$
T(n) \geq C \cdot n^{2}
$$

---
### Big-Theta
This tight bound $\Theta(f(n))$ grows **exactly** like $f(n)$. For the same function $T(n)$:
$$
\begin{align}
 & T(n) = O(n^{2}) \\
 & T(n) = \Omega(n^{2})
\end{align}
$$
then:
$$
T(n) = \Theta(n^{2})
$$
This isn't a computationally derived concept. Instead if $O$ and $\Omega$ happen to be the same then the $\Theta$ arises

[^1]: A bit looser definition than the geometrical [[Asymptote]]. Differences described in the eponymous note
