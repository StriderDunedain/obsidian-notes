---
tags:
  - tba-place
---
> Sub-types should be substitutable for their base types

In practice, this means that a child shouldn't do all the stuff just bc the parent has it. Restrict the behavior only in such a way that allows for substitution of parents without breaking the logic

---

### ❌ Bad Example
So this would be wrong (bc a pengling doesn't fly but now it has such a method)
```python
class Bird:
	def fly():
		...

class Pengling(Bird):
	...


pengling = Pengling()
pengling.fly()  # Shoudn't be possible - penglings don't fly
```

### ✅ Fixed Version
To mitigate this one could use something like that
```python
class Bird
	...

class FlyingBird(Bird):
	def fly():
		...

class Pengling(Bird):  # Can't fly no more
	...
```
