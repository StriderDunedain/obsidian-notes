---
tags:
  - math/logic
updated: 2026-05-05
created: 2026-05-04
---
Called Skolemizierung in German, this is the process of replacing predicates with existence [[Quantifiers]] to a constant $k$-arity function (called the Skolem function) that gives the result\* (one can even discard the all-quantifiers bc it's implied):
$$
\exists x \phi(x) \text{ becomes } \phi(c)
$$
However, this process preserves only satisfiability and not logical equivalence. What that means is that it preserves the [[Model (Math)]] but not the structure of the expression (i.e. gives the same result but using a different form)

### Example
$$
\forall x \exists y P(x, y) \text{ becomes } \forall x P(x, f(x))
$$
$f(x)$ here is the Skolem function and the expression overall takes the Skolem Normal Form (SNF)

### Trivia
Developed in #history/1920's by [[Thoralf Skolem]]

***
(\*) The function is actually a way of saying: "For that var $x$ how can the function give the same result as the existence-quantifiers?". E.g., $\exists y P(x, y) \text{ becomes } P(x, f(x))$ then the function $f(x)$ is gives the behavior of the existence-quantifiers through $x$