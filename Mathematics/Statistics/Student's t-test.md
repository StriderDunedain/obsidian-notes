---
tags:
  - math/statistics
updated: 2026-05-02
created: 2026-04-01
"created ": 2026-04-01
---
> [!warning]
> UNFINISHED NOTE

A statistical test to make inference about a population [[Mean]] ($\mu$), especially when the population's [[Standard Deviation]] is unknown and the sample size is too small ($n < 30$, the limit for the [[Central Limit Theorem]]). Use cases would be anything from comparison average scores of two classes to testing drug's effectiveness against a placebo.

The basic idea is to compare the signal (difference) to noise (uncertainty) and answer the question: "Is this too extreme to be random?" 

There are a lot – and I mean a lot – of [[t-test]]s but here's the Student's t-test

#### One-sample

$$
t = \frac{\overline{x} - \mu_{0}}{s / \sqrt{ n }}
$$
Where:
- $\overline{x}$ is the sample mean
- $\mu_{0}$ is the hypothesized population mean
- $s$ is the sample SD
- $n$ is the length of the sample

The numerator is what is being tested and the denominator is the noise so big t indicates a strong signal and vice versa 

### One-tailed
I haven't got time for this now...

### Two-tailed
This test checks whether the sample mean is *significantly* different in either direction from the hypothesized mean:
$$
\begin{align}
& H_{0} : \mu = \mu_{0} \\
& H_{1} : \mu \neq \mu_{0}
\end{align}
$$
Algorithm:
- Compute the t-statistic (above)
- Choose a significance level $\alpha$ (commonly $0.05$)
- Look up the critical value $t_{\alpha / 2}$​ from the t-distribution table with $n−1$ degrees of freedom
- Reject $H_{0}$ if $|t| > t_{\alpha / 2}$

Yeah, I've no idea what this means