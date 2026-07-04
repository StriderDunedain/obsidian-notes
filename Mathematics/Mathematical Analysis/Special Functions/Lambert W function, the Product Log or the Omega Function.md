---
tags:
  - math/mathematical-analysis
updated: 2026-03-19
"created ": 2025-11-09
created: 2025-11-11
---
### Definition
The Lambert W function helps with finding the roots of the equations where x is present as a power and as a multiplier:
$$ y = 2^x \cdot x$$
And the product log helps by defining that:
$$
\forall x \in \mathbb{R},\ z = x \cdot e^x \implies W(z) = x \text{ essentially } w \mapsto w \cdot e^w 
$$


Which make the W function is the inverse of a function:
$$f(x) = x * e^x \to W(x) := f^{-1}(x)$$
$$
\begin{align}
\text{Which by definition...} \\
f(f^{-1}(x)) = x \\ 
f^{-1}(f(x)) = x \\
\text{... whould mean that} \\
\end{align}
$$
$$f(W(x)) = x \to W(x \cdot e^x) = x$$

It's useful to think about it like you think of logs or roots: they don't really give you a number, instead they say that this is a number but the calculations behind it are complicated (for the Omega function it's usually [[Newton-Raphson Method]]). So something like this: W(5) is actually a number. Just a complicated to calculate one. The W is just historical and the omega bc it resembles this constant
$$\Omega \cdot e^{\Omega} = 1$$
When plotted has three [branches](https://www.desmos.com/calculator/wqwoud7uvk):
$$
\begin{cases}
W_0(z): & \text{Principal branch, real for } z \geq -\frac{1}{e}, \\
W_{-1}(z): & \text{Real-valued branch for } -\frac{1}{e} \leq z < 0, \\
W_k(z): & \text{Complex-valued branches for integers } k \neq 0, -1.
\end{cases}
$$
### Example
An equation solved using the product log would look something akin to this:
$$
\begin{align*}
&1. \ 2^x + x = 5 \text{ | \\ } 2^x \\
&2. \ 1 = 2^{-x} \cdot (5 - x) \text{ | } \cdot 2^5 \\
&3. \ 32 = 2^{5 - x} \cdot (5 - x) \text{ | sub 2 for } e^{ln(2)} \\
&4. \ 32 = (5 - x) \cdot (e^{\ln(2)})^{5 - x} \text{ | } \cdot \ln(2) \\
&5. \ \ln(2) \cdot (5 - x) \cdot e^{\ln(2)(5 - x)} = 32 \cdot \ln(2) \\
&6. \ W(\text{v.s.}) = W(\text{v.s.}) \text{ | using } W(x \cdot e^x) = x \\
&7. \ (5 - x) \ln(2) = W(32 \cdot \ln(2)) \\
&8. \ x = 5 - \frac{W(32 \cdot \ln(2))}{\ln(2)}
\end{align*}
$$
### Derivative
The derivative of the W function is as follows (usually has 3 ways of being written, this is the most common one)
$$W^{\prime}(x) = \frac{W(x)}{x \cdot (W(x) + 1)}$$
