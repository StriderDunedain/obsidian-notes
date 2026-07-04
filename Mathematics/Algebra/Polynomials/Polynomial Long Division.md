---
tags:
  - math/algorithm
  - math/polynomial
updated: 2026-06-15
created: 2026-04-04
"created ": 2026-04-07
---
This is how you'd divide one polynomial over another. Closely tied to [[Polynomial Ring]]s and [[Horner Scheme]] which is a hell lotta easier

### Example
The main principle is that you have to find how many $x$s and numbers are missing from the $x$ you currently dividing. So in the example below it'd be $2x^{2}$ since we start at $2x^3$ and divide it by $x$

Let's divide $2x^{3} - 3x^{2} +5x - 14$ by $x - 2$:
$$
\begin{align}
& (2x^{3} - 3x^{2} +5x - 14) \div (x - 2) \\
 \\
& \text{1. } \quad 2x^{3} - 3x^{2} +5x - 14 - (2x^{3} - 4x^{2}) \quad \text{| } \underline{2x^{2}} \cdot (x - 2) \\
& \text{2. } \quad x^{2} + 5x - 14 - (x^{2} - 2x) \quad \text{| } \underline{x} \cdot (x - 2) \\
& \text{3. } \quad 7x - 14 - (7x - 14) = 0  \quad \text{| } \underline{7} \cdot (x - 2)
\end{align}
$$
From all the underlined multiples we can construct the factorized version of the polynomial:
$$
2x^{3} - 3x^{2} +5x - 14 = (2x^{2} + x + 7)(x - 2)
$$