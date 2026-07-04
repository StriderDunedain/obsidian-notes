---
tags:
  - cs/recursion
updated: 2026-05-19
created: 2026-05-19
---
This recursion has its recursive case happen first (or almost first, generally "head" meaning "not the last line"[^1]):
```python
def print_numbers(n):
	if (n == 0):
		return
	print_numbers(n - 1)
	print(n)
```
This approach is very useful when dealing with reverse processing of something

[^1]: Compare with [[Tail Recursion]]
