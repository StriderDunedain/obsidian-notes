---
tags:
  - cs/foundation
updated: 2026-05-05
created: 2026-05-04
---
> [!summary] Definition
> For any sufficiently expressive first-order language (e.g. containing at least one binary predicate), the set $\text{VAL}_{\mathcal{L}}$ is **not decidable**

Also called the Undecidability of first-order logic validity is a theorem on the limits of algorithmic reasoning. What that means is that there's no algorithm ([[Turing Machine]]) $M$ such that for every $\phi$:
$$
M(\phi) = 
\begin{cases}
\text{YES} \quad  \text{if } \models \phi, \\
\text{NO} \quad  \text{if } \not\models \phi
\end{cases}
$$
The practical implication is the [[Entscheidungsproblem]]

### Definition
Let:
- $\mathcal{L}$ be a first-order language (predicate logic), more in [[Chomsky Hierarchy]]
- $\text{Sent}(\mathcal{L})$ be a set of all closed formulas in $\mathcal{L}$
- $\models \phi$ mean that $\phi$ is logically valid in every [[Structure]] (or [[Model (Math)]]) for $\mathcal{L}$
Define the set of formulas:
$$
\text{VAL}_{\mathcal{L}} = \{ \phi \in \text{Sent}(\mathcal{L} ) \models \phi\}
$$

***
Use cases include, but not limited to:
- [[Gödel's Incompleteness Theorem]]
- [[Gödel's Completeness Theorem]]
- [[Church–Turing Theorem]]