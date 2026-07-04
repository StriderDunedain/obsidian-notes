---
tags:
  - math/number-theory
  - math/modular-arithmetic
updated: 2026-04-03
created: 2026-03-25
---
A recursive algorithm used to get the GCD of two numbers:

$$
\text{ggt}(a, b) =
\begin{cases}
|b| \ \text{ if a mod b = 0} \\
\text{ggt}(b, a \text{ mod } b)  
\end{cases}
$$
Example:
$$
\begin{align} \\
\text{gcd}(240, 46): \\
& 240 = \underline{46} \cdot 5 + \underline{10} \\
& 46 = \underline{10} \cdot 4 + \underline{6} \\
& 10 = \underline{6} \cdot 1 + \underline{4} \\
& 6 = \underline{4} \cdot 1 + \underline{2} \\
& 4 = \underline{2} \cdot 2 + 0
\end{align}
$$
And since we're at zero $\implies \text{gcd}(240, 46) = 2$

There also exists an [[Extended Euclidean Algorithm]] that find some very useful numbers too. A programmatic implementation is in [[Euclidean Algorithm (Code Version)]]
