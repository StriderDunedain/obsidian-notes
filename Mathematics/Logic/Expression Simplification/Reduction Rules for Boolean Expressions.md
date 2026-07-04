---
tags:
  - math/logic
updated: 2026-06-11
created: 2026-03-18
"created ": 2026-03-19
---
A *Tautology* $\phi$ is when an expression is always true and *Antilogy* $\psi$ (or *Contradiction*) is when it's always false

### Main laws
**Kommutativität**
- $a \land b = b \land a$
- $a \lor b = b \lor a$

**Assoziativität**
- $(a \land b) \land c = a \land (b \land c)$
- $(a \lor b) \lor c = a \lor (b \lor c)$

**Distributivität**
- $a \land (b \lor c) = (a \land b) \lor (a \land c)$
- $a \lor (b \land c) = (a \lor b) \land (a \lor c)$

### Smaller ones
- $a \land 1 = a$
- $a \lor 0 = a$

**Complementing element**
- $a \land \neg a = 0$
- $a \lor \neg a = 1$

**Idempotency**
- $a \land a = a$
- $a \lor a = a$

**Involutivitat**
- $\neg(\neg a) = a$

**Absorption**
- $(a \land b) \lor a = a$
- $(a \lor b) \land a = a$

**Auslöschung**
- $a \land (b \lor \neg b) = a$
- $a \lor (b \land \neg b) = a$

See also: [[De Morgan's Laws]]