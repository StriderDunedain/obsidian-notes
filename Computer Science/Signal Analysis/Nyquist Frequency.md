---
tags:
  - cs/signal-analysis
updated: 2026-07-11
created: 2026-07-11
---
The **Nyquist frequency** is the highest frequency that can be uniquely represented by a given [[Sampling rate]]. It is defined as

$$
f_N=\frac{f_s}{2},
$$

where $f_{s}$ is the sampling frequency

> [!important]
> Any frequency greater than the Nyquist frequency is indistinguishable from a lower frequency after sampling. This phenomenon is called [[Aliasing]].

### Why is it $f_{s} / 2$?
Sampling identifies frequencies that differ by integer multiples of the sampling frequency:

$$
f \equiv f+kf_s,\qquad k\in\mathbb Z.
$$

In other words, after sampling we can no longer distinguish frequencies belonging to the same equivalence class. Mathematically, the frequency space becomes

$$
\mathbb R/f_s\mathbb Z,
$$

which is analogous to [[Congruence Class|congruence class]] modulo $f_{s}$.

For real-valued signals, positive and negative frequencies represent the same oscillation[^1], so every frequency larger than
$$
\frac{f_s}{2}
$$

has an equivalent frequency below it.

Hence,

$$
\boxed{f_N=\frac{f_s}{2}}
$$

is the highest frequency that admits a unique representation.

### Example
If

$$
f_s=1000\text{ Hz},
$$

then

$$
f_N=500\text{ Hz}.
$$

A 700 Hz sinusoid will be sampled exactly like a 300 Hz sinusoid, so they cannot be distinguished from the samples alone.

[^1]: More in [[Cosine]]
