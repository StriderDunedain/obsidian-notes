---
tags:
  - math/matrix
  - tba
updated: 2026-05-24
created: 2026-05-24
---
These are very important concepts

### Synthesis
Take a [[Matrix]] $A$ and a vector $x$:
$$
A = 
\left[
\begin{matrix}
1 & 2 \\
3 & 4
\end{matrix}
\right],
\quad 
x =
\left[\begin{matrix} a \\ b \end{matrix}\right]
$$
Then synthesis would be:
$$
Ax =
a \left[ \begin{matrix} 1 \\ 3 \end{matrix} \right]
+
b \left[ \begin{matrix} 2 \\ 4 \end{matrix} \right]
$$
So synthesis tells you how much of which vector to combine to construct the output. It goes along the columns. This is the [[Linear Map]] (or better said, combination) of columns

#tba This kinda reminds me of [[CNF and DNF]] where it'd make sense to represent an equation as a matrix (that's prob already being done but nice observation)

### Analysis
For the same matrix $A$ and vector $x$:
$$
Ax = \left[ \begin{matrix}
1 & 2 \\
3 & 4
\end{matrix} \right]
\left[ \begin{matrix}
a \\
b
\end{matrix} \right]
=
\left[ \begin{matrix}
1a + 2b \\
3a + 4b
\end{matrix} \right]
$$
This is analysis: how much output in coordinate one, two, etc. It goes along the rows. That's the [[Covector]]s