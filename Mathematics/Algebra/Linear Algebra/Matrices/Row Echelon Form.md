---
tags:
  - math/matrix
  - math/linear-algebra
updated: 2026-04-21
created: 2026-04-20
---
REF is an [[Augmented Matrix]] that abides by the rules:
1. All zeros are at the bottom and form a staircase-like structure
2. Each pivot is to the right of the one above it
3. All entries below each pivot are zero
For example:
$$
\begin{bmatrix}
1 & 1 & 9 & \mid & x \\
0 & 5 & 2 & \mid & y \\
0 & 0 & 3 & \mid & z
\end{bmatrix}	
$$

Used in [[Gaussian Elimination]]

### Reduced Row Echelon Form (RREF)
This is a special case of REF where each pivot is one and everything else is zero. For example:
$$
\begin{bmatrix}
1 & 0 & 0 & \mid & x \\
0 & 1 & 0 & \mid & y \\
0 & 0 & 1 & \mid & z
\end{bmatrix}	
$$
Used in [[Gauss-Jordan Elimination]] and finding the inverse of a [[Matrix]]

***
It's called Zeilen-Stufen-Form in German