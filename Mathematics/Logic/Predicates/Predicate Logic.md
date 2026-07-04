---
tags:
  - math/logic
updated: 2026-05-05
created: 2026-03-22
---
Predicate logic is a superset of Boolean logic that adds stuff like predicates, [[Quantifiers]] and relations between concepts. Predicates control their "universe of discourse", or simply, "domain" (Individuenbereich for German)

Essentially, it adds concepts like $\exists \text{ and } \forall$ as well as relations like: *if all humans are mortal then Socrates is mortal*.

Gives "structure" to the expressions of Boolean logic.

### Important definitions
- **Predicate**:
	A formula of predicate logic that returns either true or false ($n$ is even)
- **Formula**:
	 Something that returns a value. Predicate are also (as well as joined by some operations predicates) formulas of predicate logic 
- **Expression (Aussage)**:
	An expression is a statement that you can't go lower. Also if a predicate is quantified it becomes an expression ($\forall n \in \mathbb{N}$, $n$ is even)
- **Arity (Stelligkeit)**:
	Property of functions that says how many arguments it takes minus all arguments that have been quantified (i.e. $\forall x A(x, y) : x^2 > y$ has the arity of $1$ (it also becomes an expression)). Quantifiers "bind" the arguments