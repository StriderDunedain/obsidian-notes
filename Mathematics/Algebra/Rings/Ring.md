---
tags:
  - math/abstract-algebra
  - math/ring-theory
updated: 2026-05-10
created: 2026-03-26
"created ": 2026-04-05
---
### Definition
A ring $(R, \oplus, \odot)$ consists of a set $R$ and two operations, $\oplus$ and $\odot$, with the following properties:
1. $(R, \oplus)$ is a *kommutative* [[Group]]
2. $\forall a, b, c \in R \text{ should hold: } a \odot (b \odot c) = (a \odot b) \odot c$. So the operation $\odot$ is *associative*
3. $\forall a, b, c \in R \text{ should hold: } a \odot (b \oplus c) = (a \odot b) \oplus (a \odot c)$. And vice versa should also hold. So $\odot$ is *distributive* in relation to $\oplus$

Another way of building a ring is to show that $(G, +)$ is an abelian [[Group]] and $(G, \cdot)$ is a [[Semi-group]]

> [!attention] A word of caution
> In the first condition of what a ring is it is stated that it's a abelian group. However that goes only for addition and not multiplication. What that means is that ring have to have additive inverses but not multiplicative ones

A ring is called *kommutativ* is to the three mentioned above rules, another rule is added:
- $\forall a, b \in R \text{ should hold } a \odot b = b \odot a$

### Subrings
Let $S \subseteq R$, where $(R, +, \cdot)$ is a ring. Then $(S, +, \cdot)$ is also a ring when:
$$
\begin{align}
& 1. \ (S, +) \text{ is a subgroup of } (R, +) \text{ which means: } a, b \in S \implies a + b \in A, a^{-1} \in S \\
& 2. \ a,b \in S \implies a \cdot b \in S
\end{align}
$$

### Meaning & examples
First of all a group is a subset of a ring: $G \subset R$ (yes, even though a ring is a group with additional features). An example of a ring would be:
$$
R := (\mathbb{Z}, +, \times)
$$
The first condition of the ring being a commutative group is explained in the corresponding note about groups, so let's start from the second one:
$$
\forall a, b, c \in R \text{ should hold: } a \cdot(b \cdot c) = (a \cdot b) \cdot c
$$
Which is what you would expect of multiplication over $\mathbb{Z}$ (as to the proof... I've no idea, I just hope it's true, no time to delve deeper)

As for the third one:
$$
\forall a, b, c \in R \text{ should hold: } (b + c) \cdot a = (a \cdot b) + (a \cdot c)
$$
Which is also how this works for addition over $\mathbb{Z}$ (again, have no proof, just hope)

What's also interesting is that if a ring has a multiplicative inverse, it is a [[Field]]!

***
### Trivia
**Note on name | 1**: Hilbert sort of just came up with the name and it doesn't imply that there's a cycle somewhere, it's apparently just a name

**Note on name | 2**: if a ring qualifies all three criteria its sometimes called a unital ring or a ring with unity 


#tba What's an ideal of a ring?