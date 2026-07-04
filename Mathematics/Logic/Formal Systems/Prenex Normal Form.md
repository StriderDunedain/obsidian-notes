---
tags:
  - math/logic
updated: 2026-05-05
created: 2026-05-04
---
Abbreviated to PNF (or Pränexform) is a form of predicate logic expressions that follows this form:
$$
Q_{1}x_{1} Q_{2}x_{2} \dots Q_{n}x_{n}G
$$
Where $Q_{i}$ are [[Quantifiers]], $x_{i}$ are variables and $G$ is a formula that doesn't have quantifiers (also called the matrix). Essentially, that means that all quantifiers have to be in the front. Like this:
$$
\forall x \exists y(P(x) \to Q(y))
$$

### Transformations
The transformations are pretty intuitive (see [[Quantifiers]] for more) and try renaming the variables to avoid confusion. Resolve complex logic operations ([[Reduction Rules for Boolean Expressions]]) and move negation as close to the predicates as possible then get all the quantifiers out as far as possible away from the quantifiers; if you can make it to beyond the expression (i.e. $\text{<quantifiers>(<expression>)}$) then it's PNF

Another useful method is [[Skolemization]]

### Trivia
The name comes from Latin: "pre-" for before and "nexus" for binding, connection. Literally meaning "binding in front". The goats that developed it are [[David Hilbert]] and [[Wilhelm Ackermann]]

***
A "bereinigt" form is a NF without variables