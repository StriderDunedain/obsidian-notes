---
tags:
  - math/logic
updated: 2026-05-05
created: 2026-03-17
---
The most important concept of [[Predicate Logic]] and the most common ones are, of course, the All Quantifier: $\forall$ and Exists Quantifier: $\exists$. In German these are called quantors

In cases where the variable is quantified, it is said to be *bound*

### Rules
$$
\begin{align} \\
\text{Negation of quantifiers:} \\
& \neg \forall x F \equiv \exists x \neg F  \\
& \neg \exists x F \equiv  \forall x \neg F \\
 \\
\text{Order of quantifiers:} \\
& \forall x \forall y F \equiv \forall y\forall x F  \\
& \exists x\exists y F \equiv  \exists y \exists x F \\
 \\
\text{Quantifiers and } \land, \lor: \\
 & \forall xF \land \forall x G \equiv  \forall x(F \land G) \\
  & \exists x F \lor \exists G \equiv  \exists x (F \lor G)
\end{align}
$$
**However!**
$$
\begin{align}
& \forall x \exists y F \not\equiv \exists y\forall xF \\
& \forall x F \lor \forall x G \not\equiv \forall x(F \lor G) \\
& \exists x F \land \exists x G \not\equiv \exists x (F \land G)
\end{align}
$$
---
Another important concept that relates to quantifiers is the [[Vacuous Truth]]