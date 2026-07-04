---
tags:
  - cs/architecture
updated: 2026-03-22
created: 2026-03-12
---
Also called the *excess-N* representation, or *Exzessdarstellung*, is a way of storing negative numbers using only positive values through a bias:
$$
\text{value = x + bias}
$$

Heavily used in floating-point notations like [[IEEE 754]]
***

For a bias of $8$ this would look like:

| **Value** | **Stored value** |
| :-------: | :--------------: |
|    -3     |        5         |
|    -2     |        6         |
|    -1     |        7         |
|     0     |        8         |
|     1     |        9         |
