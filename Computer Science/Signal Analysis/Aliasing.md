---
tags:
  - cs/signal-analysis
updated: 2026-07-08
created: 2026-07-08
---
Aliasing describes a situation where two different continuous-time signals produce the same discrete-time samples after sampling[^1] and it becomes impossible to determine which is which (as well as the frequency of the original wave(s)). It occurs because sampling only observes the signal at discrete instants, allowing different frequencies to coincide at those sampling points. A good visualization of that is at the end of this [segment](https://brianmcfee.net/dstbook-site/content/ch02-sampling/Aliasing.html#what-is-aliasing). A boundary that determines when aliasing starts to happen is described in [[Nyquist-Shannon Sampling Theorem]]

### Strict definition
Strictly speaking, given a [[Sampling rate]] of $f_{s}$, two continuous-time frequencies $f$ and $f'$ are **aliases** of each other if for some $k \in \mathbb{Z}$
$$
f' = f + k \cdot f_{s}
$$
In other words, the two frequencies differ by an integer multiple of the sampling frequency. When sampled, frequencies $f$ and $f'$ will become the following discrete signals
$$
\begin{align}
x[n] = A \cdot \cos\left( 2\pi \cdot f \cdot \frac{n}{f_{s}} + \phi \right) \\
y[n] = A \cdot \cos\left( 2\pi \cdot f' \cdot \frac{n}{f_{s}} + \phi \right)
\end{align}
$$
And will produce identical results for all $n \in \mathbb{N}$ (bc of the periodic nature of [[Wave]]s)

The equations above are sometimes referred to as as *aliasing equations*

[^1]: More in [[Sampling rate]]
