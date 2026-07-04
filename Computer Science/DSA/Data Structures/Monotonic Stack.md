---
tags:
  - cs/ds
---
Much like a run-o-the-mill [[Stack]] this adds just one feature: the values are either ascending or descending. So whenever the new value violates the order, elements are popped until the order is restored (this really is the Stalin Sort)

This is useful in problems like next greater / smaller element, largest bar on a histogram, stock span, daily temp, etc. Runs in about `O(n)` time