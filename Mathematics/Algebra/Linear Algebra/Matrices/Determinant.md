---
tags:
  - math/matrix
  - math/linear-algebra
updated: 2026-05-24
created: 2026-05-09
---
> [!summary] Definition
> Essentially, if the [[Matrix]] encodes the transformation, the determinant tells you by how much the volume scaled, whether the orientation flips (i.e. the [[Chirality]])

If the determinant is zero, it means that some vectors were linearly dependent[^2] and some information gets irreversibly lost in the transformation. Another way of looking at it is that the dimensionality got cut: 3D became 2D and whatnot (like a plane collapsing to a line)

> [!faq] Why do determinants exist only for $n \times n$ matrices?
> Because only transformation that get $n$ inputs and produce $n$ outputs have any meaning. Else it would all just go from 3D to 10D and what would that even mean


> [!summary] Definition
> A determinant is a function $\text{det}: K^{2 \times 2} \to K$ with following properties:
> $$
> \begin{align}
> & \text{1. det} E = 1 \\
> & \text{2. If the rows are linearly dependent*, the determinant is $0$**} \\
> & \text{3. } \forall \lambda \in K, \ \forall \nu \in K^{n} \text{ holds:} \\
> & \quad \quad \text{det}(z_{1}, \dots, \lambda z_{i}, \dots, z_{n}) = \lambda \text{det}(z_{1}, \dots, z_{i}, \dots, z_{n}), \\
> & \quad \quad  \text{det}(z_{1}, \dots, z_{i} + \nu, \dots, z_{n}) = \text{det}(z_{1}, \dots, z_{i}, \dots, z_{n}) + \text{det}(z_{1}, \dots, \nu, \dots, z_{n})
> \end{align}
> $$


> [!summary] Definition
> A more fundamental definition is that the determinant is a sum over [[Permutation]]s[^1]:
> $$
> \text{det}(A) = \sum_{\sigma \in S_{n}} \text{sgn}(\sigma) \prod_{i=1}^{n} a_{i,\sigma(i)} 
> $$

Every square [[Matrix]] has a determinant

Geometrically, a determinant of a matrix $K^{n}$ is the volume of an $n$-dimensional body

A concept only applicable to square matrices that tells a lot of things (like invertibility) and generally how the space changes

#### For a 2x2 matrix
$$
\text{det}
\begin{pmatrix}
a \quad b \\ c \quad d
\end{pmatrix}
= ad - bc
$$
Geometrically, this is the volume of a parallelogram
#### For a 3x3 matrix
$$
\text{det}
\begin{pmatrix}
a \quad  b \quad  c \\
d \quad  e \quad  f \\
g \quad  h \quad i
\end{pmatrix}
= a(ei - fh) - b(di - fg) + c(dh - eg)
$$
Geometrically, this is the volume of a parallelepiped

Trivia:
- If the determinant is $0$ – the matrix isn't invertible
- $\text{det}(AB) = \text{det}(A) \cdot \text{det}(B)$
- Some other ways to count the determinant of (at least) a 3x3 matrix are [[Cofactor Expansion]] and [[Rule of Sarrus]]

### Elementary transformations
1. Switching two rows reverses the sign of the determinant (geometrically this is reversing of orientation)[^1]
2. Adding a multiple of a row to another row doesn't change the determinant
3. $\text{det}(z_{1}, \dots,\lambda z_{i},\dots,z_{n}) = \lambda \cdot \text{det}(z_{1},\dots,z_{i},\dots,z_{n})$


### Way of obtaining
Let there be a system of two linear equations and solve for $x$ and $y$:
$$
\begin{cases}
ax + by = e, \\
cx + dy = f
\end{cases}

\ ; \quad
x = \frac{ed - bf}{ad - bc},
\quad 
y = \frac{af - ce}{ad - bc}.
$$
Now $ad - bc$ is the determinant. When it's not zero it's solvable

### Some other properties
Let $A \in K^{n \times n}$ then the following expressions are equivalent:
$$
\begin{align}
& \text{det} \ A \neq 0 \\
& \text{rang} \ A = n \\
& \text{ker} \ A = \{ \vec{0} \} \quad \text{d.h. dim(ker(A)) = 0} \\
& \text{The vectors are lineraly independent}
\end{align}
$$
Or, vice versa:
$$
\begin{align}
& \text{det} \ A = 0 \\
& \text{rang} \ A < n \\
& dim(ker(A)) > 0 \\
& \text{The vectors are lineraly dependent}
\end{align}
$$

[^1]: More in [[Permutation Parity]]

[^2]: More on this in [[Linear Dependency]]
