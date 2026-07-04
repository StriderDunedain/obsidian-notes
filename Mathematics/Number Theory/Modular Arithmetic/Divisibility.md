---
tags:
  - math/number-theory
  - math/modular-arithmetic
updated: 2026-03-25
created: 2026-03-25
---
The definition of divisibility is:
> Let $a, b \in \mathbb{Z}$, where $b \neq 0$ then $a$ is divisible by $b$ (or $b$ divides $a$ in signs: $b \ | \ a$) only then when there's a $q \in \mathbb{Z}$ that produces this equation: $a = bq$

Which means that $b$ fits in $a$ a whole (i.e. pertaining to $\mathbb{Z}$) number of times. Like 5 being in 15 3 times. That 3 is $q$.

### Notation
A little weird perhaps but the notation for divisibility is the following:
$$
b \ | \ a
$$
Which is a bit confusing but means that $a$ can be divided by $b$ (i.e. $6 \ | \ 12$)

### Rules
1. If $c \ | \ b$ and $b \ | \ a$ then $c \ | \ a$: ($3 \ | \ 6$ and $6 \ | \ 18 \implies 3 \ | \ 18$)
2. If $b_{1} \ | \ a_{1}$ and $b_{1} \ | \ a_{2}$ then $b_{1}b_{1} \ | \ a_{1}a_{2}$: ($3 \ | \ 6$ and $4 \ | \ 8$ then $12 \ | \ 48$)
3. If $b \ | \ a_{1}$ and $b \ | \ a_{2}$ then for $\alpha, \beta \in \mathbb{Z}: b \ | \ \alpha a_{1} + \beta a_{2}$
4. If $b \ | \ a$ and $a \ | \ b$ then $a = ±b$

Further in [[Modulus]]