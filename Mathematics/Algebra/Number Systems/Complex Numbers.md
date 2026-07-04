---
tags:
  - math/complex-number
updated: 2026-04-05
created: 2026-03-29
---
An element $z \in \mathbb{C}$ can be expressed as $z = a + b \cdot i$, where $a, b \in \mathbb{R}$. Germans also call $i$ the imaginäre Einheit

### Definition
$\mathbb{C} := \mathbb{R}^{2} = \{(x,y) \ | \ x, y \in \mathbb{R}\}$ with $(a, b), \ (c, d)$ having the following properties (built from $\mathbb{R}$):
$$
\begin{align}
& (a, b) + (c, d) := (a + c, b + d) \\
& (a, b) + (c, d) := (ac - db, bc + ad)
\end{align}
$$


### Structure of a complex number
In $z = a + bi$, $a$ is called the *real part* (Realteil) and $b$ is called the *imaginary part* (Imaginärteil) and both are denoted as follows:
$$
\begin{align}
& a = \mathrm{Re}(z) \text{, or } \Re(z) \\
& b = \mathrm{Im}(z) \text{, or } \Im(z)
\end{align}
$$

### Graphical representation
The number $z$ can be expressed on a graph as follows:
![[Pasted image 20260329151137.png]]
The *(complex) conjugate* of $z$ is defined as $\overline{z} = a - b \cdot i$ (more in [[Complex Conjugate Root Theorem]])

#### Vectorified
The magnitude of a complex number $z$ is defined as
$$
|z| := \sqrt{a^2 + b^2}
$$
Geometrically this means the length of the vector $(a, b)$ in the [[Argand Plane]] (more on vectors' length in [[General on Vectors]]). Interestingly, squaring the magnitude is the same as multiplying the number by its conjugate:
$$
|z|^2 = z \cdot \overline{z}
$$
#### Some other operations
$$
\begin{align}
& |z_{1} + z_{2}| \leq |z_{1}| + |z_{2}|, \\
& |z_{1}z_{2}| = |z_{1}||z_{2}|, \\
& \overline{z_{1} + z_{2}} = \overline{z_{1}} + \overline{z_{2}}, \\
& \overline{z_{1} \cdot z_{2}} = \overline{z_{1}} \cdot \overline{z_{2}}
\end{align}
$$

#### Interesting trivia
$(\mathbb{C}, +, \cdot)$ can be shown to be a [[Field]] but it won't be an ordered one (more in [[Set Relations]]) since there's no $\leq$ relation on numbers possible (bc of $i$ being squared giving you negative number or smth)