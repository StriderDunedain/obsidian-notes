---
tags:
  - cs/c
updated: 2026-05-31
created: 2026-05-03
---
These specifiers define lifetime and visibility of variables and functions. Compare with [[Type Qualifier]]
- `static`: Used to keep the value between calls (for the entire runtime). Automatically sets them to `NULL`
- `extern`: Declares a variable that is defined somewhere else
- `auto`: A rare specifier
- `register`: Mostly obsolete, nowadays often gets ignored but it's intended to indicate that a variable will be written directly to the [[CPU]] register (dereferencing here, e.g., isn't guaranteed) which makes stuff faster (deprecated in C++17)

The following are a bit shaky on the actual term since they are also function specifiers as well as variable specifiers but I didn't wanna create a separate note

- `inline` (def 1, general): Suggests replacing the function call with just its body, allows for optimizations (a bit outdated since compilers are pretty smart)
-  `inline` (def 2, in C++): A function (and variables starting, reliably, from C++17) can have multiple *identical* definitions (but one declaration) across files (prevents header collisions in [[Translation Unit]]s)
- `extern`: The declaration is here and a *single* definition is somewhere else

### `extern` vs `inline`
For extern there can exist many declarations but only one definition per program is permitted and for inline it's a M2M connection: there can be as many declarations as you want and also as many definitions (as long as they're the same)