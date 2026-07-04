---
tags:
  - cs/c
updated: 2026-05-26
created: 2026-05-03
---
They define how the variable can be used
- `const`: You can't modify the value. It's enforced although there are ways around it. Most if not all are either undefined behavior or crashes
> [!warning] `const char *p`
> Although a const pointer cannot be modified, `p` can still change, naturally. To disable even that, use something like `const char *const p`
- `volatile`: Used for values that might change unexpectedly, effectively tells the program to always read from memory, no cache and is used only in a handful of cases
- `restrict`: Promises that this is the only way a [[Pointer]] can be accessed allowing compiler optimizations

#### `volatile` example
Here's one of the corner cases to look out for:
```cpp
std::sig_atomic_t quitGame{ false };

void handle(int signal) {
	quitGame = true;
}

int main() {
	std::signal(SIGINT, handle);
	while (!quitGame) {
		// Run game
	}
	std::cout << "Game Over!\n";
	return 0;
}
```

> [!warning] Setup
> This only works for compiler `-o3` optimizations

Here the obvious way of ending the game with ctrl + C won't work because the compiler assumes that `quitGame` actually never sets to `true` and hence replaces this loop with an infinite one. Declaring `quitGame` volatile will prevent this behavior by telling the compiler to be more cautious since the variable may change in unexpected - for compiler - ways
#### More on `const`
An expression that *must* be evaluated at compile time is called the manifestly constant-evaluated expression (mostly used only in documentation). `const`-qualified expressions are subject to that rule