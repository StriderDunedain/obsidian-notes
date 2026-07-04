---
tags:
  - math/logic
updated: 2026-03-25
created: 2026-03-19
---
A process of simplifying clauses in logic expressions like the following to derive the *resolvent* by using complementary literals in CNF:
$$
(C_{1} \lor P) \land (C_{2} \lor \neg P) \iff (C_{1} \lor C_{2}) \text{ is a "resolvent"}
$$
A *literal* is an element (or its complement) from a set:
$$
\text{Literal } P =
\left[
\begin{array}{l}
x \in A \\
x \not\in A
\end{array}
\right.
$$

An empty resolution is described with $\bot$ or $\emptyset$ and means a **contradiction** and that clauses are **unsatisfiable**

### Algorithm
- Turn an expression to CNF
- Start eliminating one complementing literal after another
- If at the end there's nothing but empty set, then it's a contradiction, else that's the minimized version

If using the normal resolution, the way goes like this:
$$
\begin{align}
& K = \{\{x, y\}, \{\neg x, y\}, \{z\}, \{\neg z, y\}\} \\
& Res^0(K) = K \cup\{\{y\}, \{y\}\} \\
& Res^1(K) = Res^0(K) \cup \{\{y\}\}
\end{align}
$$

### Solving strategies
**Unit Propagation (Einheitsresolution)**: Find a clause of just one variable and delete it from all other clauses and repeat it