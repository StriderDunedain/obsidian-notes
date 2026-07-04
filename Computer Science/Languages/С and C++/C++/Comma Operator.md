---
tags:
  - cs/c
updated: 2026-05-27
created: 2026-05-27
---
These will produce somewhat unexpected results:
```cpp
#include <iostream>

int main() {
    int x{ 5 };
    int y{ 7 };

    std::cout << (++x, ++y) << "\n";  // Prints "8"
}
```

And:..
```cpp
#include <iostream>

int main() {
	constexpr int x{ 5 };
	constexpr int y{ 7 };

	int z { (x, y) };

	std::cout << z << "\n";  // Prints "7"
}
```

This is the same in C (hi to all 42 projects and 25 line function limit)