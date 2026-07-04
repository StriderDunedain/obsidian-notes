---
tags:
  - cs/architecture
updated: 2026-03-22
created: 2026-03-13
---
IEEE 754 is a standard of storing numbers using floating-point representation. There are two cases of its usage: for numbers bigger or equal to 1 (called *normalized*) and those between 0 and 1 (called *subnormal* or *denormalized*).

Here's the example for single precision
$$
\underbrace{0}_{\text{sign bit}} \ \underbrace{00000000}_{\text{exponent}} \ \underbrace{0000\dots0000}_{\text{mantissa (23 bits)}}
$$

### Normalized Numbers
For normalized numbers (i.e. those that obey the exponential notation) the formula for building the number is:
$$
(-1)^{\text{sign}} \times \text{mantissa} \times 2^{\text{e - q}}
$$

Where:
- $sign$ is the leading sign bit
- $q$ is the bias
- $e$ is the exponent

Note: before the mantissa (a.k.a. significand) there's an implied 1

### Denormalized Numbers
These numbers occur between 0 and 1 and help prevent underflows whereby dividing a very small number one would instantly get zero. The formula for those is:
$$
(-1)^{\text{sign}} \times 0.\text{mantissa} \times 2^{\text{-exponent}}
$$

The scientific notation is deliberately broken to prevent underflows where:
$$
{1.0 \times 2^{\text{-exponent}} \over \text{something}} \to 0
$$

Instead the numbers would go like this, gradually going down to zero:
$$
\begin{align}
0.1111\dots \times 2^{\text{-exponent}} \\
0.0111\dots \times 2^{\text{-exponent}} \\
0.0011\dots \times 2^{\text{-exponent}} \\
0.0001\dots \times 2^{\text{-exponent}}
\end{align}
$$

These numbers also happen to be very resource-intensive (Laurie Wired did a great video on that)

### Machine epsilon
Also called machine precision is such a value that can still be reliably identified as different from a 1, or like that:
$$
1 + \epsilon \neq 1
$$

IEEE 754 defines it as the number of bits in the mantissa:
$$
\epsilon = 2^{-p}, \text{ where p = number of bits in the mantissa}
$$

### Biased Exponent
The biased exponent $e$ in IEEE 754 is represented by:
$$
e = E - q
$$
Where:
- $E$ is the exponent
- $q$ is the bias (calculated as $(\text{№ of bits} \ \text{ mod } \ 2) - 1$):

| **q** | **Bits** | **Precision** |
| :---: | :------: | :-----------: |
|  127  |    32    |    Single     |
| 1023  |    64    |    Double     |
| 16383 |   128    |   Quadruple   |

### Example of storing
**Convert to Base 2**
$-5.375_{10} = -101.011_{2}$
**Normalize**
$-1.01011_{2} \cdot 2^{2}$
(So mantissa (for single-precision) will look like $010110000\dots000$ so that all in all it's 23 bits long)
**Biased Exponent**
$e = E + q = 2 + 127 = 10000001_{2}$

Further in [[Rounding Error Analysis]] and [[Biased Representation]]

***
### A Note on Fixed-Point Representation
A fixed-point representation divides bytes such that the first byte, for example, is the number's natural part and the second one is the decimal part. The separation is purely fictional. Isn't used in IEEE 754 but it's too short to make a separate note