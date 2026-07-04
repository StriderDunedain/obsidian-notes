---
tags:
  - math/set
updated: 2026-04-13
created: 2025-11-11
"created ": 2025-11-12
---

A **Relation** on a class can be expressed more succinctly as follows:
$$(a, b) \in R = aRb$$

1. **Reflexivity:** Everything is always in the same group as itself (I have the same birthday as myself)
$$\forall x \in M, \ xRx $$

2. **Symmetry:** If A is in the same group as B then B is in the same group as A (if my friend has the same birthday as me then I have the same birthday as my friend) 
$$\forall x, y \in M, \  xRy \ \implies \ yRx$$

3. **Transitivity:** If A is B, B is C then A is C (if my friend has a friend then that friend is my friend)
$$\forall x, y, z \in M, \ (xRy \wedge yRz) \implies xRz$$

4. **Equivalence:** when a relation is reflexive, symmetric and transitive (thus is formed an equivalence class)
$$ [a] := \{x \in M \ | \ xRa\}$$

Naturally:
- For any given relation there exists only one EC (equivalence class)
- A union of all EC of a set gives that set

### Other Relations
#### Partially Ordered Sets, or Posets (geordnete Menge)
A key property of a poset is **Antisymmetry:** If $A$ has a relation to $B$ and $B$ has a relation to $A$ then $A$ has to equal $B$:
$$a \preceq b \ \wedge \ b \preceq a \implies a = b$$
The curvy less or equals is just a generic way of saying a is lesser to b (partielle Ordnung). Basically equality of two elements

A neat way of representing poset relations is through [[Hasse Diagram]]s

#### Total Order, or Linear Order (Vollständige od. Lineare Ordnung)
A special case of a poset where every element is comparable:
$$a \preceq b \ \vee \ b \preceq a$$


#tba Refine this note. Add more to posets and definitions of relations