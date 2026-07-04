---
tags:
  - cs/cryptography
updated: 2026-05-07
created: 2026-04-05
---
> [!attention]
> Diffie-Hellman (DH) is not an encryption algorithm but rather a key exchange protocol

It was invented in #history/1976 by Whitfield Diffie and Martin Hellman and is the first public-key idea ever (compare to [[RSA]]). It relies on the [[Discrete Logarithm Problem]]

### Principle
1. First agree on a large prime number $p$ and a base (generator) $g$
2. Let two parties pick two values $a$ and $b$ and not share what these are
3. Let one party compute $A = g^{a} \text{ mod } p$ and the other $B = g^{b} \text{ mod } p$
4. Exchange the computed values
5. Let the first party compute $S = B^{a} \text{ mod } p$ and the other $S = A^{b} \text{ mod } p$ to get the same number back

### Example
1. Let $p = 23$ and $g = 5$ (these are shared freely)
2. Alice picks $a = 6$ and Bob pick $b = 15$ (those are never shared)
3. Alice computes $A = g^{a} \text{ mod } p = 5^{6} \text{ mod } 23 = 8$
4. Bob computes $B = g^{b} \text{ mod } p = 5^{15} \text{ mod } 23 = 19$
5. Alice sends $8$ and Bob sends $19$
6. Alice computes $S = B^{a} \text{ mod } p = 19^{6} \text{ mod } 23 = 2$
7. Bob computes $S = A^{b} \text{ mod } p = 8^{15} \text{ mod } 23 = 2$

> [!faq] How does this work?
> This is due to this: $(g^{a})^{b} = (g^{b})^{a} = g^{ab} \text{ mod } p$