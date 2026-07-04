---
tags:
  - tba-place
---
> Clients shouldn't be forced to depend on methods they don't use

Kind of reminds me of [[L - Liskov Substitution Principle (LSP)]] but concerning interfaces. They also shouldn't be present and implemented[^1]  just bc the parent had it

---

### ❌ Bad Example
```pseudo
interface Worker
	work()
	eat()
	sleep()

class Robot implements Worker
	work()
	eat()  // Has to implement but is meaningless
	sleep()  // Has to implement but is meaningless
```

### ✅ Fixed Version
This mixes a lot of things. Let interfaces do that what they need
```pseudo
interface Workable
	work()

interface Eatable
	eat()

interface Sleepable
	sleep()

class Robot implements Workable  // Uses that which is needed
```

[^1]: Shout out to [[Realization (OOP)]]
