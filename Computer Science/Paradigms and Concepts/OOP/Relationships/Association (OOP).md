---
tags:
  - tba-place
---
This is a "know about" link. The structures *may* know something about each other but they are completely independent. Here's an example of `Teacher` knowing about `Student`s:
```python
class Teacher:
	students: list[Student]
```