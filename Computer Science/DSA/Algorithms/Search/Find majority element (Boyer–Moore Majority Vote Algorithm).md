---
leetcode: https://leetcode.com/problems/majority-element/description/?envType=study-plan-v2&envId=top-interview-150
space complexity: O(1)
complexity: O(n)
learned: ✅
tags:
  - cs/algo
updated: 2026-01-04
created: 2025-11-02
---
Introduced first in #history/1981 by Moore and Boyer, this is the first [[Streaming Algorithm]]. The [[Misra–Gries Heavy Hitters Algorithm]] and the [[Misra–Gries Summary]] are generalizations of this algorithm
```python
def majorityElement(nums: list[int]) -> int:
	max_, curr = 0, 0
	for x in nums:
		if max_ == 0:
			curr = x
		if curr == x:
			max_ += 1
		else:
			max_ -= 1
	return curr

print(majorityElement([1, 2, 3, 4]))
```
