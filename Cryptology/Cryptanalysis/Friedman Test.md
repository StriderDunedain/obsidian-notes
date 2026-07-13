---
tags:
  - cryptanalysis/cipher-breaking
updated: 2026-07-11
created: 2026-07-11
---
This test works on [[Homophonic Cipher]]s to determine the **index of coincidence** (denoted as $I$) which answers the question: *"If one selects a pair of letters from a ciphertext what's the probability that these are the same cleartext letters?"*. Sometimes also called the Kappa test (bc the guy called it that)The reasoning to finding the formula are pretty easy and don't require that much math but I'm just going to say that an amazing job has been done describing it in this book: [[Cryptology]]. So, without further do, here's the formula:
$$
I = \sum_{i=1}^{M}\frac{n_{i}(n_{i} - 1)}{n(n - 1)}
$$
It tells us whether we are working with a [[Monoalphabetic Cipher]] or a [[Polyalphabetic Cipher]]. Why? Bc the index of coincidence stays invariant in monoalphabetic ciphers (due to there being a bijection[^1], or in other words a direct and only correlation, "c" is only "c", no other letter). So if the index is significantly[^2] lower than the standard distribution][^3] of pairs in the cleartext of a language then that means we're dealing with a polyalphabetic cipher

[^1]: More on that in [[Mapping]]s

[^2]: #tba I still don't know what does "significantly" mean

[^3]: #tba Doe sit have anything to do with actual one? Or am I just tripping?

#tba The internet is showing some other more complicated formula. I feel like the current description from the book [[Cryptology]] is somewhat simplified
