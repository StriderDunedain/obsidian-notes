---
tags:
  - math/statistics
updated: 2026-03-31
created: 2026-03-31
---
> [!summary]
> Answers: "What's the most common element?"

#### Mode | Discrete and Ranged series
The mode is just the element that has the most frequencies / has the most occurrence

#### Mode | Interval series
This is such a monster (trying to find the interval with the most frequencies):
$$
m = L + \left( \frac{f_{m} - f_{prev}}{(f_{m} - f_{prev}) + (f_{m} - f_{next})} \right) \cdot h
$$
Where:
- $L$ is the lower border of the interval
- $f_{m}$ is the max frequency of the modal interval
- $f_{prev}$ and $f_{next}$ are the frequencies of the previous and the next intervals
- $h$ is the length of the modal interval

First of all. one has to find the interval where the cumulative sum of frequencies is $\geq N/2$. This is the *modal interval* – the interval where the mode is located

That's how you find it using the graphical method:
![[Pasted image 20260331184108.png]]
