---
tags:
  - cs/python
updated: 2026-05-27
created: 2026-05-27
---
1. This is another way of searching up a value by a tuple-key:
```python
some_dict[a, b, c]  # equiv to...
some_dict[(a, b, c)]
```

2. `assert`s with tuples always evaluates to truthy:
```python
assert (x < y, y > z)  # tuples are always truthy, unless empty
```
3. [[Mutable Defaults in Functions]]