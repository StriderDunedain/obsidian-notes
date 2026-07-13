---
tags:
  - cs/signal-analysis
updated: 2026-07-11
created: 2026-07-08
---
The **Nyquist–Shannon Sampling Theorem** states the condition under which a continuous, band-limited signal can be perfectly reconstructed from its discrete samples.

> [!abstract] Theorem
> If the highest frequency present in a signal is $B$, then
> $$
> f_s>2B
> $$
> is sufficient for perfect reconstruction.

Equivalently,

$$
B<f_N,
$$

where $f_{N}$ is the [[Nyquist frequency]].

If this condition is not met, [[Aliasing]] occurs and perfect reconstruction is impossible.