---
tags:
  - math/discrete
  - math/computer-science
updated: 2026-04-06
created: 2026-03-25
---
> [!attention] Updates Incoming!
> In 2025 an undergrad improved the very basics of hash functions whereby some part will definitely need to be revised

A hash function is essentially a function that maps an immense input to a limited output of [[Congruence Class]]

### Definition
A hash function has the following definition:
$$
h: K \to H, k \mapsto h(k)
$$
Where:
- $K$ is the set of keys ($K \subset \mathbb{Z}$)
- $H$ is the set if indices ($\{0, 1, \dots, n - 1\}$)

### Simple example
A pretty simple example of a hash function would be:
$$
h(k) = k \text{ mod } n
$$
A good choice for $n$ is a prime number (see more as to why in "Quadratic probing" in [[Collision Resolution]])

A programmatical perspective and relation to DB in [[Hash Function (Programming Perspective)]]
