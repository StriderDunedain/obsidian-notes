---
tags:
  - math/number-theory
  - math/modular-arithmetic
updated: 2026-03-29
created: 2026-03-25
---
Also called **Restklassen** in German are classes that arise through modulo operation. Are a special case of equivalence classes (or residue classes). Further described in [[Set Relations]]

### Definition
Given $a, b \in \mathbb{Z}$ and $n \in \mathbb{N}$, $a$ and $b$ are called *congruent* mod $n$ when $n$ divides $a - b$. As official notation: $a \equiv b \text{ mod } n$ or just $a \equiv b$ if it's clear about which mod the talk's about (that just means that $a$ and $b$ have the same remainder when divided by $n$)

The possible eq. classes of mod $n$ are $\{[1], [2], [3] \dots, [n - 1]\}$.

### Operations
The addition and multiplication of cong. classes are defined as:
$$
\begin{align}
[a] \oplus [b] := [a + b]  \\
[a] \odot [b] := [a \cdot b]
\end{align}
$$
Since cong. classes can be added (or multiplied) it would follow that, e.g. $(a + b) \text{ mod } n$ belongs to the eq. class of $[a + b]$. Here's an example of these operations (powers also work, ofc):
![[congruence_classes_example.png]]
All of that is to say that, for example, (under nod 5 condition) a cong. class of $[2]$ can be added to $[1]$ to create the cong. class of $[3]$, the sum of any two elements from those two cong. classes (e.g. 11 and 12) would give you an element of cong. class three:
$$
11 + 12 = 13, \ 13 \equiv 3 \text{ mod } 5
$$

Another interesting way to write congruence classes is using the [[Quotient Group]]:
$$
\mathbb{Z}/5\mathbb{Z} = \{[0], [1], [2], [3], [4]\}
$$

### Relation to groups
Since $\mathbb{Z}/n\mathbb{Z}$ is a [[Group]], there is a need to know what the inverse of an element to the cong. class of $[m]$? The answer is, of course, $-[m]$ which is the same as actually $[n - m]$ since
$$
[m] \oplus [n - m] = [m + n - m] = [n] = [0]
$$
