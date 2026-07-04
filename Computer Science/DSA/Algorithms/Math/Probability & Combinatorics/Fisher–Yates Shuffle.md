---
tags:
  - cs/algo
---
Also called the Knuth shuffle, this is a very important algorithm in CS for generating a uniformly random [[Permutation]] of a finite list. Created by Ronald Fisher[^1] and Frank Yates[^2] in #history/1938 and later popularized in CS by [[Donald Knuth]]
### Working principle
The idea behind it is pretty simple. For a list of of $n$ elements there exist $n!$ permutations. This algorithm goes from $n$ to $0$ and, choosing a random value from $0$ to $i$, swaps the last element with the element on index $i$, making the probability that the number is chosen equal to $1 \ / \ (i + 1)$ which is the definition of a permutation:
$$
P = \frac{1}{n} \times \frac{1}{n-1} \times \frac{1}{n-2} \times \dots \times \frac{1}{1}
$$
From the POV of [[Asymptotic Notation]] it's time complexity is $O(n)$ and space complexity is $O(1)$
### Algorithm
Here's an implementation in python:
```python
import random

def fisher_yates_shuffle(arr):
	n = len(arr)
	for i in range(n - 1, 0, -1):
		j = random.randint(0, n)
		arr[i], arr[j] = arr[j], arr[i]
	return arr
```

[^1]: #tba Make a separate note later. His notable works include The Design of Experiments, The Genetical Theory of Natural Selection. He's like the most brilliant statistician ever so I should give him a read

[^2]: #tba also make another note. Books are Sampling Methods for Censuses and Surveys
