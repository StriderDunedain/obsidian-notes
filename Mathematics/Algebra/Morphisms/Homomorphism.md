---
tags:
  - tba-asap
updated: 2026-05-24
created: 2026-04-05
---
> [!summary] Group Homomorphism
> Let $G$ and $H$ be [[Group]]s and $\phi: G \to H$ a mapping with the following property:
> $$
> \phi(a \cdot b) = \phi(a) \cdot \phi(b), \quad \forall a, b \in G
> $$
> Then $\phi$ is called a *group homomorphism* (or (Gruppen-)Homomorphismus in German)

> [!summary] Ring Homomorphism
> Let $R$ and $S$ be [[Ring]]s and $\phi: R \to S$ a mapping with the following property:
> $$
> \phi(a + b) = \phi(a) + \phi(b), \quad \phi(a \cdot b) = \phi(a) \cdot \phi(b), \quad \forall a,b \in R
> $$
> Then $\phi$ is called a *ring homomorphism* (or (Ring-)Homomorphismus in German)

A bijective homomorphism is called an *isomorphism* (Isomorphismus)

### Kernel & Image
These concepts describe the injectivity and surjectivity respectively and are defined as follows. Let $(G, +)$ and $(H, +)$ be either groups or rings and $\phi: G \to H$ a homomorphism. Then:
$$
\begin{align}
& \text{Ker } \phi := \{x \in G \ | \ \phi(x) = 0\} \\
& \text{Im } \phi := \{y \in H \ | \ \exists x \in G, \ \phi(x) = y\}
\end{align}
$$
Where $\text{Ker}$ is the [[Kernel]] (or Kern) and $\text{Im}$ is the [[Image]] (or Bild)

### Other properties
For a homomorphism the following properties apply:
$$
\begin{align}
& \phi(0) = 0 \quad \text{ Always in kernel} \\
& \phi(-a) = -\phi(a) \\
& \phi(a - b) = \phi(a) - \phi(b), \quad \forall a,b \in G
\end{align}
$$

More on mappings and bijectivity in [[Mapping]]