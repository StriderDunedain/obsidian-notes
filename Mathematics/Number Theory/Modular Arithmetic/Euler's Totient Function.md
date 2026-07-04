---
tags:
  - math/number-theory
  - math/modular-arithmetic
updated: 2026-05-04
created: 2026-04-06
---
Euler's Totient Function $\phi(n)$ counts how many numbers less than $n$ are *coprime* to $n$. There also exists a generalized version of this totient called [[Jordan's Totient]]

> [!summary] Coprimality
> "Coprime" means that there are no common divisors between two numbers (other than $1$). In other words: $\text{gcd}(a, b) = 1$. Note that this does not imply that either has to be a prime number – quite the contrary, in fact. Any two number could be coprime

### Prime numbers
1. If $n$ is a prime number then:
$$
\phi(n) = n - 1
$$
	Which is very logical – all previous numbers aren't going to divide $n$. Kind of like the case with [[Congruence Class]]es and there existing up to $n - 1$ of them

2. If $n = p \cdot q$ and $p$ with $q$ being distinct primes
$$
\phi(n) = (p - 1)(q - 1)
$$

### Composite numbers
> [!summary] Composite numbers
> Composite numbers are those number that are not prime or $1$

There doesn't really exists any way to count this if the number isn't prime except brute force it. This is exactly what algorithms like [[AES]] and [[RSA]] stand on. However, it's still neither proven nor disproven that such a way could be found

However, once the number if factorized the formula becomes this:
$$
\begin{align}
& \text{For a factorized number } \ n = p_{1}^{k_{1}} \cdot p_{2}^{k_{2}} \cdot + \dots + p_{m}^{k_{m}}, \\
& \text{The totient becomes: } \ \phi(n) = n \cdot \prod_{i=1}^{m}\left( 1 - \frac{1}{p_{i}} \right)
\end{align}
$$
***
**Note**: the term "totient" was coined by mathematician James J. Sylvester (who also created words like [[Matrix]], [[Graph]] and even discriminant) in #history/1879 and is derived from the Latin word $\text{tot}$ meaning "so many" and the suffix $\text{-ient}$ to match words like quotient. There didn't exist a word for it before, just a lengthy phrase