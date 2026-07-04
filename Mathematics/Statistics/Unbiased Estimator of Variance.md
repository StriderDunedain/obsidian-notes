---
tags:
  - math/statistics
updated: 2026-04-01
created: 2026-04-01
---
Called in Russian Несмещённая оценка дисперсии, this tries to estimate the *population* [[Variance]] with only its *sample*

Unlike the variance formula, we can't really use the [[Mean]] by itself since that would be a bias, so we need to introduce the **Bessel's correction**:
$$
s^{2} = \frac{1}{n - 1} \sum (x_{i} - \overline{x})^{2}
$$

**Note**: the estimate is unbiased is $E(s^{2}) = \sigma^{2}$