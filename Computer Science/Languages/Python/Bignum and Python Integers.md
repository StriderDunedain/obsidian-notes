---
tags:
  - cs/python
updated: 2026-06-29
"created ": 2026-06-15
---
This is the standard representation for numbers in python (also called arbitrary-precision integer). Internally, numbers are stored in a struct called `PyLongObject` (long here being a fossil from the times when python had ints and longs). And instead of storing the number a bit pattern, python stores "limbs" (an array of ints) in base $2^{30}$[^1]. So it becomes something like:

```python
sign + dynamic array of 30-bit chunks
```

From that an integer is built[^2]. Here's an example. Let's take a number:
```python
x = 123456789
```
When mod'ded by $2^{30}$ it gives itself so it fits in only first element (naturally, each limb is 30 bits long):
```python
limb[0] = 123456789
```
So the struct become something like:
```python
sign = +
digits = [123456789]
```

Reconstruction follows the usual pattern:
```python
value = limb[0] * (2^30)^0
```

> [!warning] [[Two's Complement]]
> Python does NOT use two's complement - the sign is stored independently of the number however Python *behaves* as if a number had infinitely many sign bits in front of it

### Algorithms for multiplication
For smaller numbers it uses the regular school-style multiplication and for bigger numbers it uses [[Karatsuba]] and [[Toom-Cook]] algorithms

An especially good description of the algorithm and the internal CPython representation of an int is described in this [article](https://levelup.gitconnected.com/how-python-represents-integers-using-bignum-f8f0574d0d6b)

[^1]: $2^{30}$ is used instead of $2^{32}$ to accommodate for the possible carry bit on 64-bit systems

[^2]: This is actually the same method as the [[Horner Scheme]] (but in reverse)
