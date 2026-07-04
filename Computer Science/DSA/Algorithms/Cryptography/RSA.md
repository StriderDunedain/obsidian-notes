---
tags:
  - cs/cryptography
updated: 2026-04-06
created: 2026-04-05
---
Invented in #history/1977 by Ron Rivest, Adi Shamir and Leonard Adleman

### Principle
1. Choose two large primes $p$ and $q$. Keep them a secret and construct a number $n = p \cdot q$
2. Compute [[Euler's Totient Function]]:
$$
\phi(n) = (p - 1)(q - 1)
$$
3. Choose a *public* exponent $e$ such that:
$$
1 < e < \phi(n), \quad \text{gcd}(e, \phi(n)) = 1
$$
4. Compute a *private* exponent $d$ as modular inverse (can be done using the [[Extended Euclidean Algorithm]] since we are searching, essentially, for $d \cdot e - k \cdot \phi(n) = 1$):
$$
d \cdot e \equiv 1 \ \text{ mod } \phi(n)
$$
5. The result pairs are: $(e, n)$ — the public key and $(d, n)$ — a private key

Now for the en- and decryption parts (based on the [[Euler's Theorem]]):
#### Encryption with public key
The $C$ is also called the ciphertext and $M < n$
$$
C = M^{e} \ \text{ mod } n
$$
#### Decryption with private key
$$
M = C^{d} \ \text{ mod n}
$$

### Example
> [!attention] Word of caution
> RSA uses 2048-bit+ numbers, here smaller ones are used for clarity

1. Let $p = 7$ and $q = 11$. Then $n = p \cdot q = 7 \cdot 11 = 77$
2. Euler's totient is $\phi(n) = (p - 1)(q - 1) = 6 \cdot 10 = 60$
3. Let $e = 7$ (it's coprime to $60$)
4. Compute $d \cdot e \equiv 1 \quad \text{mod } 60$:
$$
\begin{align}
\text{gcd}(60, 7): \\
& 60 = 7 \cdot 8 + 4 \\
& 7 = 4 \cdot 1 + 3 \\
& 4 = 3 \cdot 1 + 1 \\
& 3 = 1 \cdot 3 + 0 \\
\\
\text{Bezout's identities:} \\
& 1 = 4 - 3 \cdot 1 \\
& 1 = 4 - 1 \cdot(7 - 4 \cdot 1) = 4 \cdot 2 - 7 \\
& 1 = 2 \cdot(60 - 7 \cdot 8) - 7 = 2 \cdot 60 - 7 \cdot 16 - 7 = \\
& = 2 \cdot 60 - 7 \cdot 17
\end{align}
$$
And we need the number associated with $e$ which is $-17$ but we need $d$ which is found like this: $-17 \text{ mod } 60 = 43$ (more on why this happened in [[Modulus]])

This is how we got $(7, 77)$ for public key and $(43, 77)$ for the private one. In order to encrypt the message do this (under the condition that $M = 13$):
$$
C = M^{e} \quad \text{ mod } n \implies C = 13^{7} \quad \text{ mod } 77 = 71
$$
To decode use this (modular exponentiation):
$$
M = C^{d} \quad \text{ mod } n \implies M = 71^{43} \quad \text{ mod } 77 = 13 
$$

> [!faq] Why does the en- and decryption work?
> Excellent question. It's because of the mapping $\mathbb{Z} \to \mathbb{Z} / n\mathbb{Z}, \ z \mapsto z \text{ mod } n = [z]_{n}$ which is a [[Homomorphism]]. There's also a proof of that but my brain is, as the lower line states, already cooked (+ all the undereating doesn't help with understanding the material)

This is literally the hardest piece of algorithm I have ever had to deal with. I'm probably going to write a code version of this sometime later but for now my brain is cooked