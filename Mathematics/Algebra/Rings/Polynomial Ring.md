---
tags:
  - math/abstract-algebra
  - math/polynomial
  - math/ring-theory
updated: 2026-04-15
created: 2026-03-29
"created ": 2026-04-05
---
A polynomial is just a многочлен. But to understand what a polynomial ring is, first one has to understand what a polynomial function is:

### Polynomial function
Let $(R, \oplus, \odot)$ be a commutative ring, more in [[Ring]]s, where $a_{0}, a_{1}, \dots, a_{m} \in R$ then the function $f$:
$$
f: R \to R, x \mapsto (a_{m} \odot x^m) \oplus (a_{m-1} \odot x^{m-1}) \oplus \dots \oplus (a_{1} \odot x) \oplus a_{0} 
$$
Would be called a *polynomial function* over $R$. A more readable version is:
$$
f(x) = a_{m}x^m + a_{m-1}x^{m-1} + \dots + a_{1}x + a_{0}
$$
#### Degree of a function
The *degree* of a polynomial function $f: deg(f)$ defines the biggest index $i$ for which $a_{i} \neq 0$. And in case all $a_{i}$'s are zero (i.e. $a_{0} = a_{1} = \dots = a_{m} = 0$), then the degree will be equal to $-\infty$.

For example in the function $f(x) = 3x^4 + 2x^2 + 4$ the $deg(f) = 4$ since $4$ is the biggest non-null exponent here

### Polynomial ring
Also called a *Polynomring* in German, its definition is as follows:
1. Let $(R, \oplus, \odot)$ be a commutative ring
2. The set of all polynomials over $R$ is written as $R[X]$
3. For polynomials / polynomial functions $p, q \in R[X]$ the operations $\boxdot$ and $\boxplus$ should be defined as follows:
$$
\begin{align}
& p \boxplus q: R \to R; \ \ x \mapsto p(x) \oplus q(x) \\
& p \boxdot q: R \to R; \ \ x \mapsto p(x) \odot q(x)
\end{align}
$$
Then $(R[X], \boxplus, \boxdot)$ will be called a *polynomial ring* over $R$

> [!faq] Polynomial = polynomial ring = polynomial function?
> - A **polynomial** is an expression of form: $a_{n}x^{n} + \dots + a_{1}x + a_{0}$
> - A **polynomial ring** is the set of all polynomials over a *coefficient set* (see below) which also defines addition and multiplication
> - A **polynomial function** is just assigning a function to a polynomial. However, same function can describe different polynomials under specific circumstances (see in "Equivalence relation" below)

**Note**: the *coefficient set* is just a set from where all the coefficients before $x$ can come (i.e. $\mathbb{R}$, $\mathbb{Z}$, etc.)

> [!summary] $K$ vs $K[X]$
> Before reading further you need to understand the difference between $K$ – a [[Field]] – and $K[X]$ – a polynomial ring. $K$ is a field and it defines addition and multiplication (and maybe the boundaries if it's finite like [[Galois Field]]s) since these are exactly the things needed for polynomials. And $K[X]$ is already a ring since it loses its multiplicative inverse but it retains the addition, multiplication and coefficients defined in $K$. Think of it like a child class that has some more methods available to it and preserves some core idea of its parents but can't guarantee something that the parent could (in this example its multiplicative identity)

***
### Operations
Let $R$ be a commutative ring and $p = a_{m}x^m + a_{m-1}x^{m-1} + \dots + a_{1}x + a_{0}$ with $q = b_{n}x^n + b_{n-1}x^{n-1} + \dots + b_{1}x + b_{0}$ be two polynomials from $R[X]$ with $deg(p) = m$ and $deg(q) = n$:
#### Sum
Then the sum $p + q$ will have the degree $k \leq max(m, n)$ and the representation:
$$
p + q = (a_{k} + b_{k})x^k + (a_{k-1} + b_{k-1})x^{k - 1} + \dots + (a_{1} + b_{1})x + (a_{0} + b_{0}) = \sum_{n=0}^{k}(a_{n} + b_{n})x^{n}
$$
#### Product
Then the product $p \cdot q$ will have the degree $l = m + n$ and the representation:
$$
p \cdot q = c_{l}x^l + c_{l-1}x^{l-1} + \dots + c_{1}x + c_{0} = \sum_{k=0}^{l+l}\left( \sum_{\substack{i+j = k \\ 0 \leq i, j \leq n}}a_{i}b_{j} \right)x^{k}
$$
where: $c_{j} = \sum_{i=0}^j a_{i} \cdot b_{j - i}$ and $0 \leq j \leq m + n$

**Note**: higher coefficients are filled with zeros:
$$
\begin{align}
& a_{m + n} = a_{m + n - 1} = \dots = a_{m + 1} = 0 \\
& b_{m + n} = b_{m + n - 1} = \dots = b_{n + 1} = 0
\end{align}
$$
***
### Equality and Equivalence relation
#### Equality
> [!abstract] Equality of polynomials and polynomial functions
> 1. Two **polynomials** are equal when their coefficients match:
> $$
> a_{n}x^{n} + \dots + a_{0} = b_{n}x^{n} + \dots + b_{0} \iff a_{i} = b_{i} \ \text{ for all } \ i
> $$
> 2. Two **polynomial functions** are equal when they produce the same value for every $x$:
> $$
> f(x) = g(x) \ \text{ for all } \ x
> $$

**Note 1**: the latter can happen in case of a finite set. For example, let $f(x) = x^{2}$ and $g(x) = x$. They are not equal polynomials or functions. However, under the set $\{0, 1\}$ they essentially become the same function since the result is always the same

**Note 2**: However, if the talk is of their equivalence under a mod then two polynomials are equal when they have the same remainder mod $p(x)$

#### Equivalence relation
Let $f(x), g(x) \in K[X]$ and let $[f(x)], [g(x)]$ be the [[Congruence Class]]es of $f(x), g(x) \text{ mod } p(x)$. Then the following arises:
$$
\begin{align}
& [f(x)]\oplus[g(x)] := [f(x) + g(x)] \\
& [f(x)]\odot[g(x)] := [f(x) \cdot g(x)]
\end{align}
$$
The definition above can also be represented this way:
$$
\begin{align}
& f(x) \oplus g(x) = (f(x) + g(x)) \text{ mod } p(x) \\
& f(x) \odot g(x) = (f(x) \cdot g(x)) \text{ mod } p(x)
\end{align}
$$
The resulting set of [[Congruence Class]]es is noted as $K[X] \ / \ p(x)$ and read as $K[X]$ mod $p(x)$. As usual, the resulting sets form polynomials one smaller than the degree of polynomial $p(x)$ (i.e. $\approx\{[1], [2], \dots, [deg(p(x)) - 1]\}$). The approximation is bc its not numbers but polynomials, see below in "Examples"

> [!faq] Is $K[X] \ / \ p(x)$ still a ring or a field already?
> This is a tricky one. Everything depend on whether $p(x)$ is irreducible over the given field $K$. If it is then this becomes a field. Otherwise no. Look below in "Returning to a field" for more info on that

More on equivalence relation in [[Set Relations]]

### Examples
For a polynomial $p(x) = x^{3} + 1$ in $\mathbb{Q}[X]$, the congruence classes would consist of polynomials of degree less than $3$: $\mathbb{Q} \ / \ p(x) = \{ax^{2} + bx + c \ | \ a,b,c \in \mathbb{Q}\}$. The addition of two polynomials will still be within the allowed degree, so there's not much going in there but when it comes to addition the number can become greater so we have to mod $p(x)$ it:
$$
\begin{align}
& (2x^{2} + 1) \odot (x + 2) = 2x^{3} + 4x^{2} + x + 2 \\
& 2x^{3} + 4x^{2} + x + 2  \text{ mod } (x^{3} + 1) = 2(x^{3} + 1) + (4x^{2} + x)
\end{align}
$$
The remainder is $4x^{2} + x$ so the congruence class is $[4x^{2} + x]$ and $(2x^{2} + 1) \odot (x + 2) = 4x^{2} + x$

***
### Returning to a field
> [!faq] Can $K[X]$ become a field once again?
> Sure it can! You just have to have an inverse for multiplication. This can be done in two ways described below. The first one "adds freedom" and the second one "adds restrictions"

#### Rational functions
$K[X]$ can become a field again if you introduce rational function (with one caveat below):
$$
K(x) = \left\{ \frac{f(x)}{g(x)} \middle |  f,g \in K[X], g \neq 0 \right\}
$$
This become a field because:
$$
\left( \frac{f(x)}{g(x)} \right)^{-1} = \frac{g(x)}{f(x)} \ \text{ if } f(x) \neq 0
$$
This, however, doesn't become a "polynomial field" it becomes a field of rational function. This is due to **fractions not being polynomials** by definition anymore

#### Division over an irreducible polynomial
$K[X]$ will become a field if it is forced into being a finite one (like a [[Galois Field]] with which it's commonly used) by dividing it with an irreducible polynomial since that behaves like a prime number which ensures that every possible polynomial has a multiplicative inverse. More on that in [[Irreducibility of Polynomials]] and $GF$s