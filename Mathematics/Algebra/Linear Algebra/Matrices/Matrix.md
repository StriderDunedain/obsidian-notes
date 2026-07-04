---
tags:
  - math/matrix
  - math/linear-algebra
updated: 2026-06-03
created: 2026-04-09
"created ": 2026-04-17
---
> [!warning] Disclaimer
> Everything on matrices as of April 2026 and the foreseeable future will be from vector's POV since that's the direction the math book takes me in

> [!faq] Update coming?
> I *might* sit down and watch MIT open course ware on matrices and abstract algebra in general so these notes will be revised

#tba Watch MIT OpenCourseWare on Linear Algebra
#tba Fill out everything learned in 3b1b videos on essential algebra

### Connection to vectors
Apparently, matrices and bases, more in [[Basis and Dimension]], describe the same thing and the columns in matrices are the bases! Wtf... TT

### Square matrices
#### 2x2 Matrix
A square matrix (called "zwei Kreuz zwei" in German) is a matrix that looks like a square (if defined over real numbers, denoted as $\mathbb{R}^{2 \times 2}$):
$$
\begin{pmatrix} a \quad b \\ c \quad d \end{pmatrix}
$$
Terminology:
- Its elements are also sometimes called entries
- Top-left to bottom-right is the main diagonal
- Top-right to bottom-left is the secondary diagonal

Just the German terminology:
- $(a \quad c)$ and $(b \quad d)$ are the Spalten(-vektoren)
- $(a \quad b)$ and $(c \quad d)$ are the Zeilen(-vektoren)

#### Identity
Einheitsmatrix in German, this is the [[Group]]'s neutral element analogue:
$$
I = \begin{pmatrix}
1 \quad 0  \quad \dots \quad  0 \\
0 \quad 1 \quad \dots \quad  0 \\
\dots \\
0 \quad  0 \quad  \dots \quad  1
\end{pmatrix}
$$
It consists of 1s on its main diagonal and that's it. Ofc, $IA = AI = A$ follows. It can only be a square matrix. $I$'s determinant is $1$. Also the identity exists only for matrices the same dimensionality so the [[Linear Map]] has to be $id: K^{n} \to K^{n}$

#### Invertibility
A matrix $A$ is invertible if there exists such a matrix $A^{-1}$ that by multiplication with $A$ gives $I$:
$$
AA^{-1} = A^{-1} A = I
$$
Geometrically that means that the dimensions of $A$ remain intact, you can go back in the operations and the space doesn't collapse (like a 2D matrix collapsing into a line would lose a lot of information –> not invertible)

### Some operation rules
$$
\begin{align}
& 1. \ A + B = B + A, \\
& 2. \ (A + B)C = AC + BC, \\
& 3. \ A(B + C) = AB + AC, \\
& 4. \ (AB)C = A(BC), \\
& 5. \ AB \neq BA \text{ In general}
\end{align}
$$

### Multiplication
Two matrices can be multiplied together if matrix $A$ has the size $m \times n$ and matrix $B$ has the size $n \times p$. Notation for that is $AB$ or $A \circ B$ and it will have the size $m \times p$. The process is a dot product of each row from $A$ and each column from $B$. Formally, the following formula exists:
$$
(AB)_{ij} = \sum_{k=1}^{n}A_{ik}B_{kj} 
$$
In human words:
- Take a row $i$ from $A$
- Take a column $j$ from $B$
- Multiply
- Add 'em up

#### Example
$$
A = \begin{pmatrix} 1 \quad 2 \\ 3 \quad 4 \end{pmatrix},
\quad
B = \begin{pmatrix} 5 \quad 6 \\ 7 \quad 8 \end{pmatrix}
$$
Compute $AB$:
1. Find the sum for row one, column one:
$$
(1 \cdot 5) + (2 \cdot 7) = 19
$$
2. Find the sum of row one, column two:
$$
(1 \cdot 6) + (2 \cdot 8) = 22
$$
3. Find the sum of row two, column one:
$$
(3 \cdot 5) + (4 \cdot 7) = 43
$$
4. Find the sum of row two, column two:
$$
(3 \cdot 6) + (4 \cdot 8) = 50
$$
The final result is the following matrix $AB$:
$$
AB = \begin{pmatrix} 19 \quad 22 \\ 43 \quad 50 \end{pmatrix}
$$

> [!warning] $AB \neq BA$
> Matrix multiplication is not commutative! But it is associative and distributive

A shorter version would be:
$$
\begin{pmatrix}
a_{1,1}x_{1} + a_{1,2}x_{2} \\
a_{2,1}x_{1} +  a_{2,2}x_{2}
\end{pmatrix}
=
\begin{pmatrix}
a_{1,1} \quad a_{1,2} \\
a_{2,1} \quad  a_{2,2}
\end{pmatrix}
\begin{pmatrix}
x_{1} \\ x_{2}
\end{pmatrix}
$$
Where $a_{i}$-replete structure is a matrix and the $x$-replete one is a vector. An even shorter notation would be: $Ax$, where $A$ is the matrix and $x$ the vector

More on matrix transformations in [[Matrix Transformations]]

### Inverse Matrices
> [!warning] This applies only to square matrices

> [!tip]
> A matrix $A \in K^{n \times n}$ is invertible iff $\text{rang of } A = n$ (more in [[Matrix Rang]]) 

Somehow any matrix that maps unto itself is automatically a [[Linear Map]]. Whatever...

For any matrix $A \in K^{n \times n}$...
1. Exists a matrix $A^{-1} \in K^{n \times n}$ with the property: $A^{-1}A = AA^{-1} = I$ (where $I$ is the identity)
2. The map $A: K^{n} \to K^{n}$ is bijective
3. The columns of matrix $A$ are the basis of $K^{n}$
4. The columns of matrix $A$ are linearly independent (the above already implies that but whatever)

The sets of invertible in $K^{n \times n}$ matrices form a [[Group]] on multiplication

#### Finding the inverse matrix
That's hard. But for a 2x2 $A = \begin{pmatrix} a \quad b \\ c \quad d \end{pmatrix}$ and its inverse $\begin{pmatrix} e \quad f \\ g \quad h \end{pmatrix}$ that could go like this:
$$
\begin{pmatrix} a \quad b \\ c \quad d \end{pmatrix}\begin{pmatrix} e \quad f \\ g \quad h \end{pmatrix} = \begin{pmatrix} ae + bg \quad af + bh \\ ce + dg \quad cf + dh \end{pmatrix} = \begin{pmatrix} 1 \quad 0 \\ 1 \quad 0 \end{pmatrix}
$$
That could be further simplified to:
$$
\begin{pmatrix} e \quad f \\ g \quad h \end{pmatrix} = \frac{1}{ad - bc}\begin{pmatrix} d \quad -b \\ -c \quad a \end{pmatrix}
$$
That would, of course, work only when $ad - bc \neq 0$. Conversely, if that doesn't hold, there isn't an inverse