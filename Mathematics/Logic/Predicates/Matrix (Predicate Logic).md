---
tags:
  - math/logic
updated: 2026-05-07
created: 2026-05-04
---
> [!summary] Definition
> The matrix of a function is the part of the formula after all the [[Quantifiers]] that contains no quantifiers:
> $$
> Q_{1},x_{1} \ Q_{2}x_{2} \ \dots \ Q_{n}x_{n} \cdot \phi
> $$
> $\phi$ is the matrix. In [[Prenex Normal Form]]'s definition the $G$ is the matrix

Basically speaking it's the expression after the quantifiers:
$$
\underbrace{\forall x \exists y}_{\text{Quantifiers}}\underbrace{ (P(x, y) \lor \neg Q(y))}_{Matrix}
$$
### Clausal form
Matrixklauselform is the next step, essentially turning the matrix into [[CNF and DNF]]-style expressions, also written in my uni as a set of objects (like for [[Resolution]])