---
tags:
  - cs/c
updated: 2026-06-01
created: 2026-06-01
---
##### `[[fallthrough]]`
Since ofc switch statements don't have blocks without breaks / returns the code after a match in all other cases will be executed – this is called fallthrough. So to indicate intentional one, use the eponymous attribute:
```cpp
#include <iostream>

int main() {
	int x { 5 };
	switch (x) {
	case 5:
		std::cout << "5";
		[[fallthrough]];
	case 10:
		std::cout << "10";
	}
}
```