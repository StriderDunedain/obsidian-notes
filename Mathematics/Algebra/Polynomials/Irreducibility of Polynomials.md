---
tags:
  - math/algebra
  - math/polynomial
updated: 2026-04-25
created: 2026-04-04
---
Not really a very long note but I felt it deserved this since it bridges between [[Galois Field]]s and [[Polynomial Ring]]s and it's usually both structures used at the same time that make this concept useful

> [!faq] What makes a polynomial irreducible?
> A polynomial $f(x)$ of degree $g = n$ is *irreducible* when its representation by other polynomials $g(x) \text{ and } h(x)$ has their degrees either $g = 0$ or $g = n$

### Checking for irreducibility
There are not really a lot of methods you could go over to check for something like that. But here are the ones I've managed to find:
- First of all all degree one polynomials are irreducible
- For degrees two or three it's usually enough to check for the roots (the restriction also comes from the [[Abel-Ruffini Theorem]]). If there are roots then the polynomial is reducible
- For polynomials over $\mathbb{Q}$ you can use the [[Eisenstein's criterion]] (whatever this is, thx chatgpt)
- Try factoring the polynomial into lower degrees (like $x^{4} - 1 = (x^{2} - 1)(x^{2} + 1)$)


### Connection to [[Polynomial Ring]]s and [[Galois Field]]s
The core idea is to combine polynomials with a Galois-like field structure to make a field out of a polynomial ring. The idea is the same as with Galois fields – if it's based on a prime number it will have an inverse to every element of that field. Same idea extends to irreducible polynomials that behave exactly like prime numbers: that can be divided only by one and itself which ensures multiplicative inverses for every element. The notation is $K[X] \ / \ p(x)$

#### Examples
Let's take the field $GF(2)$ and $p(x) = x^{2} + x + 1$ to make: $GF(2)[X] \ / \ x^{2} + x + 1$. The only allowed irreducible elements here are: $\{0, 1, x, x + 1\}$. Here's an example of modulus on a polynomial in that field:
$$
\begin{align}
&\text{1. } \ (x + 1)^{2} \text{ mod } 2 = x^{2} + 2x + 1 \text{ mod } 2 = x^{2} + 1 \\
& \text{2. Now reduce by p(x): } x^{2} \equiv x + 1 \iff x^{2} + 1 = (x + 1) + 1 = x + 2 \text{ (take mod 2)} = x
\end{align}
$$
Why is $x^{2} \equiv x + 1$? It's all because:
$$
\begin{align}
& x^{2} + x + 1 = 0 \\
& x^{2} = -(x + 1) \\
& \text{And since } -1 \equiv 1 \iff x^{2} \equiv x + 1
\end{align}
$$
