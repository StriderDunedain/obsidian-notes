---
tags:
  - cs/signal-analysis
updated: 2026-07-08
created: 2026-07-08
---
To first understand bandwidth, you have to know one property that any continuous-time signal can be, under mild conditions, be represented as a weighted sum of waves:
$$
\begin{align}
& x(t) = A_{1} \cdot \cos(2\pi \cdot f_{1} \cdot t + \phi_{1}) + \\
& \quad \quad \quad A_{2} \cdot \cos(2 \pi  \cdot f_{2} \cdot t + \phi_{2}) + \\
& \quad  \quad \quad A_{3} \cdot \cos(2\pi \cdot f_{3} \cdot t + \phi_{3}) + \dots
\end{align}
$$
Same can be said for discrete-time signals (albeit using [[Sampling rate]] instead of time)

A signal $x(t)$ is **band-limited** if it can be expressed by a weighted sum of pure sinusoids whose frequencies lie between some minimum frequency $f_{-}$ and some maximum frequency $f_{+} \geq f_{-}$ which makes up the  band of frequencies
$$
f_{+} \text{ to } f_{-}
$$
This is known as the **bandwidth** of the signal. Another way of saying this is that frequencies outside of the bandwidth have no effect on the signal (which is the basis for the [[Nyquist-Shannon Sampling Theorem]])

### Band-limiting in practice
The Nyquist-Shannon theorem tells us *how* to choose the sampling rate provided we know the band limits of the signal(s) we'd like to sample. But how do we ensure that $x(t)$ is actually band-limited? In a computer this is typically done using analog-to-digital converters ([[ADC]]s) that remove anything above $f_{+}$ prior to sampling