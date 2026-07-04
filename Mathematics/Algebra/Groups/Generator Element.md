---
tags:
  - math/algebra
  - math/group-theory
updated: 2026-04-06
created: 2026-04-06
---
Also called a *primitive element* or *erzeugendes Element* this is an element that can produce every other element on a group by repeated application of the group operation

> [!faq] How many generators are there in a group?
> In a group of size $n$ the number of generators is the number produced by [[Euler's Totient Function]] – i.e. $\phi(n)$

### Definition
A number $g$ is a generator if:
$$
g^{1}, g^{2}, g^{3}, \dots, g^{p - 1} \text{ mod }  p  
$$
Produces all the numbers in a set (from $1$ to $p - 1$). A more formal definition is:
$$
G = \{g^{k} \ | \ k \in \mathbb{Z} \}
$$
### Example
For example in a [[Galois Field]] $GF(7)$ which consists of $\{1, 2, 3, 4, 5, 6\}$ the generator $g = 3$ since:
$$
\begin{align}
& 3^{1} \text{ mod } 7 = 3 \\
& 3^{2} \text{ mod } 7 = 2 \\
& 3^{3} \text{ mod } 7 = 6 \\
& 3^{4} \text{ mod } 7 = 4 \\
& 3^{5} \text{ mod } 7 = 5 \\
& 3^{6} \text{ mod } 7 = 1
\end{align}
$$
> [!summary] Cyclical groups
> A cyclical group is such a group that has a generator. Which means that by applying an operation one can reach any number in this group

***
There doesn't exist an algorithm that can compute even the number of generators (let alone their values) in a group. I suspect it could be an avenue of cracking either the factorization or the [[Discrete Logarithm Problem]]s