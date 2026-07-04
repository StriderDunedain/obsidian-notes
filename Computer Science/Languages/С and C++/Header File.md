---
tags:
  - cs/c
updated: 2026-06-01
created: 2026-05-02
---
### Include guard
That's this statement in a header file:
```
#ifndef HEADER_H
#define HEADER_H
...
#endif
```
This is used to avoid redefinition errors. Common rule is to make it the same as the header file's name: header.h -> HEADER_H, libft.h -> LIBFT_H. This isn't used anywhere else. If it throws an error, try putting a space after '#'

Something called `#pragma once`[^1] avoids this entirely. It's tells the compiler to keep track of this file and link it only once. Relies on the compiler's ability to do that instead of the preprocessor. However, not a part of the standard C but practically universal

It can also be used as comment substitution:
```cpp
#if 0
...
#endif
```
In this block, nothing will be executed

#tba Is this only C++ or C too?
#tba Learn more about header files

### Collisions & Resolutions
Honestly, it's a fucking MESS in C++. So I'm not even going to write anything about that, just refer to [section 7 of this tutorial](https://www.learncpp.com/) for closer info. The only thing worth noting is the `constexpr` and `inline` described in [[constexpr]] and [[Storage Class Specifiers]]

[^1]: `pragma` itself is not guaranteed to exist or have the same commands, however with `once` it's fairly ubiquitous already (works on a single [[Translation Unit]])
