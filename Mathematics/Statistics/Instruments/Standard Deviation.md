---
tags:
  - math/probability
  - math/statistics
updated: 2026-04-01
created: 2025-11-17
---
> [!summary]
> Answers: "How 'sparse' are the elements in the dataset?"

Standard Deviation (или среднеквадратическое отклонение) is the measure of how far apart are the elements in a set, effectively how "sparse" or "dense" is the distance is between the numbers. Calculated as the **square root** of [[Variance]] to get the original measurements back:
$$\sigma = \sqrt{\frac{\sum (x_{i} - \overline{x})^{2}}{N}}$$

### Decision Theory
With respect to business and [[Decision Theory]], the formula gets a flair of weighted sum, the weight being the probability of something happening. This version calculates how far apart the probabilities are with respect to how valuable they are to prevent a glass cannon situation (like winning a million with a 1% that would shine as the best option if using the [[Expected value, Мат ожидание or µ-Criterion]])
$$\sigma(A_i) = \sqrt{ \sum_{k=1}^K p_k \cdot (e_{ik} - \mu(A_i))^2 }$$
$$
\begin{align*}
& A_{i}: \text{ the Alternative, the Action} \\
& p_{k}: \text{ the Probability of } A_{i} \text{ happening} \\
& e_{ik}: \text{ the table-y representation for how valuable an } A_{i} \text{ is}\\
&  \mu(A_{i}): \text{ the function for weighing the µ-Criterion for } A_{i} \\
\end{align*}
$$

### SD vs MAD
SD is essentially MAD but, through the use of [[Variance]], it becomes a lot easier to handle