---
tags:
  - math/statistics
updated: 2026-03-31
"created ": 2026-03-31
created: 2026-03-31
---
### Discrete
A discrete series (дискретный ряд) shows data bound to specific values. For example, a table showing how many farms watered their plant one, two, there, etc. times:

| № of waterings | № of farms |
| :------------: | :--------: |
|       1        |     3      |
|       2        |     7      |
|       3        |     4      |
So this aggregates and binds the data to a specific, discrete, value

### Ranked
Ranked series (ранжированных ряд) shows data in ascending or descending order

### Interval
Interval series (интервальный ряд) is almost the same as discrete series but instead of binding data to a specific number it maps it to a range. An example would be a "How old are you?" question in forms:
- under 18
- 18-25
- 25-45
- etc.

To build the intervals adequately for "medium" sized sets, one can use the [[Sturges' formula]] and by getting the range and dividing it by the number of groups get the appropriate interval length:
$$
i = \frac{x_{max} - x_{min}}{m}
$$

How to count the [[Mean]], [[Median]] and [[Mode]] for these sets, look into the corresponding notes