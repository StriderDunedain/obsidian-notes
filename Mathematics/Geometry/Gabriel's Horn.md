---
tags:
  - math/geometry
updated: 2026-05-18
created: 2026-05-15
---
<img src="Pasted image 20260515003221.png" width="300" style="display:block; margin:auto;">
Gabriel's Horn (also called Torricelli's Trumpet) is a figure that has infinite surface area but finite volume. It's created by taking $f(x) = \frac{1}{x}$ with $x \geq 1$ and rotating it

It's volume is:
$$
	V = \pi \int_{1}^{a}\left( \frac{1}{x} \right)^{2}dx = \pi\left( a - \frac{1}{a} \right) 
$$
And the surface area:
$$
	A = 2\pi \int_{1}^{a} \frac{1}{x} \sqrt{ 1 + \left( - \frac{1}{x^{2} } \right)^{2}  } dx = 2\pi \ln a
$$


#tba Kinda reminds me of [[Zeno's Paradoxes]] and [[The Continuum Hypothesis]], study further

#tba FdF project in 42 CC in C I think could prove useful in drawing the horn programmatically 