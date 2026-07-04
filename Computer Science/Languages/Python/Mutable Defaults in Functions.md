---
tags:
  - cs/python
updated: 2026-05-27
created: 2026-05-27
---
Default parameters in Python functions get evaluated just once, at 'def', for the entire program run which means – if the default is mutable – it will get initialized once and remain for the whole program's lifetime:
```python
def f(arr=[]):
	arr.append(5)
	return arr

print(f())  # [5]
print(f())  # [5, 5]
print(f())  # [5, 5, 5]
```

### Use cases
While a seemingly weird design decision, it actually has its upsides. This, for example, will be a lot faster since it gets evaluated just once:
```python
import math

def has_to_be_fast(sin=math.sin, cos=math.cos):
```

Or if used in recursion:
```python
def calculate(a, b, c, memo={}):
    try:
        value = memo[a, b, c] # return already calculated value
    except KeyError:
        value = heavy_calculation(a, b, c)
        memo[a, b, c] = value # update the memo dictionary
    return value
```

(although nowadays it's probably a lot cleaner to call `lru_cache`)

### How to avoid
The most simple use case is something like this:
```python
def f(value=None):
	if value is None:
		value = "Default expression"
	# use / modify 'value' here
```

***
Courtesy of [this wonderful website](https://web.archive.org/web/20200221224620id_/http://effbot.org/zone/default-values.htm)