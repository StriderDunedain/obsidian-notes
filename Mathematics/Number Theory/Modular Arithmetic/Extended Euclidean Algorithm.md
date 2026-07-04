---
tags:
  - math/number-theory
  - math/algorithm
  - math/modular-arithmetic
updated: 2026-04-06
created: 2026-04-03
---
Give me a This algorithm is one of the ways to find the [[Bézout's Identity]]. It's really easier to show an example rather than give an algorithm

### An example
Using as an example this gcd from the [[Euclidean Algorithm]]:
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
We'll find the identities like this:
$$
\begin{align}
\text{Starting backwards:} \\
& \text{1. }\ 2 = 6 - 4 \cdot 1 \quad \text{| The gcd "reversed"} \\
& \text{2. }\ 2 = 6 - 1 \cdot (10 - 6 \cdot 1) \quad \text{| The "4"-remainder is reversed from 3rd eq.} \\
& \text{Simplification: }\ 2 = 6 - 1\cdot 10+ 6 \cdot 1 =  2 \cdot 6 - 1 \cdot 10 \\
& \text{3. } \ 2 = 2 \cdot (46 - 10 \cdot 4) - 1 \cdot 10 \quad \text{| The "6"-remainder}\\
& \text{Simplification: } \ 2 = 2 \cdot 46 - 10 \cdot 8 - 1 \cdot 10 = 2 \cdot 46 - 9 \cdot 10 \\
& \text{4. } \ 2 = 2 \cdot 46 - 9 \cdot (240 - 46 \cdot 5) \quad \text{| The "10"-remainder} \\
& \text{Simplification: } \ 2 = 2 \cdot 46 - 9 \cdot 240 + 46 \cdot 45 = 46 \cdot 47 - 9 \cdot 240 \\ \\

& \text{From which we get: } 2 = 46\cdot \underline{47} - \underline{9} \cdot 240
\end{align}
$$
So we get the identity to be $(47, -9)$
This is a core part of the [[RSA]] and [[Diophantine Equations]]