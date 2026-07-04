---
tags:
  - tba-place
---
> Instead of creating dependencies, pass them directly

Basically, [[Structs]]' usage. We don't create one every time we need it - we pass it by address and re-use the same thing. That's the dependency being injected

---
Here's an example
```pseudo
logger = Logger()  // bad, re-creating every time

f(logger)  // good, gets re-used
```