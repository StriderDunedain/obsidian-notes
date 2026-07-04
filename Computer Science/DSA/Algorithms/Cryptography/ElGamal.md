---
tags:
  - cs/cryptography
updated: 2026-04-06
created: 2026-04-06
---
This is a cryptographic algorithm that is built upon [[Diffie-Hellman]] and turns it into a proper algorithm

#### Key generation
1. Pick a prime number $p$ out of $GF(p)$ (more in [[Galois Field]]), a generator $g$ (more in [[Generator Element]]) and a private key $x$
2. Compute the public key: $y = g^{x} \text{ mod } p$

#### Encryption
1. Pick a random $k$
2. Compute:
$$
\begin{align}
& c_{1} = g^{k} \text{ mod } p \\
& c_{2} = m \cdot y^{k} \text{ mod }  p  
\end{align}
$$
Ciphertext = $(c_{2}, c_{2})$

#### Decryption
1. Receiver computes $s = c_{1}^{x} = (g^{k})^{x} = g^{kx}$
2. $m = x_{2} \cdot s^{-1} \text{ mod } p$

Yeah, no, algos are enough...