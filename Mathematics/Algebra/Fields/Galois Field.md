---
tags:
  - math/abstract-algebra
  - math/field-theory
  - math/finite-field
updated: 2026-04-05
created: 2026-04-01
---
A Galois [[Field]] (abbr. GF), named after [[Evariste Galois]], is a *finite* field that is built using a mod of a prime number $p$ and, consequently, has the elements from $0$ to $p - 1$: $\{0, 1, 2,\dots, p - 1\}$.

### Multiplicative inverses
The primality is a very important part since it ensures the multiplicative inverses. This is based on the [[Euclidean Algorithm]] that provides that all numbers' GCD with $p$ being one: $GCD(a, p) = 1$

In practice this means (e.g. for $GF(5)$) that $3$ is the inverse of $2$ since $2 \cdot 3 \text{ mod } 5 = 1$. And it's exactly because it gives a $1$, it is the multiplicative inverse (look into the description of a field). So yeah, every number here has an inverse, that's basically it

### Connection to [[Polynomial Ring]]s
The coefficients in GF(p) are usually written as p-tuples. For GF(2), for example, those'd be: $0 = (0, 0)$,  $1 = (0, 1)$,   $x = (1, 0)$,  $x + 1 = (1, 1)$. That's why for $GF(2) \ / \ (x^{2} + 1)$ the addition and multiplication tables look like that:
<img src="Pasted image 20260404172728.png" width="550" style="display:block; margin:auto;">
The null-element is $(0, 0)$ and the one-element $(0, 1)$. Even here there exists an inverse element in every and each column. Further connection described in [[Irreducibility of Polynomials]]

### $GF(2)$
This is a special instance of GF since:
- Addition behaves like [[Exclusive Disjunction or XOR]] (since $1 + 1 = 0$ here, too) and multiplication like conjunction
- There's no distinction between addition and subtraction since $-1 \equiv 1$ (look to [[Modulus]] under "true modulus")

This also the simplest finite Galois Field which makes it ideal for programmatic purposes. In fact, [[AES]] uses $GF(2^{8})$ as its basis

### $GF(p^{n})$
> [!summary] Definition
> If $p$ is a prime number, $n$ is a natural number and $f(x)$ is a polynomial in $GF(p)[X]$ then the field $GF(p)[X] \ / \ f(x)$ can be abridged as $GF(p^{n})$

These groups have elements that are polynomials of $deg < n$ and all of its coefficients are in $GF(p)$. Interestingly enough, any finite field has the form $K = GF(p^{n})$. This also means that for such a field its [[Cardinality]] $|K| = p^{n}$