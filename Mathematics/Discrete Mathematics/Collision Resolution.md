---
tags:
  - math/discrete
  - math/computer-science
updated: 2026-03-26
created: 2026-03-26
---
Here and down $p$ will be a prime number. As to why collisions happen in the first place, refer to [[Mapping]]

### Open addressing
This approach is based on finding existing slots
#### Linear Probing
The simplest solution of them all. If there's a collision, just look $[\text{current place}]+ 1$ until an empty place is found. Strictly speaking it's defined as:
$$
s(k) = (h(k) + i) \text{ mod } p, \ i=1, \dots, p-1
$$
The first bad thing is that you can't delete the element after that without risking breaking the search so you have to manually mark it as "deleted" or something else. The second bad thing is that using this technique the data tends to cluster around one place which isn't that good when we're talking about hash function. To overcome these problems, use the next technique

#### Quadratic probing
This removes the seconds problem of clustering by spreading the search exponentially:
$$
s(k) = (h(k) ± i^2) \text{ mod } p, \ i=1, \dots, (p - 1) / 2
$$
The constraint $(p - 1) / 2$ is needed because any number nigher than that will be bigger than $p$ and the table would wrap-around. A good question is whether the such a method goes over all possible values. And the answer is yes! It does! Even if you don't start from $h(k) = 0$! This is due to a weird property of prime numbers:
$$
\begin{align}
& \text{For } p \equiv 3 \text{ mod } 4\text{:} \\
& \{±i^{2} \text{ mod } p, i = 1, \dots, (p - 1) / 2\} = \{1, 2, 3, \dots, p - 1\}
\end{align}
$$
Why that happens, I'm not exactly sure

#### Double hashing
Solves clustering by having an incremental step unique to the hash:
$$
h(k, i) = (h_{1}(k) + i \cdot h_{2}(k)) \text{ mod } m
$$
Where:
- $m$ is the table size
- $h_{1}(k)$ is the initial value
- $h_{2}(k)$ is the "step"
- $i$ is a probing value (i.e. $\{1, 2, 3, \dots\}$)
Gives a very good avoidance of clustering but is pretty complicated especially by a few other restrictions and recommendations. $h_{2}(k) \neq 0$ has to hold. As a nice option $m$ should be a prime number and $h_{2}(k)$'s way of producing values should be tied to $m$

### Separate Chaining
Instead of storing everything in one table this approach goes about solving the problem by simply "chaining" one more value to the same hash (making sure you can still separate them, of course)

Others include Bucket hashing, Coalesced hashing, Cuckoo hashing, Robin Hood hashing and, albeit not a resolution method directly, Rehashing which I'll def add later bc this is cool topic as hell