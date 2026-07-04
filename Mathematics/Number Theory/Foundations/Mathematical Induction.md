---
tags:
  - math/number-theory
updated: 2026-03-24
created: 2026-03-11
---
This note is all about how to correctly prove induction:
$$
\text{To prove } A(n): \forall n \in \mathbb{N}, \text{ show that:}
\begin{cases}
\text{(Base case) } & A(1) \text{ is true}, \\
\text{(Inductive step) } & \forall k \in \mathbb{N}, \; A(k) \implies A(k+1).
\end{cases}
$$

A very important thing when proving using induction is to write: Assume some $n \in \mathbb{N}$ satisfies the assumption and not $\forall n \in \mathbb{N}$ the assumption is true (since that would be circular logic)