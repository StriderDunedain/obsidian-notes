---
tags:
  - moc
  - cs/signal-analysis
updated: 2026-07-08
created: 2026-07-07
---
### Notation & Conventions
- $x(t)$ denotes **continuous-time** signals, where $t \in \mathbb{R}$. Read as "signal $x$ at time $t$"
- $x[n]$ denotes **discrete-time** signals, where $n \in \mathbb{Z}$. Read as "the $n^{\text{th}}$ sample of signal $x$"
- When either $t$ or $n$ fall below zero, the output of signals is also zero (think of it as the signals are silent before the recording)
[[Basic Concepts in Signal Analysis]]

There doesn't really exist any difference between signals and [[Wave]]s other than that the waves not only carry information but also propagate through space

Converting between sine and cosine ([proof](https://brianmcfee.net/dstbook-site/content/ch01-signals/Waves.html#converting-between-sine-and-cosine)):

$$
\begin{align}
\sin(\theta) = \cos\left( \frac{\pi}{2} - \theta \right) \\
\cos(\theta) = \sin\left( \frac{\pi}{2} - \theta \right)
\end{align}
$$

For the units of measurement:
- time will be measured in seconds
- frequency in cycles / second
- phase in radians

#tba Might be worthwhile read on [acoustics](https://brianmcfee.net/dstbook-site/content/references.html#id2)


### Sound propagation
There's a source emitting a signal $x_{s}$ and a microphone is placed 5 meters away, recording the signal $x_{m}$. If the speed of sound is $C$ then it will take $5 / C$ seconds to travel to the microphone. Put another way, by the time it reaches the microphone $t - 5 / C$ seconds will have passed so
$$
x_{m}(t) \approx x_{s}(t - D / C)
$$
