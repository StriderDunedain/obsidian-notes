---
tags:
  - cs/c
updated: 2026-06-22
created: 2026-05-19
"created ": 2026-06-01
---
cpp has both C-style and its own, safer[^1], casts. Since the implicit conversion work the same, let's look more carefully to explicit conversions:

#### C-style casting
You can do either of the following but both are discouraged bc they do dangerous conversions:
```c
double d = 3.14;
int x = (int)d;
```
```cpp
double d = 3.14;
int x = int(d);
```

#### C++ style casts
There are 4 explicit casts:
##### static_cast
This is the most common cast and is used for numeric, pointer and enum conversions as well as for constructor calls:
```cpp
double d = 3.14;
int x = static_cast<int>(d);
```
Or on classes with upcasting (but usually unnecessary bc it's almost always implicit):
```cpp
class Animal {};
class Dog : public Animal {};

Dog d;
Animal* a = static_cast<Animal*>(&d);
```

For enum it works like this:
```cpp
enum Color { RED, BLUE };
int x = static_cast<int>(RED);
```

> [!danger] static_cast is unsafe
> Just like in C, downcasting is still dangerous! There are **no** runtime checks for errors, see dynamic_cast for that


##### dynamic_cast
This is used for safe runtime polymorphic downcasting. Requires inheritance and at least one [[Virtual Function]]. It also checks conversions at runtime:
```cpp
#include <iostream>
using namespace std;

class Base {
public:
    virtual void show() {}
};

class Derived : public Base {
public:
    void hello() {
        cout << "Derived class";
    }
};

int main() {
    Base* b = new Derived;

    Derived* d = dynamic_cast<Derived*>(b);

    if (d)
        d->hello();
}
```

> [!danger] Failure of dynamic_cast
> Leads to nullptr and `std::bad_cast`


##### const_cast
> [!warning] Legacy
> It's mostly used for legacy APIs and backwards-compatibility

Adds or removes the const [[Type Qualifier]]:
```cpp
const int x = 5;

int* p = const_cast<int*>(&x);
```

> [!danger] UB
> Modifying an originally const object will cause UB. const_cast doesn't actually make the object writable, it's just a way to suppress a warning from the compiler


##### reinterpret_cast
Performs low-level reinterpretation of bits:
```cpp
int x = 65;
char* p = reinterpret_cast<char*>(&x);
```

> [!warning] Reinterpreting unmatching types
> You shouldn't do that because of compiler optimizations. Use `bit_cast` instead. It copies the bytes into a new object and doesn't confuse the compiler. So if you want to have the bit pattern of a float in [[IEEE 754]], for example, use `bit_cast`


### Direct-initialization vs direct-list-initialization
#tba-asap also do the typedef weird double name thing

[^1]: Compare with [[Type Casting in C]]