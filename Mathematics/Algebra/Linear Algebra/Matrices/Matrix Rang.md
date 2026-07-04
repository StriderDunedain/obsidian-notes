---
tags:
  - math/matrix
  - math/linear-algebra
updated: 2026-05-04
created: 2026-04-17
---
> [!summary] Definition
> The rang of a matrix is the maximum number of linearly independent column-vectors in a [[Matrix]]

For a [[Linear Map]] $f: K^{n} \to K^{m}$ with a corresponding matrix $A \in K^{n \times m}$ and the column-vectors $(s_{1}, s_{2}, \dots, s_{n})$ holds:
1. $\text{Im}(f) = \text{Span}\{ s_{1}, s_{2}, \dots, s_{n} \}$
2. $\text{Ker}(f) = \{ x \ | \ Ax = 0 \}$ is the set of solutions for $Ax = 0$
3. $\text{dim}(\text{Im}(f))$ = $\text{rang of } A$
4. $\text{dim}(\text{Ker}(f))$ = $n - \text{rang of } A$

### Examples
> [!tip] Rows vs Columns
> Rows, as well as columns, can be used to find the rang of a matrix, it doesn't matter which is used. That is due to rows being easily convertible into columns

Matrix $\begin{pmatrix}1 \quad 0 \quad 1 \\ 0 \quad 1 \quad 1 \\ 2 \quad 0 \quad 2\end{pmatrix}$ has the rang of $2$ since $s_{1} + s_{2} = s_{3}$
Matrix $\begin{pmatrix}1 \quad 2 \quad 4 \\ 2 \quad 4 \quad 8  \\ 3 \quad 6 \quad 12\end{pmatrix}$ has the rang of $1$ since every other column is a multiple of the first one

#### Triangular matrices
This is a type of square matrices where there're are only zeroes either below or above the main diagonal:
$$
\text{Upper: }
\begin{pmatrix}
* \quad  * \quad  * \quad  \dots \quad  *\\
0 \quad  * \quad * \quad \dots \quad * \\
0 \quad  0 \quad * \quad \dots \quad * \\
\dots \\
0 \quad 0 \quad  0 \quad \dots \quad  *
\end{pmatrix},
\quad
\text{Lower: }
\begin{pmatrix}
* \quad  0 \quad  0 \quad  \dots \quad  0 \\
* \quad  * \quad 0 \quad \dots \quad 0 \\
* \quad  * \quad * \quad \dots \quad 0 \\
\dots \\
* \quad * \quad  * \quad \dots \quad  *
\end{pmatrix}
$$
Their rang corresponds to the number of columns

***
The rang of a [[Row Echelon Form]] matrix is the number of pivots