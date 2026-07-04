---
tags:
  - cs/automata
updated: 2026-05-01
created: 2026-04-23
---
Also called a Zeichenkette in German, this is exactly what is is in cs/. From a mathematical POV it's a [[Monoid]]

### Properties and definitions
The alphabet is denoted by the letter $\Sigma$ and any string is built using following rules:
1. $\epsilon$ is an empty string (leere Zeichenkette / Leerwort) in $\Sigma$
2. If $x, a \in \Sigma$ then $xa \in \Sigma$

#### Lengths
The length of a string $x$ is:
$$
|x| = 
\begin{cases}
0, \text{ falls } x = \epsilon \\
n, \text{ falls } x = a_{1} a_{2} \dots a_{n}, n > 0
\end{cases}
$$
All strings of length $k$ can be expressed as $\Sigma^{k}$. And $\Sigma^{0} = \{ \epsilon \}$
All sets of all lengths (any word, essentially) over $\Sigma$ are expressed as:
$$
\Sigma^{*} = \bigcup_{k=0}^{\infty}\Sigma^{k}
$$
Any **language** $L$ can be expressed as $L \subseteq \Sigma^{*}$
And all sets of lengths over $\Sigma$ **sans** $\Sigma^{0}$ is expressed as:
$$
\Sigma^{+} = \bigcup_{k=1}^{\infty} \Sigma^{k} 
$$In other words:
$$
\Sigma^{*} = \Sigma^{+} \cup \{ \epsilon \}  
$$

### Concatenation (Verkettung)
The neutral element in strings is the $\epsilon$ not changing the concatenation: $x\epsilon = \epsilon x = x$
It's also associative: $\forall x, y, z \in \Sigma^{*}: x(yz) = (xy)z$

### Prefix, suffix and Teilwort
It's a bit weird but both the prefix and the suffix are kind of the same:
$$
\begin{align}
 & \text{Every word } x = a_{1}\dots a_{k}, \ (1\leq k \leq m) \text{ is a "Prefix" of } x \\
  & \text{Every word } x = a_{k}\dots a_{m}, \ (1 \leq k \leq m) \text{ is a "Suffix" of } x
\end{align}
$$
A Teilwort is literally just a part of a word. All of them could be "true" versions of themselves if they aren't wholly equal to words themselves (i.e. "pre-" in "prefix" is a true prefix since "pre-" isn't the whole word)