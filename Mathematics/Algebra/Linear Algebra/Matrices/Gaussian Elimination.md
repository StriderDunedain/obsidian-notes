---
tags:
  - math/matrix
  - math/linear-algebra
  - math/algorithm
updated: 2026-04-21
created: 2026-04-20
---
Also called Gauß'sches Eliminationsverfahren this is an algorithm for finding solutions in an [[Augmented Matrix]]. The ultimate goal is to get the matrix to [[Row Echelon Form]]. A close concept is the [[LU Decomposition]]

> [!summary] Pivot (or Leitkoeffizient)
> The first non-zero entry in a row (from left to right)

### Basic operations
These three operations are idempotent:
1. Rows can be swapped
2. A row can be multiplied by a non-zero number
3. Adding/subtracting a multiple of one row to another

### The algorithm
The idea is to eliminate variables column by column. We go left -> right and top -> bottom. for example:
$$
	\begin{bmatrix}
	2 & 1 & -1  & \mid & 8 \\
	-3 & -1 & 2  & \mid & -11 \\
	-2 & 1 & 2  & \mid & -3
	\end{bmatrix}
	\quad \text{ The pivot here is "2"}
$$
1. We want all entries below a pivot to be equal to zero so we use $a + p\cdot b = 0$ and then $c \cdot R_{1} + R_{2} \to R_{2}$:
$$
	\begin{bmatrix}
	2 & 1 & -1 & \mid & 8	\\
	0 & 0.5 & 0.5 & \mid & 1 \\
	0 & 2 & 1 & \mid & 5
	\end{bmatrix}
$$
By that I mean that we need to find such an equation that $-3 + 2b = 0$. That's $\frac{3}{2}$ and then we need to count $\frac{3}{2} \cdot R_{1} + R_{2}$ and that will become the new value for the second row's entry (that's fucked up honestly). We repeat the same for the third row with $b = 1$
2. Then we go to the second row and the pivot $p = 0.5$. Repeat the same process as above and you will get:
$$
	\begin{bmatrix}
	2 & 1 & -1 & \mid & 8	\\
	0 & 0.5 & 0.5 & \mid & 1 \\
	0 & 0 & -1 & \mid & 1
	\end{bmatrix}
$$
3. Now comes the *back-substitution*, the solving phase:
$$
	\begin{align}
	 & \text{The last row: } -z = 1 \implies z = -1 \\
	 & \text{The penultimate row: } 0.5y + 0.5z = 1 \implies y = 3 \\
	 & \text{The first row: } 2x + y - z = 8 \implies x = 2
	\end{align}
$$
Which is the solution: $(x, y, z) = (2, 3, -1)$

### Corner cases
- An infinite solution arises if the pivots are not in a stairway-shaped figure (since that leads to free variables and the solution is not a point but a whole plane)
- No solutions exists for a contradiction such as $\begin{bmatrix}0 &  0 & 0 & \mid & 5\end{bmatrix}$

### Geometric meaning
Every equation is a plane and the algorithm finds their intersections
***
A programmatic version is in the [[Gaussian Elimination (Programmatic View)]]