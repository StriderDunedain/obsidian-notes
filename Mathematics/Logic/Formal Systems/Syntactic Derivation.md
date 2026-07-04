---
updated: 2026-05-05
created: 2026-05-04
tags:
  - math/logic
---
A way of obtaining a formula in a formal system through axioms and [[Inference Rules]]. Concept has deep connections with automata theory (like [[Context Free Grammar]])

Let $\mathcal{L}$ be a formal language (e.g. predicate logic), $\Gamma$ be a set of formulas (assumptions / premises) and $\phi$ be a formula. Then:
$$
\Gamma \vdash \phi
$$
means that there exists a finite set of formulas ending in $\phi$ where each step is: an axiom, an element of $\Gamma$, or a statement that follows by inference. All of that is to say that $\phi$ is proved through $\Gamma$

### Structure
A derivation is a finite sequence:
$$
\phi_{1}, \phi_{2}, \dots, \phi_{n} = \phi
$$
Such that for each $\phi_{i}$:
1. $\phi_{i} \in \Gamma$, or
2. $\phi_{i}$ is a axiom, or
3. $\phi_{i}$ follows by inference

### Example
[[Modus Ponens]] can be modelled using syntactic derivation:
$$
\frac{P \to  Q \quad P}{Q}
$$
1. $P \to Q$ is a premise
2. $P$ is also a premise
3. $Q$ (from 1. and 2. by modus ponens)

So it becomes:
$$
\{ P \to  Q, P \} \vdash Q
$$

***
- The symbol $\vdash$ is called the "turnstile" or "syntactic derivation"

Is one of the foundations for [[Gödel's Incompleteness Theorem]], [[SAT]]s and other automated proving systems as well as a ton of other stuff. See also [[Semantic Consequence]]