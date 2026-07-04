---
tags:
  - math/abstract-algebra
  - math/structure
updated: 2026-05-10
created: 2026-04-23
---
> [!summary] Definition
> A monoid is a triple $(M, \odot, e)$ where: $M$ is a set, $\odot$ is such a binary operation that: $M \times M \to M$ and $e \in M$ is the distinguished element (also called the identity or the neutral element). It also has the following properties:
> $$
> \begin{align}
>  & \forall a, b, c \in M: (a \odot b) \odot   c = a \odot (b \odot c) \\
>  & \exists e \in M \text{ such that } \forall a \in M: a \odot  e = e \odot a = a
> \end{align}
> $$

#### Remarks
- Identity is unique
- There's no requirement for inverses – this is the property that makes it different from a [[Group]]

### Free monoid
$(\Sigma^{*}, \odot, \epsilon)$, for example is a free monoid because it has no relation between symbols other than concatenation

If there's no requirement for the identity then the structure is called a [[Semi-group]]