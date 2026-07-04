---
tags:
  - math/abstract-algebra
  - math/field-theory
updated: 2026-04-05
created: 2026-03-28
---
### Definition 1 | Long Version
Also called a *Körper* in German, a field $(K,\oplus, \odot)$ is composed of a set $K$ and *at least* two elements and two operations $\oplus$ and $\odot$ over $K$ such that:
1. $(K, \oplus, \odot)$ is a *kommutativer* ring (more on that in [[Ring]]s)
2. $\exists 1 \in K$ such that $1 \odot a = a \odot 1 = a, \ \forall a \in K$
3. $\forall a \in K$, where $a \neq 0$, there is an element $a^{-1} \in K$ with the property of $a^{-1} \odot a = 1$. So that means $a^{-1}$ is *inverse* to $a$ in relation to $\odot$

The existence of at least two elements in $K$ is equivalent to $1 \neq 0$ (that's just genius, I'd honestly never imagine that)

### Definition 2 | Short version
Under same notation as above the properties should be:
1. $(K, \oplus)$ in a *kommutative* group with a *neutral element* $0$
2. $(K \setminus \{0\}, \odot)$ is a *kommutative* group with a *neutral element* of $1$
3. $a \odot (b \oplus c) = (a \odot b) \oplus (a \odot c), \ \forall a, b, c \in K$

A [[Congruence Class]] of $\mathbb{Z}/2\mathbb{Z}$ is a field. Interestingly enough, if $p$ is a prime then $\mathbb{Z}/p\mathbb{Z}$ is always a field ([[Galois Field]])

### Other properties
1. $\forall a \in K \ | \ a \cdot 0 = 0$
2. $a, b \in K \ | \ a, b \neq 0 \text{ means } a \cdot b \neq 0$
3. Division by 0 also doesn't make much sense here

### Equivalence classes (again)
Described in [[Set Relations]], an equivalence class in this sense is
$$
[a] = \{b \in \mathbb{Z} \ | \ a \sim_{n} b\}
$$
The notation for an equivalence relation is:
$$
a \sim_{n} b \iff a \equiv b \text{ mod } n
$$
I don't really get how the notation changes anything but dayum I'm tired. I off to hit the sack

### Meaning & examples
Let's take a field $K := (\mathbb{Q}, +, \times)$ then:
2. A neutral element would be a $1$:
$$
\forall a \in K: 1 \cdot a = a \cdot 1 = a
$$
3. The inverse element also exists (when $a \neq 0$):
$$
\forall a, b \in K: \frac{a}{b} \cdot \left( \frac{a}{b} \right)^{-1} = () 
$$
### Connection to [[Polynomial Ring]]s
If $K$ is a field and $p(x) \in K[X]$ is a polynomial then $K[X] \ / \ p(x)$ is also a field iff $p(x)$ is irreducible (more in [[Irreducibility of Polynomials]]). And $K$ becomes a subfield of $K[X] \ / \ p(x)$