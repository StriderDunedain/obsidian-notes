---
tags:
  - cs/automata
updated: 2026-05-01
created: 2026-04-23
---
> [!warning] This article is incomplete or just a number of facts
> This is just a shitty lecture and I don't have the time to get into this topic to make structured notes about this now

Abbreviated to CFG, it's is a system that describes how to build [[String]]s in a language. The properties of a grammar $G = (V, \Sigma, P, S)$ and mean:
- $N$ is the set of non-terminal symbols
- $\Sigma$ is the set of terminal symbols (i.e. the alphabet)
- $P$ is the set of production rules (recursively used to make a language)  #tba is it always recursive?  It's defined as: $P \subseteq N \times (N \cup \Sigma)^{*}$. More in detail below
- $S \in N$ is the starting symbol

Another restriction is $N \cap \Sigma = \emptyset$. The **total** or **working alphabet** is denoted as $\Gamma = N \cup \Sigma$

A handy way of thinking about them is this:
- $N$ are like inter-results in a recipe (dough, filling)
- $\Sigma$ are the actual ingredients (sugar, flour)
- $\Gamma$ is everything you might see during a recipe
- $P$ the rules by which a recipe takes you to the result

Notation:
- $A, B, C, \dots$ are used for non-terminals $\in N$
- $a, b, c, \dots$ are used in terminals $\in \Sigma$
- $\alpha, \beta, \gamma,\dots$ are words in the working alphabet $\in \Gamma^{*}$

These sit at level 2 of [[Chomsky Hierarchy]]

### Terminal vs Non-terminal
#### Terminals ($\Sigma$)
These are the actual symbols that will appear in a language (or its string). In our language that'd be letters and punctuation marks
#### Non-terminals ($V$)
These are the symbols that come up while making the final version of a string without them (like the imaginary root $i$ coming up and then vanishing, being just a stepping stone)

### Production rules $P$
> [!faq] What does $N \times (N \cup \Sigma)^{*}$ mean?
> Let's take a production rule $A \to \alpha$ where $A \in N$ and $\alpha$ is a string. The question is what can $\alpha$ contain. It could be terminals, non-terminals or both hence $(N \cup \Sigma)$ and the $*$ because it can be any length. And since the result is $(A, \alpha)$ that implies $N \times (N \cup \Sigma)^{*}$ (or just $N \times \Gamma^{*}$ using the total alphabet)

Two important concepts include semantics – the meaning of the sentence and the syntax – the rules by which the sentences are built. Their application is called:

#### Derivation (Ableitung)
The process of applying the rules. Formally it's such a sequence of steps that take you from $\Gamma$ to $\Sigma^{*}$:
$$
S \in \Gamma \Rightarrow \alpha_{1} \Rightarrow  \alpha_{2} \Rightarrow \dots \Rightarrow w \in \Sigma^{*} 
$$
This happens by taking one non-terminal at a time and applying a production rule using the **derivation relation** $\Rightarrow$:
$$
\alpha \Rightarrow \beta
$$
This means you can get $\beta$ from $\alpha$ in one step by using a prod rule. There exist different relations:
- $\Rightarrow$ one step
- $\Rightarrow^{*}$ zero or more steps
- $\Rightarrow^{+}$ one or more steps
Also the derivation can be right- and left-most. That just means take the first non-terminal from right or left, very genius. More in [[Parse Tree]]

> [!faq] The fuck it's all for?
> Well, you could define a language using it like that:
> $$
> L(G) = \{ w \in \Sigma^{*} \ | \ S \Rightarrow^{*} w \}
> $$
> Meaning that words $w$ are made of letters and there exists a derivation $S$ capable of making that word

#### Example
Grammar:
$$
S \to  aSb \ | \ \epsilon
$$
Derivation:
$$
S \Rightarrow aSb \Rightarrow aaSbb \Rightarrow aabb
$$
Replace $S$ with $aSb$ until you get tired and then end it by replacing $S$ with the empty string

### Examples
Let's build binary bigger than zero (i.e. $\{ 0, 1 \}^{+}$):
- $N = \{ S \}$, $\Sigma = \{ 0, 1 \}$ and $P = \{ \text{1: } \ S \to 0, \text{ 2: } \ S \to 1, \text{ 3: } \ S \to 0S, \text{ 4: } \ S \to 1S \}$
This way you can build any binary numbers bigger than zero
