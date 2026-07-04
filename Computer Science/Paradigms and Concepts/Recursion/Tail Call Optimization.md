---
tags:
updated: 2026-05-19
created: 2026-05-19
---
TCO for short, this is something the compilers use to optimize [[Tail Recursion]] by transforming it into an iterative structure like a while or a for loop. This is mainly done so that it wouldn't rake up so much space on the heap, after all function calls stack so the space[^1] occupied is $O(n)$ but with a linear iterative approach it becomes $O(1)$

[^1]: More in [[Asymptotic Notation]]
