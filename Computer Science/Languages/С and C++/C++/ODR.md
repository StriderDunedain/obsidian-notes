---
tags:
  - cs/c
updated: 2026-05-31
created: 2026-05-25
---
The "One Definition Rule". Uhhh, very stupid nonsense that could've been avoided or fixed (it's 2026 after all, come on). This is a set of rules for resolving header inclusions-collisions:
1. Put `inline`[^1] on every function in the header so that it doesn't potentially get relinked at some point
2. Put `extern`[^2] on every variable in the header for the same reason as `inline` (actually you can also use `inline` on variables)
3. Function prototypes have to be identical everywhere (duh...)
4. The include guard[^3] could potentially lead to a problem so refrain from using in context of changing types depending on context (like `double x` if THIS else `int x`)

This can all be resolved by simply writing code as usual and fixing module system for cpp (oh they actually made it in C++20 by introducing module, thank god)

[^1]: Look up `inline` (def 2) in [[Storage Class Specifiers]]

[^2]: More in [[Storage Class Specifiers]]

[^3]: Look up [[Header File]]
