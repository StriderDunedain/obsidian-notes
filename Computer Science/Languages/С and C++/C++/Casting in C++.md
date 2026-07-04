---
tags:
  - cs/c
updated: 2026-06-21
created: 2026-06-06
"created ": 2026-06-06
---
Here're some unexpected / interesting aspects of conversion:
```cpp
int n{ 3.0 };  // brace init disallows even this

constexpr double f { 0.1 };
float f1 = f;  // for consts even lossy conversions are ok
```

### OH MY FUCKING GOD!!!
Apparently, the first one is "surprising" and is a no-no but the second one is so mundane it's not worth the error:
```cpp
#include <iostream>

int main() {
    int n { 3.0 };  // Uh-uh, bad boy
    float f { 1.2345678 };  // Sure thing buddy (gets truncated to 1.2346)
}
```

#tba Read [cppref for arithmetic conversions](https://en.cppreference.com/cpp/language/usual_arithmetic_conversions)

> [!tip] Names
> **Numerical conversion** is explicit casting and a **numerical promotion** is the same thing that the compiler does automatically (usually to make the operand "workable" on the variable)