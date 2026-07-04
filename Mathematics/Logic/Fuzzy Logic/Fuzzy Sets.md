---
tags:
  - math/logic
updated: 2026-03-19
created: 2026-03-19
---
Instead of asking whether an element is in a set or not, we ask to what degree is an element in the set (i.e. how "true" it is). That is the function $\mu(x)$.

For example, the speed range is from 50 to 70 on a highway, then the closer to 50 the more true it is in the sense that it "kinda" is there plus-minus. Exactly why it's fuzzy. Serves as an extension of Boolean algebra

### Set definitions
- **Conjunction**: $(A \cup B) \ = \ max\{\mu_{A}(x), \ \mu_{B}(x)\}$
![[Pasted image 20260319014128.png]]

- **Disjunction**: $(A \cap B) \ = \ min\{\mu_{A}(x), \ \mu_{B}(x)\}$
![[Pasted image 20260319014151.png]]


- **Negation**: $\overline{A}(x) \ = \ 1 - \mu_{A}(x)$

![[Pasted image 20260319014212.png]]

