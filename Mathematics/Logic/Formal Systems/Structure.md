---
tags:
  - math/logic
updated: 2026-05-05
created: 2026-05-01
---
A sematic structure (a.k.a. interpretation) $\frak{A}$ (that's an A) is something that gives meaning to formulas.

It tells how to interpret everything: constants, functions, predicates, etc. Formally, it consists of a domain (the Universe $U$) and interpretation of symbols. E.g. for a structure $\alpha = (U, \phi, \psi, \xi)$ the part mean:
- $U$ the **universe** – anything everything else refers to (the objects upon which operations will be executed)
- **Interpretations** $(\phi, \psi, \xi)$:
	- Every constant $c$ is assigned a specific object $c^{\phi} \in U$ (just that a constant $c = 2$ is always equal to $2$)
	- Every function $f$ with arity of $n$ has a [[Mapping]] $f^{\phi}: U^{n} \to U$
	- Every predicate $P$ with the arity of $n$ has a relation $P^{\phi} \subseteq U^{n}$ (that means that a predicate becomes a set of tuples of objects (i.e. describes something that can be either true of false))
	- Every free variable $x$ has an element $x^{\xi} \in U$ (also the same stuff with us having to assign a meaning first, blah-blah-blah)

A [[Model (Math)]] is a special kind of structure where a formula is true

So basically:
- $\phi$ refers to functions
- $\psi$ refers to predicates
- $\xi$ refers to variables