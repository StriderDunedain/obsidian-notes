---
tags:
  - math/number-theory
  - math/modular-arithmetic
  - math/computer-science
updated: 2026-04-05
created: 2026-03-25
---
### Definition
For two numbers $a, b$, where $b \neq 0$ there's just one representation $a = bq + r$, where $q, r \in \mathbb{Z}$ and $0 \leq r < |b|$. For further cases it is implied that $a , b > 0$, $r$ is the remainder (or Rest in German)

Closely related to [[Congruence Class]]

### Greatest common divisor (GCD)
A.k.a greatest common factor (GCF), Наибольший Общий Делитель (НОД) or größte gemeinsame Teiler (ggt) is defined as: for $a, b, d \in \mathbb{Z}$ and if $d \ | \ a$ and $d \ | \ b$ then is $d$ the GCD of $a$ and $b$. (For German it'll be $\text{ggt}(a, b)$). Can be found using the [[Euclidean Algorithm]]

### Programming, mod and negative numbers
#### Languages: Case 1
In languages that follow the true modulus (like Python or Matlab) the rule is: the sign follows the divisor:
$$
a \% b = a - b \cdot \lfloor a / b \rfloor  
$$
With the resulting table being:

| Expression | Result |
| :--------: | :----: |
|   7 % 3    |   1    |
|   -7 % 3   |   -1   |
|   7 % -3   |   1    |
|  -7 % -3   |   -1   |
#### Languages: Case 2
In languages like C, C++ and Java the sign follows the dividend (i.e. that which is being divided):
$$
a \% b = a - (a / b) \cdot b
$$
With the resulting table looking like this:

| Expression | Result |
| :--------: | :----: |
|   7 % 3    |   1    |
|   -7 % 3   |   -1   |
|   7 % -3   |   1    |
|  -7 % -3   |   -1   |
The reason why these languages don't follow the math consensus on the % operator is because of the subtle difference between the remainder and the modulus (these languages follow the remainder whereas the others follow modulus). The difference lies in the definition. The modulo is defines as
$$
a \equiv r \text{ mod } n, \ 0 \leq r < |n|
$$
This guarantees a non-negative result as long as $n > 0$

And in the other ones followed a different path of choosing the remainder over the modulo because of hardware simplicity and compatibility with the division operator. To get true modulo in C use:
```C
int true_mod = (a % b + b) % b;
```
