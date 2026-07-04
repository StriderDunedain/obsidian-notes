---
tags:
  - cs/c
updated: 2026-05-31
created: 2026-05-19
---
Oh how I love cpp. This bulky machinery fixing already complicated things, trying to be not just good but great at literally everything at the same time by over-backward-compatibiliting its code. So without further ado, here are some weird things in cpp that are now not quite obsolete but do look weird:
1. `constexpr`
	This declaration specifier comes from the ancient times when compilers were dumber and couldn't figure out what could be determined already at compile time rather than runtime. It doesn't enforce[^1] the statement to be evaluated at compile time, just says that it will be if it's possible (with the exception for variable initialization, that has to be able to run). Again, compilers have become a lot smarter and now this isn't that useful

> [!warning] `constexpr` and `inline`[^2]
> `constexpr` *function* are implicitly *inline* but variables *are not*

[^1]: `consteval`, on the other hand, is stricter and enforces the statement to be evaluated regardless at compile time

[^2]: [[Storage Class Specifiers]]
