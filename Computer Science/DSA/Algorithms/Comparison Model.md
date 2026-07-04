---
tags:
  - cs/algo
---
This is the restriction on comparison algorithms saying that:
> [!abstract] Restriction
> No comparison algorithm can run below $O(n \log n)$[^1]

Not really proven by anyone (somehow?..). Stems from a very simple chain of reasoning involving decision [[Tree]]s:
1. There are $n!$ possible [[Permutation]]s
2. Each comparison gives two outcomes
3. Therefore each comparison gives one bit of information
4. So distinguishing among $n!$ possibilities requires at least:
$$
\log_{2}n!
$$
comparisons. Using [[Sterling's Approximation]] we get:
$$
\log_{2} n! = \Theta(n \log n)
$$

[^1]: Look more to [[Asymptotic Notation]]
