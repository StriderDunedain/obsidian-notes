---
tags:
  - cs/c
updated: 2026-05-03
created: 2026-05-03
---
They define how the variable can be used
- `const`: You can't modify the value. It's enforced although there are ways around it. Most if not all are either undefined behavior or crashes
> [!warning] `const char *p`
> Although a const pointer cannot be modified, `p` can still change, naturally. To disable even that, use something like `const char *const p`
- `volatile`: Used for values that might change unexpectedly, effectively tells the program to always read from memory, no cache
- `restrict`: Promises that this is the only way a [[Pointer]] can be accessed allowing compiler optimizations