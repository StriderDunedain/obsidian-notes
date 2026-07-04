---
tags:
  - cs/c
updated: 2026-06-01
created: 2026-06-01
---
To avoid accidentally misusing the null statement (;) you can mimic Python's `pass` keyword using the [[Preprocessor]]:
```cpp
#define PASS

int main(char *str) {
	int len { 0 };
	
	while (str[len++])
		PASS;
}
```


An infinite for loop has the form of: `for (;;)` and they can also work on multiple variables:
```cpp
#include <iostream>

int main() {
	for (int x{}, y{ 10 }; x < 10; --y, ++x)
		std::cout << x << " " << y << "\n";
}
```