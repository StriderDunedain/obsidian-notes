---
tags:
  - cs/c
updated: 2026-05-26
created: 2026-05-26
---
The compiler may transform the program any way it likes as long as the output is the same. That includes:
```cpp
int x;
x = 5;
// Turns to...
int x = 5;
```
And a lot of other cases. One notable exception to that is the `volatile` [[Type Qualifier]] 