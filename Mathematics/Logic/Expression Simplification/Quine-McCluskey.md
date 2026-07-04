---
tags:
  - math/logic
updated: 2026-03-29
created: 2026-03-18
---
Using [[CNF and DNF]] as well as [[Reduction Rules for Boolean Expressions]], this is a way to simplify logical expressions

### Algorithm
It is suspiciously close to [[Dynamic Programming]] (esp. Divide & Conquer)
1. Express everything as SOP (i.e. DNF)
2. Look for commonalities between terms
3. Simplify
4. Repeat

Whatever's left (prime implicants) is the simplified version of the expression
A "grander" version of this are the [[Karnaugh Diagrams]]

![[Pasted image 20260329152725.png]]