---
tags:
  - math/abstract-algebra
  - math/structure
updated: 2026-05-02
"created ": 2026-05-02
---
> [!summary] Definition 
> A semi-group $(S, \otimes)$ is such a structure where $S$ is an non-empty set and $\otimes: S \times S \to S$

This is one of the simplest algebraic structures requiring only associativity:
$$
\forall a, b, c \in S \ | \ (a \cdot b) \cdot c = a \cdot (b \cdot c)
$$
An *abelian semi-group* also requires commutativity:
$$
a \cdot b = b \cdot a
$$

Examples would be $(\mathbb{N}, +)$ or concatenation of [[String]]s since both of those operations are associative and don't require identity or inverse elements