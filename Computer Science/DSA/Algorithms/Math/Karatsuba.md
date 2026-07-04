---
tags:
  - cs/algo
  - tba
  - tba-place
---
This algorithm was discovered by a soviet mathematician [[Анатолий Карацуба]] in #history/1960 disproving - much to [[Колмогоров]]'s surprise - the assumption that any multiplication of $n$ digit-numbers has to take $n^2$ operations. The former managed to take it down to $O(n^{\log_{2} 3})$ operations (roughly $n^{1,585}$ operations) by substituting some multiplications with addition

### The algorithm
Suppose two numbers:
$$
	\begin{align}
	x = a \cdot B^m + b \\
	y = c \cdot B^m + d
	\end{align}
$$
Where:
- $B$ is the base (Python uses $2^{30}$)

Naively:
$$
	xy = acB^{2m} + (ad + bc)B^m + bd
$$
And Karatsuba observes:
$$
	(a + b)(c + d) = ac + ad + bc + bd
$$
So:
$$
	ad + bc = (a + b)(c + d) - ac - bd
$$

#### `n = 2` numbers' case
A shorthand for quicker multiplication of two two-digit numbers for daily life:
$$
	ad \cdot bc = (a + b)(c + d) - ac - bd
$$
---
# Function growth comparison
```desmos-graph
left=-5; right=30; bottom=-5; top=60
---
\std(x) = x^2 \{x \geq 0\}|#c74440
\kar(x) = x^{\log_{2}(3)}|#2d70b3

(5, \std(5))|#666666
(5, \kar(5))|#666666
```

#tba Consider replacing with interactive graphs
#tba Learn to solve [[Transcendental Equation]]s to get the acceleration diff