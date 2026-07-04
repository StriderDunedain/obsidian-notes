---
updated: 2026-05-26
created: 2026-03-11
tags:
  - cs/architecture
  - tba
"created ": 2026-03-23
---
Also called *Zweierkomplement* in German, this is the usual way of representing negative numbers nowadays (mainly because there's no ±0). It works by taking the [[One's Complement]] of a number and adding 1:
$$
\sim x \ = \ \text{not } x + 1
$$

Another quick way of getting the complement is by going from right to left until the first 1, carry it over to the complemented number and invert all other bits.

![[Pasted image 20260318114057.png]]

### Programming
The ~ is very commonly used in cs/ languages[^1] to get two's comp:
```python
# For 2 the ~2 is -3, etc.
for n in range(5):
	print(f"{n = } -> {format(n, 'b')} | {~n = } -> {format(~n, 'b')}")
```

### Subtraction in binary
To subtract one number in binary from another:
![[Pasted image 20260318121436.png]]

1. Get the complement of the subtrahend:
![[Pasted image 20260318121415.png]]

2. Add the result to the minuend (no carry means the number is negative, else assume positive and discard it):
![[Pasted image 20260318121523.png]]

3. Do yet another complement on the result:
![[Pasted image 20260318121710.png]]

[^1]: Python is a special case, look to [[Bignum and Python Integers]] for more info
