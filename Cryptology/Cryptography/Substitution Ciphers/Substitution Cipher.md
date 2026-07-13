---
tags:
  - cryptography/cipher-type
updated: 2026-07-11
created: 2026-07-11
---
This is a cluster of [[Monoalphabetic Cipher]]s and [[Polyalphabetic Cipher]]s that rely on switching up the position of letters by some algorithm (usually addition or multiplication and then mod'ing[^1] it). Types are:
- [[Additive Cipher]]
- [[Multiplicative Cipher]]
- [[Affine Cipher]]
- [[Keyword Cipher]]
- [[Homophonic Cipher]]
By adding / multiplying cleartext is meant the respective index of the letter in the alphabet. Mod'ding ensures that the indexes stay inside the [[Cardinality]] of the alphabet (its length)

[^1]: Further in [[Modulus]]
