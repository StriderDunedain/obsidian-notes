---
tags:
  - tba-place
---
> An entity should be **open to extensions** and **closed to modifications**

In practice, this means that a new entity shouldn't be a reason to change the existing infrastructure. Best summed up by a line from the [[Zen of Python]]: Special cases aren't special enough to break the rules

---

### ❌ Bad Example
Adding a `Triangle` requires modifying the function
```pseudo
function calculateArea(shape)
    if shape is Circle
        ...
    else if shape is Rectangle
        ...
```

### ✅ Fixed Version
Add a new entity that implements the required behavior
```pseudo
interface Shape
    function area()

class Circle implements Shape
    function area()

class Rectangle implements Shape
    function area()

function totalArea(shapes)
    for each shape in shapes
        total += shape.area()
```
