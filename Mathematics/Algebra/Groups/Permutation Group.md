---
tags:
  - math/abstract-algebra
  - math/permutation
  - math/combinatorics
  - math/group-theory
updated: 2026-04-03
created: 2026-03-30
---
A special case of [[Group]]s that is a combination of all possible [[Permutation]]s of a set of elements of $\{1, 2, \dots, n\}$ denoted as $S_{n}$. This is a bijective mapping (more in [[Mapping]]) and there exists exactly $n!$ of these permutations (i.e. $|S_{n}| = n!$)

> [!important] **Note**
> This is **not** a commutative group! Which means that $(\dots)_{1} \circ (\dots)_{2}$ can't be done vice versa! (with one exception below)

Some of permutations for $S_{3}$ would be, for example:
$$
a =
\begin{pmatrix}
1 & 3 & 2 \\
2 & 1 & 3
\end{pmatrix},
\quad
b =
\begin{pmatrix}
3 & 2 & 1 \\
2 & 3 & 1
\end{pmatrix},
\quad
c = 
\begin{pmatrix}
2 & 3 & 1 \\
2 & 1 & 3
\end{pmatrix}, \
\dots
$$
This means that every element of the upper row is tied to the an element below it (a sequence of numbers essentially, which is a permutation by definition):
$$
\begin{align}
& a = 1 \to 2, \ 3 \to 1, \ 2 \to 3 \\
& b = 3 \to 2, \ 2 \to 3, \ 1 \to 1 \\
& c = 2 \to 2, \ 3 \to 1, \ 1 \to 3
\end{align}
$$

### Identity
The *identity* of a permutation group is the *neutral element* of a group. It's often denoted as an empty cycle: $()$, a cycle of just one number: $(n)$ or just as $e$. It is its own inverse too since it doesn't really do anything:
$$

$$

### Cycles, pt. 1
A very handy way of writing permutations is by identifying a *cycle* inside a set and writing every element of it in one line:
$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\
1 & 3 & 2 & 4
\end{pmatrix}
= (3 \ 2)
$$
For example, the set above can be turned into a compact cycle by deleting the identity mappings that aren't doing anything (i.e. $1 \to 1$ and $4 \to 4$) and by doing:
$$
\begin{align}
& 2 \to 3 \\
& 3 \to 2
\end{align}
$$
Which is a cycle that can be written as $(3 \ 2)$. A double cycle such as that one is also called a *transposition*. Every cycle can be split into transpositions: 
$$
(e_{1}, e_{2},\dots, e_{n}) = (e_{1}, e_{2}) \circ (e_{2}, e_{3}) \circ \dots \circ (e_{n-1}, e_{n})
$$
#### Further examples
$$
\begin{pmatrix}
1 &  2 &  3 & 4 \\
3 &  4 &  2 & 1
\end{pmatrix} = (1 \ 3 \ 2 \ 4),
\quad
\begin{pmatrix}
1 &  2 &  3 &  4 \\
3 & 1 &  2 &  4
\end{pmatrix} = (1 \ 3 \ 2),
\quad
\begin{pmatrix}
1 &  2 & 3 & 4 \\
3 & 4 & 1 & 2
\end{pmatrix} = (1 \ 3)(2 \ 4)
$$
The last example is very interesting since it has two non-overlapping cycles, it can be written as $(1 \ 3)(2 \ 4)$ and by no means is it definitive: $(1 \ 3)(2 \ 4) = (4 \ 2)(1 \ 3)$. Which is closer inspected right below...

### Cycles, pt. 2
Since a cycle is in itself a permutation (oh my god...), $(1 \ 2)(1 \ 3)$ can also be represented by a composition:
$$
(1 \ 2)(1 \ 3) = (1 \ 2) \circ (1 \ 3)
$$
To compose that one has apply every element of the set of values $\{1, 2, 3\}$ to the following algorithm (let $(1 \ 3) = \tau$ and $(1 \ 2) = \sigma$). The main principle is to "move" to the next element once and record the step:
$$
\begin{align}
& \text{1. For "1":} \\
& \quad \tau(1) = 3 \text{ Move the result into the second term}\\
& \quad\sigma(3) = 3 \\
& \quad\implies 1 \to 3 \\
\\
& \text{2. For "2":} \\
& \quad\tau(2) = 2 \text{ Since there's no "2" in (1 3)} \\
& \quad\sigma(2) = 1 \\
& \quad\implies 2 \to 1 \\
\\
& \text{3. For "3":} \\
& \quad\tau(3) = 1 \\
& \quad\sigma(1) = 2 \\
& \quad\implies 3 \to 2 \text{ Takes the originial plugged value "3"}\\
\end{align}
$$

All of that nonsense is then used to build a new permutation of $(1 \ 3 \ 2)$ (since $1 \to 3, \ 3 \to 2, \ 2 \to 1$)

Another interesting aspect is that if the transpositions do not share elements (i.e. $(a \ b)(c \ d)$), their composition is themselves, so only in this case is the composition commutative:
$$
(a \ b)(c \ d) = (c \ d)(a \ b)
$$

### Cycles, pt. 3
A finite group $(G, *)$ with $n$ elements is called *cyclical* (*zyklisch* in German) when there's an element $g \in G$ that has the following property:
$$
G = \{g, g^{2}, g^{3}, \dots, g^{n}\}
$$
Then $g$ is called the *generator* element (or *erzeugendes Element* in German) of the group. It could also be a set of elements (transpositions are a great choice). Essentially this means that from that element one can get all other elements of the group $G$. So for a set $\{1, 2, 3\}$ the generator of $S_{3}$ are, for example, these two transpositions:
$$
(1 \ 2) \text{ and } (2 \ 3)
$$
Since they can generate any other element by repeatedly applying $\circ$:
$$
\begin{align}
& (1 \ 2) \\
& (2 \ 3) \\
& (1 \ 2) \circ (2 \ 3) =  (1 \ 2 \ 3) \\
& (2 \ 3) \circ (1 \ 2) = (1 \ 3 \ 2) \\
& (1 \ 2) \circ (2 \ 3) \circ (1 \ 2) = (1 \ 3) \\
& (1 \ 2) \circ (1 \ 2) = (1 \ 2)^{2} = e \\
& (2 \ 3) \circ (2 \ 3) = (2 \ 3)^{2} = e
\end{align}
$$
This get us all six elements of $S_{3}$.

> [!faq] What about $(3 \ 2 \ 1)$?
> While it is an element of the permutation of $\{1, 2, 3\}$, it's the same as the cycle of $(1 \ 3 \ 2)$ since rotating them doesn't do anything. It's basically a double ended queue 
