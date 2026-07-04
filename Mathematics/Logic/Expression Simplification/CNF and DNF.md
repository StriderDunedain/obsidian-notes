---
tags:
  - math/logic
date: 2010-10-10
cover:
updated: 2026-03-19
created: 2025-10-11
---
**Conjunctive Normal Form** and **Disjunctive Normal Form** are two approaches to ordering logical expressions. The former favors conjunction (i.e. AND) over OR while the latter favors disjunction (i.e. OR) over AND which dives following results:
$$
CNF:\;\;(A \ \vee \ B) \; \wedge \; (A \vee B) \; \dots
$$
$$
DNF:\;\;(A \ \wedge \ B) \; \vee \; (A \wedge B) \; \dots
$$
Sometimes called **Product of Sums** (POS, i.e. CNF) or **Sum of Products** (SOP, i.e. DNF)

SAT-Solvers usually expect CNF as input.

A set of sets in CNF is called a **Klausel** (clause) and serves as a one and only way of describing an expression. Further in [[Resolution]]