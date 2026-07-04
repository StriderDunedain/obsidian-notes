---
tags:
  - math/geometry
---
> [!abstract] Definition
> A line $y = ax + b$ is an asymptote of a function $f(x)$ if:
> $$
> \lim_{ x \to \infty } (f(x) - (ax + b)) = 0
> $$

Essentially, with $x$ going to infinity, the $f(x)$ will converge with $y$

### Computer Science definition
It is worth noting, however, that the computer science definition of an asymptote is somewhat looser than the mathematical one. Instead of having a line to which a function converges, the CS asymptote measures the rate of change:
$$
T(n) = 3n^{2} + 7n + 10
$$
Then
$$
\frac{T(n)}{n^{2}} = 3 + \frac{t}{n} + \frac{10}{n^{2}}
$$
Taking the [[Limit]]
$$
\lim_{ n \to \infty } \frac{T(n)}{n^{2}} = 3
$$
So, as one can see, this says that $T(n)$ behaves like $3n^{2}$ and not that it converges (which is proven by the statement below that trivially grows to infinity)
$$
T(n) - 3n^{2} = 7n + 10
$$