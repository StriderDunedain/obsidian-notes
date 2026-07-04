---
tags:
  - math/abstract-algebra
  - math/group-theory
updated: 2026-04-14
created: 2026-03-25
"created ": 2026-04-02
---
### Definition
A group is a structure that consists of a *set* and an *operation*: $(G, *)$: $* : G \times G \to G$ and has three properties:
1. There is such an element $e \in G$ with such a quality that $e * a = a * e = a \ | \ \forall a \in G$. This element is called the *neutral element*
2. $\forall a \in G$ there exists an element $a^{-1} \in G$ with such a quality that $a * a^{-1} = a^{-1} * a = e$. Such an element $a^{-1}$ is called *inverse* to $a$ (also expressed with $\hat{a}$)
3. $\forall a, b, c \in G$ holds: $a * (b * c) = (a * b) * c$. That means that operation $*$ on $G$ is *assoziativ*

A group is called *kommutativ* or *abelsch* (to honor their inventor, [[Niels Hendrik Abel]]) if to the main properties adds this one:
- $\forall a, b \in G$ holds: $a * b = b * a$. That means the operation $*$ on $G$ is *kommutativ*

#### Additivity & multiplicity
Moreover, groups bound by addition are called "additive" and those by multiplication "multiplicative":
1. Additive groups:
	- The neutral element is "0" (not that is has to be equal to 0, it's just a notation, an epitome of neutrality)
2. Multiplicative groups:
	- The neutral element is "1" (again, logic is the same)
	- $a \cdot b^{-1} = a/b$

Same goes for the inverse: $a^{-1} = -a$ here just for convenience

Further on names of laws in: [[Reduction Rules for Boolean Expressions]]

### Other properties
For elements $a, b \in G$ holds: the inverse of $(a * b) = b^{-1} * a^{-1}$ and that the inverse element of $a$ (i.e. $a^{-1}$) is clearly defined.

#### Proof
$$
\begin{align}
& (a * b) * (b^{-1} * a^{-1}) = e \\
& a * (b * b^{-1}) * a^{-1} = e \text{ (Assoziativät)} \\
& a * e * a^{-1} = e \text{ Inverse element} \\
& a * a^{-1} = e \text{ Neutral element} \\
& e = e \text{ Inverse element, again}
\end{align}
$$

**Note**: it is very important to notice that $(a * b) \neq a^{-1} * b^{-1}$ as attractive as it looks like

### Subgroups
If $(G, *)$ is a group and $U \subseteq G$ is a non-empty subset of $G$ then $(U, *)$ is a *subgroup* if the following conditions are met:
$$
\forall a, b \in U \text{ should hold: } a * b \in U \text{ and } a^{-1} \in U
$$

### Meaning & examples
Let's take $G := (\mathbb{Z}, +)$ to be a group, then:
1. The neutral element would be $0$ since:
$$
\forall a \in G : a + 0 = 0 + a = a
$$
2. The inverse element would be, naturally, $-a$ since:
$$
\forall a \in G: a + (-a) = -a + a = 0 \text{ (the neutral element)}
$$
3. Associativity of addition is obvious:
$$
\forall a, b, c \in G: = a + (b + c) = (a + b) + c
$$
As you can see we take the elements from the ring and the output maps it also unto the ring, not going beyond it