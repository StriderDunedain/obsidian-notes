---
tags:
  - math/logic
---
An important concept in [[First-Order Logic]] that dictates that a statement is true if the situation in which it could possibly be false never happens (i.e. the situation is irrelevant to the statement, that's where [[Implication]] gets it's weird-looking table). Work strictly on universal statements (i.e. those bound by the for all quantifier[^1]) . This is the basis for the proof by contradiction and generally makes proofs a lot shorter and helps avoid corner cases (like what is something is an empty set, or whatever)

### Examples
1.  All unicorns are blue
	But since there are no unicorns, the statement that they're blue is considered to be truthful since no counterexample can be found[^2]

2. Suppose $A = \emptyset$ then $\forall x \in A, x^{2} \geq 0$ will be true, since in the empty set $A$ has no element whose square is a negative (in fact for all statement of this kind, truthfulness holds: $\forall x \in \emptyset, P(x)$)

3. Suppose you want to prove that if $n^{2} = 2$ then $n$ is irrational. There's no integer $n^{2} = 2$ that satisfies that condition, hence the statement is vacuously true

4. Consider the statement: there's no even integer between 10 and 11. But since there's no integer to begin with, the statement is vacuously true (there's no counterexample of there being an odd integer between 10 and 11)

[^1]: More in [[Quantifiers]]

[^2]: Reminds me of proof by contradiction ([[Proving Statements in Logic]])