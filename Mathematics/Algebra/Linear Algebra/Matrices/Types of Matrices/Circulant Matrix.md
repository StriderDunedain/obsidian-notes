---
tags:
  - math/matrix
  - math/matrix-type
  - math/linear-algebra
---
A circulant matrix is a square [[Matrix]] whose rows are successive cyclic shifts of its first row. Formally:
$$
c = (c_{0}, c_{1}, \dots, c_{n-1}) \in \mathbb{F}^{n} 
$$
Where $\mathbb{F}$ is a [[Field]] (typically $\mathbb{R}$ or $\mathbb{C}$). The associated $n \times n$ circulant matrix is:
$$
C = \text{circ}(c_{0}, c_{1}, \dots, c_{n-1})
$$
An example:
$$
C =
\begin{pmatrix}
1 & 2 & 3 & 4 \\
4 & 1 & 2 & 3 \\
3 & 4 & 1 & 2 \\
2 & 3 & 4 & 1
\end{pmatrix}
$$
### 