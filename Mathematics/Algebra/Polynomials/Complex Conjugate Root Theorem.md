---
tags:
  - math/theorem
  - math/polynomial
  - math/abstract-algebra
updated: 2026-04-05
created: 2026-04-05
---
> [!summary] Definition
> Let $f(x) \in R[X]$ and $z = a + bi \in \mathbb{C}$ be a root of the polynomial in $\mathbb{C}$. Then the complex conjugate $a - bi$ is also a root of $f(x)$

Usually denoted as $\overline{z}$. To prove it the following has to hold: $\phi: \mathbb{C} \to \mathbb{C}, z \mapsto \overline{z}$ is an isomorphism (more in [[Homomorphism]]s). Then:
$$
\begin{align}
& \phi(f(z)) = \phi(a_{n}z^{n} + \dots + a_{0})  \quad (\phi\text{ is homomorphic}) = \\
& \phi(a_{n})\phi(z)^{n} + \dots + \phi(a_{0}) \quad (a_{i} \in R) = \\
& a_{n}\phi(z)^{n} + \dots + a_{0} = f(\phi(z))
\end{align}
$$
And because $f(z) = 0$ then $\phi(f(z)) = 0$ so $f(\phi(z)) = f(a - bi) = 0$

This was a revolutionary idea for its time and showed that there exists a close correlation between roots (i.e. zeros of a function, a.k.a. Nullstellen) and morphisms