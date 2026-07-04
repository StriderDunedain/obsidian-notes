---
tags:
  - math/combinatorics
  - math/permutation
updated: 2026-03-25
created: 2026-03-25
---
A permutation is an arranging of elements where order matters (compare with [[Combination or Binomial Coefficient]])

### Build arrangements: sans repetition
> Without repetition, elements of number $n$ can be arranged $n!$ different ways.

For example, $\{A, B, C\}$ can be arranged into $\{\{ABC\}, \{ACB\}, \{BAC\}, \{BCA\}, \{CAB\}, \{CBA\}\}$. So $3$ elements can be arranged $3!$ different ways – i.e. $6$ ways

### Build arrangements: of length $k$
>To build arrangements of certain length $k$, the formula is $n^k$, where $n$ is the number of elements in the origin

So for the set $\{A, B, C\}$ and $k = 2$ the arrangements are: $\{\{AA\}, \{AB\}, \{AC\}, \{BA\}, \{BB\}, \{BC\}, \{CA\}, \{CB\}, \{CC\}\}$

### Build arrangements: if there're repeating elements
> If there are repeating elements in the origin (like in the word Mississippi), use this formula to count only unique pairs:

$$
\frac{n!}{\prod_{i=1}^{m} {k_{n}!}}
$$
Where $k_{n}$ is the number of the elements in the origin (like for $M: k = 1$ and for $S: k = 4$)