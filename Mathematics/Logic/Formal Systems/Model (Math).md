---
tags:
  - math/logic
updated: 2026-05-05
created: 2026-05-01
---
A structure $\frak{A}$ (or $\alpha$ as THI would write it) is a **model** of $F$ when $\mathfrak{A}(F) = 1$ (where the formula is true). That we denote as $\mathfrak{A} \models F$ (more in [[Semantic Consequence]]). Could also be written as $\mathcal{A}$
Facts:
- A formula $F$ is tautological if it's true regardless of the structure
- A formula $F$ is satisfiable if there's a model for it
- F is unsatisfiable when $\neg F$ is a tautology

1. A structure $\mathfrak{A}$ is a model of a set of formulas $F$ if it makes every formula in the set true: $\mathfrak{A} \models F$
2. Two formulas are semantically equivalent if they are true in exactly same structures: $F \equiv G$
3. ibid. it would follow that when that's the case then when $F$ is true then $G$ must also be true
4. Two formulas $F$ and $G$ are semantically equivalent ($F \equiv G$) when $F \models G \land G \models F$
5. Substitution theorem (two things are the same -> replacement doesn't do anything). If $F_{1}$ and $F_{2}$ are $F_{1} \equiv F_{2}$ and $G$ is a "sub-formula" of $F_{1}$ so to say then $G \equiv F[F_{1}/F_{2}]$. That means that $F_{1}$ and $F_{2}$ can be replaces in $G$ without making any difference


To show that a model is satisfiable, one has to prove that for all expressions $F_{i}$: $F_{1} \land F_{2} \land \dots \land F_{n}$