---
tags:
  - cs/signal-analysis
updated: 2026-07-11
created: 2026-07-11
---
The **quantization** of a sampled signal is the process of mapping each sample to one of a finite amplitude levels. If each sample is represented using $b$ bits, then there are
$$
2^{b} 
$$
possible quantization levels

Quantization discretizes the **amplitude** (i.e. the y-axis) of a signal, whereas sampling discretizes its time (i.e. the x-axis). Here's a good [visualization of quantization](https://brianmcfee.net/dstbook-site/content/ch02-sampling/Quantization.html#the-effects-of-quantization). Since this is a tradeoff between perception and storage, there ofc exist interesting tricks and techniques, which is why:

#tba Explore perceptual coding and lossy audio compression