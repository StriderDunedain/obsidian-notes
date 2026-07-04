---
tags:
  - math/combinatorics
updated: 2026-03-25
created: 2026-03-25
---
A **combination** (a.k.a. **binomial coefficient**) is such an arrangement of elements where the order of the element doesn't matter (i.e. $\{A, B\} = \{B, A\} = 1$ element). The basics are: $n$ is the number of elements and $k$ is the length of the output arrangements (read as $n$ choose $k$)

### Building an arrangement: sans repetition
> If the duplication isn't wanted, then the formula is

$$
\binom{n}{k} = \frac{n!}{k!(n - k)!}
$$
So for $\{A, B, C\}$ choose 2 the result would be: $\{\{AB\}, \{AC\}, \{BC\}\}$. Interestingly, it the result can also be acquired using Pascal's triangle:
![[Pasted image 20260325132507.png]]

### Building an arrangement: with repetition
> If repetitions are allowed (i.e. $\{AA\}$) the the formula becomes:

$$
\binom{n + k - 1}{k}
$$

For the same set $\{A, B, C\}$ choose 2 the result is: $\{\{AB\}, \{AC\}, \{BC\}, \{AA\}, \{BB\},\{CC\}\}$


### Further uses
The following formula is used to produce formulas of sum of products (формулы скоращенного умножения):
$$
(x + y)^n = \sum_{k=0}^n\binom{n}{k}x^{n-k} \cdot y^k
$$
Here's a quick example of a formula that would come out of it: $(x + y)^2 = x^2 + 2xy + y^2$

### Special cases for fast counting
1. Sum of sums
$$
\sum_{k=m}^nA(k) + \sum_{k=m}^n B(k) = \sum_{k=m}^n(A(k) + B(k))
$$

2. Multiplication by a constant
$$
c \cdot \sum_{k=m}^n A(k) = \sum_{k=m}^n ( c \cdot A(k))
$$

3. Moving the index
$$
\sum_{k=m}^m A(k) = \sum_{k=m + 1}^{n + 1} A(k - 1)
$$

4. Changing the range
$$
\sum_{k=m}^n A(k) = A(m) + \sum_{k=m + 1}^n A(k) = \sum_{k=m}^{n - 1} A(k) + A(n)
$$
