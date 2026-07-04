---
tags:
  - math/abstract-algebra
  - math/polynomial
  - math/algorithm
updated: 2026-04-04
created: 2026-04-02
---
Closely tied to [[Congruence Class]]es and [[Polynomial Ring]]s this is a way to divide one polynomial with another

### Example
An easier way is to do it using a table (the missing powers of $x$ are filled with $0$s). For the same example, the algorithm is:
1. Write out the coefficients of $x$s in the upper row
2. Put the non-$x$ part of the polynomial you divide with in the bottom left cell with the inverse sign (i.e. we have $+ 1$ -> $-1$)
3. Put a $1$ into the cell to the right
4. (this step covers how to fill all cells) Multiply that $-1$ by, first, $1$ (and then the last cell you filled) and add it to the number diagonally above you and write the result in the cell below (see below)
<img src="Pasted image 20260404114055.png" width="500" style="display:block; margin:auto;">
So you take $-1$, multiply by $1$, add to $1$ and write the result below ($0$). Then:
$$
\begin{align}
& -1 \cdot 0 + 0 = 0 \\
& -1 \cdot 0 + 1 = 1 \\
& -1 \cdot 1 - 7 = -8 \\
& -1 \cdot -8 - 8 = 0
\end{align}
$$Since the result is a $0$ it means that the polynomial has been divided without remainder and the polynomial that divided it was its root. The resulting coefficients in the lower table cells are the new coefficients so it can be written out as:
$$
x^{5} + x^{4} + x^{2} -7x - 8 = (x^{4} + x - 8) \cdot (x + 1)
$$