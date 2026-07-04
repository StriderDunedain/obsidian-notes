---
tags:
  - tba-place
---
Aggregation is a special kind of [[Association (OOP)]] where one object contains the other but the contained object can exist without the container. This is also called "weak ownership" (as opposed to [[Composition (OOP)]])
```python
class Team:
	players: list[Player]
```