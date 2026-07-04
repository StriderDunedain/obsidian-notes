---
tags:
  - cs/recursion
updated: 2026-05-19
created: 2026-05-19
---
A tail recursion has its recursive condition entirely at the end and the return only contains the function call:
```python
def fact(n, acc=1):
	if n == 0:
		return acc
	return fact(n - 1, cc * n)
```

**Note**: to be a tail recursion the last statement has to be exclusively the returning of the function so something like `return 1 + f()` is no longer a tail recursion

To be more effective with dealing with them, the compiler oftentimes uses [[Tail Call Optimization]]