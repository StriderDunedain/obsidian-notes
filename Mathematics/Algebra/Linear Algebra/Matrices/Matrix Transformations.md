---
tags:
  - math/matrix
  - math/linear-algebra
updated: 2026-04-20
created: 2026-04-10
---
#### Scaling (Streckung)
In such matrices everything is simply stretched by a factor $k$:
$$
\begin{pmatrix} k \quad 0 \\ 0 \quad k \end{pmatrix}\begin{pmatrix} x_{1} \\ x_{2} \end{pmatrix} = \begin{pmatrix} k x_{1} \\ k x_{2} \end{pmatrix} = k \begin{pmatrix} x_{1} \\ x_{2} \end{pmatrix} = kx
$$

#### Shearing (Scherung)
A sideway-shift that keeps one direction fixed. The shape will look distorted and parallel lines will stay parallel

**Horizontal shear**: This is the left/right movement: $\begin{pmatrix} 1 \quad k \\ 0 \quad 1 \end{pmatrix}$
**Vertical shear**: This is the up/down movement: $\begin{pmatrix} 1 \quad 0 \\ k \quad 1 \end{pmatrix}$

#### Reflection (Spiegelung)
**Across the x-axis**: Flips vertically: $\begin{pmatrix} 1  \ \quad \ 0 \\ 0 \quad -1 \end{pmatrix}$
**Across the y-axis**: Flips horizontally: $\begin{pmatrix} -1 \quad 0 \\ 0 \quad 1 \end{pmatrix}$
**Across y = x**: Swaps coordinates: $\begin{pmatrix} 0 \quad 1 \\ 1 \quad 0 \end{pmatrix}$

#### Rotation (Drehung)
Yeah, basically just use [[Sine]] and [[Cosine]] to rotate it, it's pretty boring stuff