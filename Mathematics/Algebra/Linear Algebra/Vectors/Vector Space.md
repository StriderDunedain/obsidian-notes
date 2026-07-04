---
tags:
  - math/vector
updated: 2026-05-24
created: 2026-04-07
---
> [!summary] Definition
> Let $K$ be a [[Field]]. A vector space (or Vektorraum in German) with scalars from $K$ consists of an abelian [[Group]] $(V, +)$ and a scalar multiplication $\cdot: K \times V \to V, \quad (\lambda, \nu) \mapsto \lambda \cdot \nu$ so that for all $\nu, w \in V$ and for all $\lambda, \mu \in K$ holds:
> $$
> \begin{align}
> & 1. \lambda(\mu \nu) = (\lambda \mu)\nu \\
> & 2. 1 \cdot \nu = \nu \\
> & 3. \lambda(\nu + w) = \lambda \nu + \lambda w \\
> & 4. (\lambda + \mu)\nu = \lambda \nu + \mu \nu
> \end{align}
> $$
> And is called *K-vector space* or *vector space over $K$*

**Note**: for every field $K$ the set $K^{n}$ is a vector space

### Subspace
Also called Untervektorraum, Unterraum or Teilraum in German it is such a set $U \subset V$, where $V$ is a vector space when these properties are present:
$$
\begin{align}
& 1. \ u + v \in U, \quad  \forall u, v \in U \\
& 2. \ \lambda u \in U, \quad \forall \lambda \in K, u \in U
\end{align}
$$
A simple test would be to check the presence of $\vec{0}$ (since $U$ is a group). Also lines of the form $\{ \lambda \nu \ | \ \lambda \in K \}$ and are called Ursprungsgeraden (English seems to lack the definition) and also form subspaces. Moreover, spans also form subspaces.

The two properties are being closed under addition and scalar multiplication

### Span
A span is a linear combination of some vectors. For $V$, a vector space over $K$, let $n \in \mathbb{N}$, $u_{1},\dots, u_{n} \in V$ and $\lambda_{1}, \dots, \lambda_{n} \in K$. Their sum: $\lambda_{1}u_{1} + \dots + \lambda_{n}u_{n}$ is called the *linear combination* and the span is defined as:
$$
\text{Span}(u_{1}, \dots, u_{n}) := \left\{  \sum_{i=1}^{n}\lambda_{i}u_{i} \ \middle | \ \lambda_{i} \in K  \right\}
$$
If $M$ is an infinite subset of $V$ then:
$$
\text{Span M} := \left\{  \sum_{i=1}^{n}\lambda_{i}u_{i} \ \middle | \ n \in \mathbb{N}, \lambda_{i} \in K, u_{i} \in M \right\}
$$

More on vector spaces in [[Dual Space]]s

***
### Trivia
- Somehow related to some linear codes, whatever that is. Anyhow, those operate in $(\mathbb{Z}/2\mathbb{Z})^{n}$