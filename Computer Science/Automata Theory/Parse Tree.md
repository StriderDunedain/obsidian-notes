---
tags:
  - cs/automata
updated: 2026-05-01
created: 2026-05-01
---
This is a way to represent the building of a language through a tree. I loved the concept when I saw it somewhere that approximates functions' values using this somehow by building trees of operations and operators, tweaking little parts to get to a better and better result. It's also called Ableitungsbaum in German or a derivation tree in English

Also a grammar is ambiguous if there exists a [[String]] that can be formed using two different parse trees

Now the rigorous stuff from the lecture. A tree $T = (V, E, v_{0})$ has nodes in $V$, sides in $E$ and root at $v_{0}$:
- The root $v_{0}$ is denoted as $S$
- Every inner variable (non-terminal) is marked $N$
- Every leaf is a terminal from $\Sigma \cup \{ \epsilon \}$

### Example
- $G = (\{ S, A, B \}, \{ a, b \}, P, S)$ with $P = \{ S \to AB, A \to aaA | \epsilon, B \to Bb | \epsilon \}$
- A derivation $S \Rightarrow AB \Rightarrow aaAB \Rightarrow aaABb \Rightarrow aaBb \Rightarrow aab$
- The tree would look like:
![[Pasted image 20260501230846.png]]
The language $L(G) = \{ a^{2m}b^{n} \ | \ m,n \geq 0 \}$

A control word (Kontrollwort) is just a way of writing down derivations by their names and not their results. So instead of $aSb \Rightarrow aaSbb$ you get $S, A$ where $S \to aSb, A \to aSb$. Sometimes also encoded by the number of the derivation. Denoted as $\pi$