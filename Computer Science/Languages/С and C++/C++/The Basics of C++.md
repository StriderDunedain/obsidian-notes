---
tags:
  - cs/c
updated: 2026-05-27
created: 2025-11-08
---
### Operators
- *<<* is called "put to" (cout)
- *>>* is called "get from" (cin)
- *\** means "contents of"
- *&* means "address of" or "reference to" when used in a declaration where that would mean working with the value
- $::$ is called the *scope resolution operator*, the identifier with a namespace prefix is called the qualified name, i.e. cout in `std:.:cout`. Can be used without a namespace in front to indicate global

### Random
- Using *using namespace std* makes writing cin/cout easier. Instead of putting *std::cout*, you just write *cout*
- *const* insures immutability at runtime
- *constexpr* is somewhat alike to lambda funcs in python but this needs further research

### Pointers
- *nullptr* is a null pointer
- *new* is the new malloc with better features (like throwing an exception instead of a NULL and casting to type automatically)
### for loop
```cpp
#include <iostream>
using namespace std;

int main(void) {
	// Normal for-loop
	for (int i = 0; i != 10; i++) {
		continue;
	}
	
	// or...
	
	// for a in b loop (working with shallow copies here)
	int arr[] = {1, 2, 3, 4, 5};
	for (int i : arr) {
		cout << i;  // Returns: 12345
	}
	
	// or...
	
	// for a in b loop (working with actual elements)
	int v[] = {0,1,2,3,4,5,6,7,8,9};
	   for (auto& x : v) {
	       ++x;
	       cout << x;  // Returns: 1, 2, 3, etc.
	   }
	
	// or...
	
	// for-loop of pointers (no need for an initializer)
	char *ptr = "Hello, World!";
	char x = 'o';
	for (; *ptr != 0; ptr++) {
		if (*ptr == x) {
			cout << "Found it!";
		}
	}
}
```

### while loop
```cpp
int i = 0;
while (i < 10) {
	...
}
```

### structs (i.e. classes)
Accessing structs can be done either using the dot notation or using the arrow -> on properties if they are given as pointers
```cpp
struct name {
	<properties>;
};
```


### Trivia
- Nested functions are not supported