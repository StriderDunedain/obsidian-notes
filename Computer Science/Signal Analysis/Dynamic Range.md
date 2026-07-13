---
tags:
  - cs/signal-analysis
updated: 2026-07-11
created: 2026-07-11
---
> [!danger] Warning
> Not to be confused with [[Signal-to-Noise Ratio]]

The dynamic range is a ration between the largest and the smallest signal's [[Quantization]] that can be represented without significant distortion. Increasing the bit depth - i.e. the precision - increases the number of quantization levels and therefore the dynamic range.

For a $b$-bit quantizer, the rule of thumb is that it should have its dynamic range at about $6.02b$ dB, which is why:
- 8-bit audio has a dynamic range of about 48 dB
- 16-bit of about 69 dB
- 24-bit of 144 dB

### Why $6.02b$ dB?
That's an easy question, actually. Imagine the signal as voltage jumping up and down from $-V$ to $+V$. If $q$ represents a quantized integer between $-2^{n - 1} \leq q \leq 2^{n - 1} - 1$, then we can make a map of the quantization to maximum quantized amplitude that maps $q$ to a value $v(q)$:
$$
v(q) = V \cdot \left( \frac{q}{2^{n - 1} } \right)
$$
This is, ofc, a lossy process but oh well, can't be perfect (yes, $2^{n - 1} - 1$ is *technically* the correct upper value but for big quantizers is negligible)

> #tba Research what is acceptable and why it's acceptable

Since intensity is proportional to the square of pressure (and therefore of voltage)[^1] this means that (taking the logarithm bc of the decibels):
$$
R_{\text{dB}} = 10 \cdot \log_{10}\left( \frac{v_{+}}{v_{-}} \right)^{2} 
$$
Now, calculating the minimum amplitude:
$$
v_{-} = v(1) = V \cdot \left( \frac{1}{2^{n - 1} } \right)
$$
And the maximum amplitude:
$$
v_{+} = v(2^{n - 1}) = V \cdot \left( \frac{2^{n - 1}}{2^{n - 1} } \right)
$$
So the ratio becomes
$$
\frac{v_{+}}{v_{-}} = 2^{n - 1} 
$$
Plugging that in the formula above we get
$$
R_{\text{dB}} = 20 \cdot \log_{10}2^{b - 1} = 20 \cdot (n - 1) \cdot \log_{10}2 \approx (n - 1) \cdot 6.02\text{ dB}
$$


> [!note]
> Increasing the [[Sampling rate]] allows higher frequencies to be represented, whereas increasing bit depth increases the dynamic range by allowing finer distinctions between amplitudes

[^1]: Mentioned in [[Basic Concepts in Signal Analysis]]
