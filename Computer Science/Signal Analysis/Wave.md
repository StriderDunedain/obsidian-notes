---
tags:
  - cs/signal-analysis
updated: 2026-07-08
created: 2026-07-08
---
Any wave can be expressed using the following standardized form
$$
x(t) = A \cdot \cos(2\pi \cdot f \cdot t + \phi)
$$
Where:
- $A$ is the amplitude of the wave; how high it rises / falls from 0
- $f$ is the wave's frequency; how many cycles it completes a second
- $\phi$ is the phase offset; how far before / after is the waves being offset by compared to starting at 0, shifts the wave to the left or the right

### Symmetry and anti-symmetry
The cosine has a horizontal symmetry: $\cos(\theta) = \cos(-\theta)$ (sometimes called an *even function*). Geometrically, these are counter-clockwise and clockwise rotations respectively. This is a very important property that explains a ton in [[Nyquist-Shannon Sampling Theorem]]

The sine function has a horizontal anti-symmetry: $\sin(-\theta) = \sin(\theta)$. Geometrically corresponds to "flipping the orientation"[^1]:
![[sine_horizontal_anti_symmetry.png]]

[^1]: Reminds me of some morphism. [[Enantiomorph]]? Something about [[Chirality]], too and the adding of new dimension in order to make such a flip. Needs research #tba
