---
tags:
  - math/matrix
  - math/algorithm
  - math/linear-algebra
updated: 2026-05-15
created: 2026-05-15
---
This is a quick way of getting the [[Determinant]] of a 3 x 3 matrix (compare with [[Cofactor Expansion]]). It goes like this. Consider a 3 x 3 matrix:
$$
A =
\begin{pmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{pmatrix}
$$
Then the determinant is:
$$
\text{det}(A) = aei + bfg + cdh - ceg - bdi - afh
$$
The key idea behind it is that the determinant is built from all possible ways to choose exactly one entry from each row and column. For a 3 x 3 matrix that's: $3! = 6$. As to why some terms are positive and some negative, look to [[Permutation Parity]]

### Example
Write the first two columns to the right of the matrix:
$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix}
\to
\left.
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}
\
\right|
\
\begin{matrix}
1 & 2 \\
4 & 5 \\
7 & 8
\end{matrix}
$$
#### The positive diagonals
1. First diagonal: $1 \cdot 5 \cdot 9 = 45$
2. Second diagonal: $2 \cdot 6 \cdot 7 = 84$
3. Third diagonal: $3 \cdot 4 \cdot 8 = 96$
4. Adding them up: $45 + 84 + 96 = 225$

#### The negative diagonals
1. First diagonal: $3 \cdot 5 \cdot 7 = 105$
2. Second diagonal: $2 \cdot 4 \cdot 9 = 72$
3. Third diagonal: $1 \cdot 6 \cdot 8 = 48$
4. Adding them up: $105 + 72 + 48 = 225$

Finally, subtract the former from the latter: $\text{det}(A) = 225 - 225 = 0$