---
tags:
  - cs/recursion
updated: 2026-05-19
created: 2026-05-19
---
These are some of the generalized recursion patterns that preserve the structure (like [[Homomorphism]]s and the like)

#### Catamorphism
A catamorphism is a fold or a reduction. Like sum or reduce (like the one from python):
```python
def sum_list(lst):
	if not lst:
		return 0
	return lst[0] + sum_list(lst[1:])
```

#### Anamorphism
That's the opposite of catamorphism. Instead of consuming a structure an anamorphism creates it. An example would be list generation:
```python
def countdown(n):
	if n == 0:
		return []
	return [n] + countdown(n - 1)
```

#### Hylomorphism
A mix of both a catamorphism and an anamorphism. Something that creates a structure and reduces it at the same time. Like [[Merge Sort]]

Some others include, but are not limited to: paramorphism, apomorphism, histomorphism and futumorphism