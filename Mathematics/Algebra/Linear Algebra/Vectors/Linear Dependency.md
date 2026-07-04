---
tags:
  - math/vector
updated: 2026-04-09
created: 2026-04-08
---
### Linear Independence
Vectors $v_{1}, v_{2}, \dots, v_{n}$ are linearly independent if:
$$
\lambda_{1}v_{1} + \lambda_{2}v_{2} + \dots + \lambda_{n}v_{n} = \vec{0}
$$
Which implies:
$$
\lambda_{1} = \lambda_{2} = \dots = \lambda_{n} = 0
$$
The meaning here is that the only way to combine vectors to get the zero vector is by having all coefficients set to zero (this does remind me of [[CNF and DNF]] which use the exact same strategy). Geometrically this means that vectors point in different directions. These expand the span

#### Example
$$
(1, 0, 0), \quad (0, 1, 0)
$$
These spans build a plane and aren't multiples of each other ergo they are independent

### Linear Dependence
The opposite: you can get zero with non-zero coefficients. That means that at least one vector is redundant and can be built from others (i.e. multiplies of one another). Geometrically this means that at least one lies on the same line or inside the same plane. These don't bring anything to the span. The rigorous definition is:

>[!summary] Definition
>Let $V$ be a [[Vector Space]] over $K$ and $u, v_{1}, \dots v_{n} \in V$. The vector $u$ is called linearly dependent of $v_{1}, \dots, v_{n}$ when there exist such scalars $\lambda_{1}, \dots, \lambda_{n} \in K$ that:
>$$
>u = \sum_{i=1}^{n} \lambda_{i}v_{i} 
>$$
>If it's not the case then it's linearly independent

#### Example
$$
(1, 2, 3), \quad (2, 4, 6)
$$
The second vector can be built from the first one: $2 \cdot (1, 2, 3)$ so:
$$
2 \cdot (1, 2, 3) - (2, 4, 6) = 0
$$
Ergo they are dependent

### Testing for independence
The question we have to answer here is: "Can these vectors cancel each other out?". If the answer is yes, they are dependent, otherwise independent. Think of it like forces. If they cancel each other out – they don't bring anything new to the equation (here they don't add a direction)

Here's a check of $(2, 3), \ (3, 4) \text{ in } \mathbb{R}^{2}$ (we're looking for a trivial solution):
$$
\begin{align}
& \text{1. } \ \lambda(2, 3) + \mu(3, 4) = (0, 0) \\

& \text{2. } \
\begin{cases}
2 \lambda + 3 \mu = 0 \ | \cdot 3\\
3 \lambda + 4 \mu = 0 \ | \cdot 2
\end{cases}
\\
& \text{3. } \
\begin{cases}
6 \lambda + 9\mu = 0 \\
6\lambda + 8\mu = 0
\end{cases}
\\
& \text{4. } \ (6\lambda + 9\mu) - (6\lambda + 8\mu) = \mu = 0 \implies \lambda = 0
\end{align}
$$
Since **both** $\mu$ and $\lambda$ are equal to zero that means it's a trivial solution and these vectors are independent. In other words that means that there's no way you can substitute either $\mu$ or $\lambda$ to make the other vector which is why strictly booth have to be zero

***
### Trivia
- If you have more than $n$ vectors in $\mathbb{R}^{n}$ it automatically means dependency (through redundancy)