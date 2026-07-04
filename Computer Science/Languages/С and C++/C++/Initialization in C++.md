---
tags:
  - cs/c
updated: 2026-05-25
created: 2026-05-25
---
There exist two ways of variable initialization in cpp:

#### Copy-initialization
A somewhat obsolete way of initializing (not assigning, despite the "=") that allows implicit conversions:
```cpp
int x = 5.6;  // gets cut to 5
std::string s = "hello";  // this calls the constructor
```

#### Direct-initialization
This calls the class constructor directly, still allows implicit conversions:
```cpp
int c(6.5);  // or...
std::string s("hello");
```
The only difference lies in class constructors marked `explicit`:
```cpp
class Test {
public:
	explicit Test(int) {}
};

Test a(5);  // Ok
Test b = 5;  // Error
```

##### Direct List initialization
A sub-topic or something, this is the most modern way to initialize variables. Prevents implicit conversions and garbage values:
```cpp
int d{7};  // Ok
int a{4.5};  // Error
int e{};  // '0', for string it's "", etc.
```