---
tags:
  - math/vector
updated: 2026-05-24
created: 2026-04-09
"created ": 2026-05-10
---
### Basis
> [!summary] Definition
A basis of a vector space is such a set of vectors that is:
> 1. Linearly independent (more in [[Linear Dependency]])
> 2. Spans the whole space
>    
> A *standard basis* is a basis that looks like binary code in vectors

Which means that you can built every other vector from that vector space. The same principle as in [[Generator Element]]. Every [[Vector Space]] has one (except for $\{ \vec{0} \}$). Moreover every basis (whether a space has a finite amount of them or no) are of equal size (i.e. dimensionality) and can't have more than $n$ elements in it ($n$ here being the dimensionality)

#tba Is there an algorithm for finding all bases of a space?

#### Examples
In $\mathbb{R}^{3}$ the standard basis is, for example:
$$
(1, 0, 0), \quad  (0, 1, 0), \quad (0, 0, 1)
$$
Just some basis in $\mathbb{R}^{2}$ is (there are infinitely many in there):
$$
(2, 3) \quad (3, 4)
$$
Interestingly enough, for $\mathbb{R}^{2}$ it's enough to show that the vectors are linearly independent. From here their spanning of the whole space is somehow automatic

An example of a space with infinite number of bases is the [[Polynomial Ring]] in $\mathbb{R}[X]: \{ 1, x, x^{2}, x^{3},\dots \}$ (this is due to being always able to squeeze one more polynomial into this ring)

#### Testing for basis-ness
A way to check it is by putting vectors in a [[Matrix]] and computing the [[Determinant]]. Here's an example for $(2, 3), \ (3, 4)$:
$$
\begin{pmatrix}
2 & 3 \\
3 & 4 
\end{pmatrix}
$$
The determinant is: $2 \cdot 4 - 3 \cdot 3 = -1 \neq 0$. Since the determinant is not zero that means it's a basis


### Coordinates in relation to bases
> [!summary] Definition
> For any basis $B = \{ v_{1}, v_{2}, \dots, v_{n} \}$ any vector $v \in V$ can be uniquely written as:
> $$
v = \{ c_{1}v_{1} + c_{2}v_{2} + \dots + c_{n}v_{n} \} = 
\begin{pmatrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{pmatrix}_{B}
>$$

This means that any vector can be written using a base as a reference. Of course, for different bases different outcomes are to be expected. This serves as a standard reference of sorts to make stable transitions from one point of reference to another. Like getting everything together under the same denominator

#### Example
Let there be bases $B = \{ b_{1}, b_{2} \}$ and $C = \{ c_{1}, c_{2} \}$. The vectors $c_{1} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}_{B}, \ c_{2} = \begin{pmatrix} 1 \\ 2 \end{pmatrix}_{B}$ are linearly independent. Given $v = \begin{pmatrix} x \\ y\end{pmatrix}_{B}$ and we'd like to get the coordinates in $C$'s point of reference: $v = \begin{pmatrix} \lambda \\ \mu \end{pmatrix}_{C}$. The process goes like this: $v = \lambda c_{1} + \mu c_{2}$. But since $c_{1}$ and $c_{2}$ are in $B$'s point of reference we need to make some transformations:
$$
\begin{pmatrix}
x \\ y
\end{pmatrix}_{B}

= v = \lambda c_{1} + \mu c_{2} = \lambda

\begin{pmatrix}
2 \\ 2
\end{pmatrix}_{B}

+ \mu

\begin{pmatrix}
1 \\ 2
\end{pmatrix}_{B}
$$
From this we get the following system of equations:
$$
\begin{cases}
x = 2\lambda + \mu, \\
y = 2\lambda + 2\mu
\end{cases}
\iff
\begin{cases}
\lambda = x - \frac{1}{2}y, \\
\mu = -x + y
\end{cases}
$$
This gives us a way to transform from $B$ to $C$ and vice versa:
$$
\begin{pmatrix}
2 \\ 1
\end{pmatrix}_{B}
=
\begin{pmatrix}
\frac{3}{2} \\ -1
\end{pmatrix}_{C}
, \quad 
\begin{pmatrix}
2 \\ 2
\end{pmatrix}_{B}
=
\begin{pmatrix}
1 \\ 0
\end{pmatrix}_{C}
, \ \dots
$$

More on that in [[Linear Map]]


### Dimension
It's the number of vectors in the basis:
$$
\begin{align}
& \mathbb{R}^{2} \to  2 \text{ dimensions} \\
& \mathbb{R}^{3} \to  3 \text{ dimensions}
\end{align}
$$
Essentially, the dimension is the exponent over the [[Field]] of scalars over vector space (i.e. $\text{dim}(K^{n}) = n$). The Nullraum of $\{ \vec{0} \}$ has the dimensionality of zero

As a product of the [[Replacement Theorem]] every linearly independent set of vectors with $n$ elements in an $n$-dimension space is automatically a basis