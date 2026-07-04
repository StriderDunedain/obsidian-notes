---
tags:
  - math/set
updated: 2026-03-17
created: 2025-11-13
---
A function, a map and an Abbildung are the same thing: take one element and turn it into another one. Do that with a lot and you get a set. Is closely related to [[Set Relations]]

### Notation and other stuff
For historical reasons:
$$\text{"}\to \text{"} \ \text{ is used for sets: } f: M \to N$$
$$\text{"} \mapsto \text{"} \ \text{ is used for elements: } x \mapsto f(x)$$
$$
\begin{align*}
&\text{Given } \hspace{3.8cm} f : M \to N \\
&D(f) := M \hspace{2.7cm} \text{ is the Definitionsmenge of } f \\
&N \hspace{4.6cm} \text{ is the Zielmenge of }  f \\
&f(M) := \{f(x) \mid x \in M\} \text{ is the Bildmenge or the Wertmenge of } f \\
\end{align*}
$$
$M$ is called he domain, $N$ is the codomain

Given
$$y = f(x)$$
- y is the *Bild* or image von x
- x is *Urbild* or preimage von y

One more fun thing:

$$\text{Identische Bildung: } f: M \to M, x \mapsto x =: id_{M}$$


### Example
![[Pasted image 20260311152000.png|583]]

- Wertemenge $W = \{1, 3\}$
- *1* is a Bild of *a* and *b*
- *2* has no Bild
- *a* and *b* are the Urbild of *1*
- $U = \{a, b\} \to f(U) = \{1\}$
- $V = \{2\} \to f^{-1}(V) = \emptyset$ *and* $V = \{2, 3\} \to f^{-1}(V) = \{c, d\}$


### Concepts and relations
An important notation of consecutive execution of functions (**read and executed from right-to-left**):
$$(g \circ f)(x) := g(f(x))$$

The relations between functions' created sets can be (Given f: M -> N):
$$
\begin{align*}
&\text{Injective: } \hspace{0.5cm} \forall x_{1}, x_{2} \in M: x_{1} \neq x_{2} \ \implies \ f(x_{1}) \neq f(x_{2}) \\
&\text{Surjective: }  \hspace{0.2cm}  \forall y \in N, x \in M : f(x) = y \\
&\text{Bijective: } \hspace{0.5cm}  \text{when a relation is both Injective and Surjective}
\end{align*}
$$
1. **Injective:** no two inputs map to the same output, guarantees *uniqueness*, a OneToOne relation (prevents duplicates)
2. **Surjective:** for every y in the *codomain* (output) there is at least one x in the *preimage* (input), guarantees that *no element in the codomain is left out*, a ManyToOne relation
3. **Bijective:** only this type of function has an inverse (denoted as f^(-1)). Essentially takes the "no duplicates" from injectivity and "use all from codomain" from surjectivity which guarantees a perfect one-to-one mapping

To check for bijectivity, one can prove this (that is if *f* and *g* work on $N$ and $M$ in reverse and both are needed):
$$g \circ f = id_{N} \leftrightarrow  f \circ g = id_{M}$$

### Real-life examples
Hash functions like *h(n) = n mod p* are surjective (i.e. FK) but not injective (don't guarantee uniqueness, e.g. *h(0) = h(p)*) which is exactly where hash collisions come from

The ASCII code is both injective and surjective (so bijective) bc each element maps to exactly one element. Injectivity is core to the en- and decoding. Without it, that which was once encoded, will be lost forever

### Consequent execution and $g \circ f$
#tba why does the following happen?

| **Property of $g \circ f$** |            **Consequence**             |
| :-------------------------: | :------------------------------------: |
|          injective          |            $f$ is injective            |
|         surjective          |           $g$ is surjective            |
|          bijective          | $f$ is injective and $g$ is surjective |
