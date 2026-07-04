---
tags:
  - math/vector
updated: 2026-04-09
created: 2026-04-08
---
> [!summary] Definition
> Let $U$ and $V$ be [[Vector Space]]s over $K$. A map $f: U \to V$ is called a linear map if for all $u, v \in U$ and for all $\lambda \in K$ holds:
> $$
> \begin{align}
> & 1. \ f(u + v) = f(u) + f(v) \\
> & 2. \ f(\lambda u) = \lambda f(u)
> \end{align}
> $$
> For a bijective (i.e. isomorphic) mapping the notation $U \cong V$ is used

There exist no maps between different scalar fields (i.e. between $\mathbb{R}$ and $\mathbb{C}$) bc of the second criteria – $\lambda$ must be the same
### Other properties
- If $f: U \to V$ is an isomorphism then the reverse mapping $g := f^{-1}$ is linear and also isomorphic
- If $f: U \to V$ and $g: V \to W$ linear mappings then $g \circ f: U \to W$ is also linear
- If $f: U \to V$ a linear map then the $\text{Ker}(f)$ as well as $\text{Im}(f)$ are subspaces of either $U$ or $V$

- If $f: U \to V$ is a linear map, $U_{1}$ is a subspace of $U$ and $V_{1}$ a subspace of $V$ then:
$$
\begin{align}
& 1. \ f(U_{1}) = \{ f(u) \ | \ u \in U_{1} \} \text{ is a subspace of } V \\
& 2. \ f^{-1}(V_{1}) = \{ u \in U \ | \ f(u) \in V_{1} \} \text{ is a subspace of } U
\end{align}
$$


### Examples
Here's an example of an isomorphism between $\mathbb{R}^{2}$ and $\mathbb{R}^{3}$:
$$
f: \mathbb{R}^{2} \to  U,
\begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix}
\to 
\begin{pmatrix}
x_{1} \\
x_{2} \\
0
\end{pmatrix}
, \quad 
U := \{ 
\begin{pmatrix}
x_{1} \\
x_{2} \\
0
\end{pmatrix}
| x_{1}, x_{2} \in \mathbb{R}\} \subset \mathbb{R}^{3}
$$
A counterexample would be (because $f(0) \neq 0$):
$$
f: \mathbb{R} \to  \mathbb{R}, x \mapsto x + 1
$$

More in [[Mapping]], [[Homomorphism]] and [[Basis and Dimension]]

> [!summary] Linear maps + bases
> Let $U$ and $V$ be vector spaces over $K$, $\{ b_{1}, b_{2}, \dots, b_{n} \}$ be a basis of $U$ and $\{ v_{1}, v_{2}, \dots, v_{n} \}$ be the elements of $V$. Then there exists only one linear map $f: U \to V$ with the property $f(b_{i}) = v_{i}$ for all $i = 1, \dots , n$

This means that any vector can be uniquely written as a linear combination of the basis vectors with some scalars here and there. Out of this stems another important concept:

> [!tip] Very important
> Finite vector spaces $U$ and $V$ over $K$ are isomorphic iff they have the same dimensionality:
> $$
> U \cong V \iff \text{ dim}(U) = \text{ dim}(V)
> $$

Something else important is:

> [!summary] Morphisms + Vector Spaces
> Let $U, V$ be vector spaces, $\text{dim}(U) = n$ and $f: U \to V$ a linear map. Then the following holds:
> $$
> \text{dim}(\text{Ker}(f)) + \text{dim}(\text{Im}(f)) = \text{dim}(U)
> $$