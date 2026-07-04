---
tags:
  - cs/c
updated: 2026-05-31
created: 2026-05-26
---
A very interesting (wrong) use-case is the following:
```cpp
#include <iostream>
#include <string>
#include <string_view>

std::string getName() {
	std::string s { "Name" };
	return s;
}

int main() {
	std::string_view name { getName() };
	std::cout << name << "\n";  // Will result in UB
}
```

This is due to the fact that `string_view` creates a view of an object, skipping the initialization. And since the return value of `getName()` will get destroyed if not put to use (viewing it doesn't count) `string_view` can't be used on that

Same goes for:
```cpp
#include <string>
#include <iostream>
#include <string_view>

int main() {
	std::string_view s { "Name"s };
	std::cout << s << "\n";  // UB bc "Name"s is a std::string
}
```

Generally, initializing `string_view` with string is a bad idea since changing string-object will result in UB:
```cpp

#include <string>
#include <iostream>
#include <string_view>

int main() {
	std::string s { "Name" };
	std::string_view name_sv { s };

	std::cout << name_sv << "\n";  // Prints "Name"

	s = "Hello!";

	std::cout << name_sv << "\n";  // UB since `s` was changed
}
```

> [!tip] One subtlety
> Changing the string in a big way will cause UB however if you just reassign (e.g. `s[0] = 'j'`) it's all right. Generally speaking, `string_view` should point to the same mem address if changes happen within it, it's ok

> [!danger]
> `string_view` strings are not guaranteed to be null-terminated. As such avoid writing code that relies on null-terminated-ness (however `string_view` does keep the length of the string to look up)