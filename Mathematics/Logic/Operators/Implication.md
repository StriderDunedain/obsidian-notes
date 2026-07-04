---
tags:
  - math/logic
date: 10/10/2025
cover:
updated: 2026-03-19
created: 2025-10-11
---
Implication (→) is the most confusing operator of them all for me. Essentially meaning **if P is True then Q is True** which gives this odd-looking table:

|  P  |  Q  | P → Q |
| :-: | :-: | :---: |
|  0  |  0  |   1   |
|  0  |  1  |   1   |
|  1  |  0  |   0   |
|  1  |  1  |   1   |
Can be unfolded as:
$$ \neg P \lor Q $$
**Note:** Doesn't imply causality, rather minimal requirements for the result to be true[^1]

[^1]: For the explanation of the weird behavior for when P is false but the result is true irrelevant of Q, see [[Vacuous Truth]]
