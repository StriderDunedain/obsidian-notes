---
tags:
  - math/statistics
  - math/algorithm
updated: 2026-04-01
created: 2026-04-01
---
The $\chi^{2}$ test by Pearson (also called the goodness-of-fit test) is used to check whether the observed frequencies match the frequencies expected under a theoretical distribution.

The null hypothesis $H_{0}$ here is that the frequencies **are** close together

### Chi statistic
$$
\chi^{2} = \sum^{k}_{i=0} \frac{(O_{i} - E_{i})^{2}}{E_{i}}
$$
Where:
- $O_{i}$ is the observed frequency in category $i$
- $E_{i}$ is the expected frequency

The smaller the result, the more likely that $H_{0}$ (the [[Null Hypothesis]]) is true

#### Choosing the hypothesis
1. Compute the statistic
2. Choose a significance level $\alpha$
3. Look up the critical $\chi^{2}$ value from the distribution table with $df$
4. Decision:
$$
\begin{align}
& \chi^{2}_{calc} > \chi^{2}_{critical} \to \text{ reject } H_{0} \\
& \chi^{2}_{calc} \leq \chi^{2}_{critical} \to \text{ accept } H_{1}
\end{align}
$$

### Degree of freedom
$$
df = k - 1 - m
$$
Where:
- $k$ is the number of categories
- $m$ is the number of estimated parameters

Example: for a six-sided die with no estimated parameters, $df = 6 - 1 = 5$

### Example
Suppose we roll a six-sided die 60 times and observe frequencies:
$$
O=[8,12,9,11,10,10]
$$
Expected frequencies (fair die): $E=[10,10,10,10,10,10]$, $\chi^{2}$ = 1 and $df = 6 − 1 = 5$

Critical $\chi^{2}$ at $\alpha=0.05$ and $df=5 \approx 11.07$

Since $1 < 11.07$ the $H_{0}$ holds which mean that the die is consistent with being fair