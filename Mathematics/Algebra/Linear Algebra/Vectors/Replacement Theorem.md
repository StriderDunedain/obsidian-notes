---
tags:
  - math/vector
updated: 2026-05-08
created: 2026-04-09
---
> [!summary] Definition
> If you have a linearly independent set of vectors in a [[Vector Space]] and a spanning set (a candidate for a basis), you can replace some vectors in the spanning set with vectors from the independent set without losing the spanning property

Let $S = \{ v_{1}, v_{2}, \dots, v_{m} \}$ be a linearly independent set and $T = \{ w_{1}, w_{2}, \dots, w_{n} \}$ be a spanning set. Both are in some vector space $V$. The theorem says that you can – carefully, as always – replace some vectors in $T$ with vectors from $S$ without losing the spanning property. Also, the number of vectors in $S$ can't exceed the number in $T$ ($m \leq n$). One more thing, in German it's called der Austauschsatz

> [!faq] Why is it important?

Good question. While it does seems to be pretty obvious, it rigorously allows:
1. To show that any base has the same number of elements as another base in the same space (that the dimensionality is well-defined)
2. To build a basis systematically. If there are some particularly good vectors you'd like to see in the spanning set this allows you to replace the useless ones with the useful ones
3. To prove that a linearly independent set in $K^{n}$ has $\{ \dots \}\leq n$ elements and that the spanning set has $\{ \dots \} \geq n$ elements

More in [[Basis and Dimension]] and [[Linear Dependency]]