---
tags:
  - math/tba
  - math/morphism
updated: 2026-05-24
created: 2026-05-17
---
> [!tip] Definition
> Kernel (also called a nullspace) describes which inputs collapse to $0$ or the identity (in case of [[Group]]s). What concerns [[Linear Map]]s and vectors, it's all vectors from the domain that get mapped directly to $\vec{0}$. Strictly:
> $$
> \text{Ker}(\phi) := \{x \in G \ | \ \phi(x) = 0\} \\
> $$

It essentially measures the loss of information. For example:
1. For $\phi(n) = 2n$ the kernel $Ker(\phi) = \{0\}$ (which is when the map is *injective*) because only $0$ maps to $0$
2. Another example is for $\phi: \mathbb{Z} \to \mathbb{Z}/6\mathbb{Z}, \quad \phi(n) = n \text{ mod } 6$. The kernel here is $6\mathbb{Z}$ since all the elements of $\mathbb{Z} \text{ mod } 6$ fall to $0$

More on kernels in [[Matrix Rang]] and on mappings in [[Mapping]]s

The dimension of kernel is also called its *nullity*