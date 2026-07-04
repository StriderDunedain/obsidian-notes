---
tags:
  - math/probability
  - math/statistics
updated: 2026-05-02
created: 2025-11-17
---
> [!summary]
> Answers: "Can we make [[Mean Absolute Deviation]] even more useful?"

Variance, дисперсия на русском, measures the same stuff as the MAD but uses a square since it's a lot more useful and fits a lot nicer in formulas:
$$\sigma^2 = \frac{\sum (x_{i} - \overline{x})^{2}}{N}$$
The square is for convenience:
- Is differentiable
- Has the identity: $e(x^2) = e(x)^{2}$
- Some formulas work better for squares

Another version of the formula is:
$$
\sigma^{2} = \frac{\sum x_{i}^{2}}{n} - \overline{x}^{2}
$$

However, the power makes the units of measurements different, that's why we have [[Standard Deviation]]

The addition of variances is the same as described in [[Volume of Variation]]