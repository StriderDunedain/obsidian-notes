---
tags:
  - math/theorem
  - math/complex-number
updated: 2026-03-30
created: 2026-03-29
---
This is exactly the answer to a question that has been nagging me for years...

> [!abstract] Question
>  Is there anything beyond $\mathbb{C}$? 

The answer: it doesn't make sense to have anything over $\mathbb{C}$ since it is algebraically closed which means that to any polynomial you can think of there exists a solution inside $\mathbb{C}$

### Fundamental Theory of Algebra
> Every non-constant (relying on a variable) polynomial in $\mathbb{C}[X]$ has at least one root (Nullstelle) in $\mathbb{C}$

Essentially this means that for any polynomial you can think of there exists a solution to it that would fall under the umbrella of $\mathbb{C}$

Moreover, every polynomial $f \in \mathbb{C}[X]$ with $deg(f) = n$ has **exactly** $n$ roots and there are $a, x_{1}, x_{2}, \dots, x_{n} \in \mathbb{C}$ with $a \neq 0$ such that:
$$
f(x) = a(x - x_{1}) \times \dots \times (x - x_{n})
$$

A [[Field]] $K$ is called *algebraically closed* (algebraisch abgeschlossen) when every non-constant polynomial from $K[X]$ has a root in $K$ (which means that a solution to a polynomial over a field has to be inside that field)

So...
> $\mathbb{C}$ is algebraically closed

More in [[Polynomial Ring]]s