---
tags:
  - math/statistics
updated: 2026-04-01
created: 2026-03-31
---
> [!summary]
> Answers: "What's the middle element?"

#### Median | Discrete series
1. Find the median by normal means
2. Judging by cumulative frequencies, find the answer!

For example, for the following table the answer is $4$ since the median ($\frac{170}{2} = 85$):

| $x_{i}$ | $f_{i}$ | $S_{f}$ |
| :-----: | :-----: | :-----: |
|    1    |   10    |   10    |
|    2    |   11    |   21    |
|    3    |   29    |   50    |
|  **4**  |   43    | **93**  |
|    5    |   34    |   127   |
|    6    |   23    |   150   |
|    7    |   20    |   170   |

#### Median | Ranged series
Found using a normal median definition

#### Median | Interval series
The median is found using this monstrosity:
$$
m = L + \left( \frac{ \frac{N}{2} - S_{prev} }{f_{m}} \right) \cdot h
$$
Where:
- $N$ is the total number of observations
- $L$ is the lower border of the modal interval
- $h$ the length of the modal interval
- $f_{m}$ is the frequency of the modal interval
- $S_{prev}$ is the cumulative sum of frequencies

First of all. one has to find the interval where the cumulative sum of frequencies is $\geq N/2$. This is the *modal interval* – the interval where the mode is located