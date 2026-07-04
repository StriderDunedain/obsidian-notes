---
tags:
  - math/matrix
  - math/algorithm
  - math/linear-algebra
updated: 2026-05-24
created: 2026-05-15
---
Also called the Laplace Expansion, this is yet another way of finding the [[Determinant]] of a [[Matrix]]. It uses a recursive idea that matrices have submatrices and those have determinants that are simpler to count which is why we reduce the problem to smaller and smaller matrices

Two important concepts are:
- The [[Minor]] $M_{ij}$
- The [[Cofactor]] $C_{ij}$: that's this expression = $(-1)^{i+j}M_{ij}$

The formula goes like this:
$$
\text{det}(A) = \sum_{j=1}^{n}(-1)^{i+j}a_{ij}\text{det}(A_{ij})  
$$
### Example
Consider this matrix:
$$
A = \begin{pmatrix}
2 & 1 & 3 \\
0 & -1 & 4 \\
5 & 2 & 1
\end{pmatrix}
$$
We'll expand along the first row. In practice it's better to choose the row/column with many zeros but any will do. Other rows won't be shown bc it's just do damn long
$$
\text{det}(A) = a_{11}C_{11} + a_{12}C_{12} + a_{13}C_{13}
$$That becomes:
$$
\text{det}(A) = 2C_{11} + 1C_{12} + 3C_{13}
$$
Then, computing each cofactor:
1. $C_{11}$ (remove row 1, column 1):
$$
\begin{pmatrix}
-1 & 4 \\
2 & 1
\end{pmatrix}
$$
The minor is $M_{11} = (-1)(1) - 4 \cdot 2 = -9$
The sign: $(-1)^{1+1} = +1$ so the cofactor $C_{11} = -9$
And finally: $a_{11}C_{11} = 2 \cdot (-9) = -18$

Skipping other rows, $\text{det}(A) = -18 + 20 + 15 = 17$

### Adjugate matrices
Cofactors are also used to compute inverses and such a matrix of cofactors forms an [[Adjugate Matrix]]:
$$
A^{-1} = \frac{1}{\text{det}(A)}\text{adj}(A)
$$