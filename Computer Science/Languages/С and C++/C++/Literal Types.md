---
tags:
  - cs/c
updated: 2026-05-26
created: 2026-05-26
---
#### Diff between `"string"` and `"string"s`
The first one is a classical C-string and the other is a more python-string. The second one can be compared, concatenated, etc. Also the first one is a string literal while the other is an allocation of `std::string`, also requires `using namespace std::string_literals`