---
tags:
  - math/matrix
  - math/linear-algebra
  - math/matrix-type
updated: 2026-05-24
created: 2026-05-15
---
This is a special kind of a [[Transposed Matrix]] where the transposed matrix is the [[Cofactor Matrix]]. Denoted as $\text{adj}(A)$:
$$
A = 
\left[ \begin{matrix}
a & b \\
c & d \end{matrix} \right],
\quad 
\text{adj}(A) = \left[ \begin{matrix}
d & -b \\
-c & a
\end{matrix} \right]
$$

It also appears in the inverse formula:
$$
A^{-1} = \frac{1}{\det(A)}\text{adj}(A)
$$
Geometrically, this means