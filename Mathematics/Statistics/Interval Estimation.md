---
tags:
  - math/statistics
updated: 2026-04-01
created: 2026-04-01
---
Called интервальная оценка in Russian, this tries to estimate the unknown parameters of the population using the data available in a sample (for bias look to [[Unbiased Estimator of Variance]]) by introducing an error margin:
$$
\overline{x} \pm z \cdot \frac{s}{\sqrt{n}}
$$
Where:
- $z$ is the confidence level, usually a percentage
- $s$ is the sample [[Standard Deviation]]
- $n$ is the sample size

The second term is actually just the [[Standard Error of the Mean]]
***
Wonder if I could use it in [[IEEE 754]] in the part about the machine epsilon... I have to review it later