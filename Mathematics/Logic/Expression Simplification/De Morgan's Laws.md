---
tags:
  - math/logic
updated: 2026-03-19
created: 2025-11-12
---
These laws were formulated by Augustus De Morgan in 19 century but were pretty much known since Aristotle

### Laws themselves
$$
\begin{align}
\neg (A \land B) \ = \ \neg A \lor \neg B \\
\neg (A \lor B) \ = \ \neg A \land \neg B
\end{align}
$$

### Proof (for set theory)
**Part 1**
Let $x \in \overline{A \cap B}$. Then, $x \not \in A \cap B$.
Because $A \cap B = \{y | y \in A \land y \in B\}$, it must be the case that $x \not \in A \lor x \not \in B$.
If $x \not \in A$, then $x \in \overline{A}$, so $x \in \overline{A} \cup \overline{B}$.
Similarly, if $x \not\in B$, then $x \in \overline{B}$, so $x \in \overline{A} \cup \overline{B}$.
Thus, $\forall x (x \in \overline{A \cap B} \implies x \in \overline{A} \cup \overline{B})$
that is, $\overline{A \cap B} \subseteq \overline{A} \cup \overline{B}$.

**Part 2**
To prove the reverse, let $x \in \overline{A} \cup \overline{B}$, and for contradiction assume $x \not\in \overline{A \cap B}$.
Under the assumption, it follows that $x \in A \cap B$,
so it becomes $x \in A \land x \in B$, and thus $x \not\in \overline{A} \land x \not\in \overline{B}$.
However, this means $x \not\in \overline{A} \cup \overline{B}$, in contradiction to the hypothesis that $x \in \overline{A} \cup \overline{B}$,
therefore, the assumption $x \notin \overline{A \cap B}$ must not be the case, meaning that $x \in \overline{A \cap B}$.
Hence, $\forall x (x \in \overline{A} \cup \overline{B} \implies x \in \overline{A \cap B})$,
that is, $\overline{A} \cup \overline{B} \subseteq \overline{A \cap B}$.

**Conclusion**
Since $\overline{A} \cup \overline{B} \subseteq \overline{A \cap B}$ and $\overline{A \cap B} \subseteq \overline{A} \cup \overline{B}$, then $\overline{A \cap B} \ = \ \overline{A} \cup \overline{B}$
