---
tags:
  - cs/c
updated: 2026-05-26
created: 2026-05-26
---
Variable Length Array is an array whose size is determined at runtime instead of compile time:
```c
int n;
scanf("%d", &n);

int arr[n];  // VLA
```
Introduced to C in C99 and heavily discouraged in C++ though still available (ofc...)