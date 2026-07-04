---
tags:
  - math/statistics
updated: 2026-04-01
created: 2026-04-01
---
> [!summary]
> Answers: "How much total deviation is in the dataset?"

Also called "объем вариации", is the sum of squared deviations (is the numerator of [[Variance]]):
$$
\sum (x_{i} - \overline{x})^{2}
$$

### Types of variation
***
> [!faq] **Total variation**
> Measures the total deviation in the dataset

This tell you how spread the variation is but why it is spread as it is. This is also what you would use for your [[Standard Deviation]]:
$$
S_{total} = \sum (x_{i} - \overline{x})^2
$$

> [!faq] **Within-group variation**
> Measures how different are members of the same group from each other

This measures the scatter inside a group. If it's big then the scatter of elements is big, if small then the elements are close together:
$$
S_{within} = \sum_{i} \sum_{j} (x_{ij} - \overline{x}_{j})^{2}
$$
> [!faq] **Between-group variation**
> Measures how different are the groups from each other

The larger this variation is the more different are the groups
$$
S_{between} = \sum n_{j} (\overline{x}_{j} - \overline{x})^{2}
$$
Where: $n_{j}$ is the size of group $j$

**Note**: moreover, the total variation can be found by:
$$
S_{total} = S_{within} + S_{between}
$$

***
### What about variance?
The aforementioned three types of variation also exist as variance but are counted using the same formula:
$$
\sigma^{2}_{type} = \frac{S_{type}}{N}
$$
