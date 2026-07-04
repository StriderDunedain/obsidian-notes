---
tags:
  - math/set
updated: 2026-04-02
created: 2025-11-11
---
Used to map indexes on elements of a set (better to think of it like a search over sets that builds a set of results)
- **Indexed Union**:
$$ \bigcup_{i \in I} A_i := \{x|x \in A_i, \ \exists i \in I\} $$
In programmatic terms, this could be written as:
```
for i in I:
	if x in A_i:
		return True
return False
```

- **Indexed Intersection**:
$$ \bigcap_{n \in M} A_n := \{x|x \in A_n, \ \forall n \in M\} $$
```
for n in M:
	if x not in A_n:
		return False
return True 
```
