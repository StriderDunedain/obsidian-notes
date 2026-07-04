---
tags:
  - math/linear-algebra
  - math/matrix
  - math/matrix-type
updated: 2026-05-24
created: 2026-05-24
---
A transposition (also called a swap) is a [[Matrix]] "flip" across its diagonal (i.e. rows become columns and vice versa). Denoted as $A^{T}$:
$$
A =
\left[
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{matrix}
\right],
\quad

A^{T} =
\left[
\begin{matrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{matrix}
\right]
$$

### Transposed Matrix
(Seemed a bit overkill to separate the action from the object)

In terms of coordinates it look like this (notice the flipping of $i$ and $j$ there):
$$
(A^{T})_{ij} = A_{ji}
$$

Essentially, a transposed matrix transforms measurements / coordinates

An important identity is:
$$
(Ax) \cdot y = x \cdot (A^{T}y)
$$

An important property of transposed matrices and their [[Determinant]]s is:
$$
\det(A^{T}) = \det(A)
$$
This works bc transpositions don't change the "volume" produced by a matrix, it just gives another POV of it

#### Properties
- Double transpose gives the original back: $(A^{T})^{T} = A$
- $(AB)^{T} = B^{T}A^{T}$