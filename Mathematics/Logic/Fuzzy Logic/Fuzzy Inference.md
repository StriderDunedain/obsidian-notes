---
tags:
  - math/logic
updated: 2026-03-19
created: 2026-03-19
---
Substitution for "expression" in Boolean algebra that follow the following structure:
$$
\text{IF } \ p \ \text{ THEN } \ c
$$
Example would be:
$$
\text{IF } \ \text{temperature = hot} \ \text{ THEN } \ \text{fan speed is fast}
$$

Rule activation $\alpha$ is the strength of this rule: by $\alpha = 0$ it's completely off, by $\alpha = 1$ it is completely in effect and by $0 < \alpha < 1$ is the degree of how strongly in effect it is 
### Max–Min Inference
**Algorithm**:
- Take the minimum of rules' activation strength
- Cut at that point (that's called "clipping") — that's the answer. Outcome is nice and flat

### Max–Prod Inference
**Algorithm**:
- Take the maximum of rules' activation strength
- Multiply the activation strength by the value of previous step over and over again to get a slope
That's called "scaling"

### Example
**Prerequisites**:
Let's say the rule activation $\alpha = 0.6$, $z$ be the speed of the fan and $\mu_{fast}(z)$ the function that describes how "fast" the fan is spinning. $\mu_{out}(z)$ will be the function that makes the output set. Let's also define this table:

|   $z$ (speed)   |  0  | 25  | 50  | 75  | 100 |
| :-------------: | :-: | :-: | :-: | :-: | :-: |
| $\mu_{fast}(z)$ |  0  | 0.2 | 0.5 | 0.8 |  1  |

#### Case: Max-Min Inference
Since this is the **max-min** inference, the next step is to determine what is *weaker*:
$$
\mu_{out}(z) = min(\alpha, \ \mu_{fast}(z))
$$

|   $z$ (speed)   |  0  | 25  | 50  | 75  | 100 |
| :-------------: | :-: | :-: | :-: | :-: | :-: |
| $\mu_{fast}(z)$ |  0  | 0.2 | 0.5 | 0.8 |  1  |
|   $\mu_{out}$   |  0  | 0.2 | 0.5 | **0.6** | **0.6** |
Which means that everything above **0.6** gets cut down. We take the weakest rule. The result looks like this:
![[Pasted image 20260319151354.png]]

#### Case: Max-Prod Inference
Since this is the **max-prod** inference, the next step is to determine what is *stronger*:
$$
\mu_{out}(x, y) = max(\mu_{A}(x), \ \mu_{B}(y))
$$
(This is a bad example since we have just one rule of temperature so here there's just one value, nevertheless...)

Then find the *degree of strength*:
$$
\mu_{out}(z) = \alpha \cdot \mu_{fast}(z)
$$

|   $z$ (speed)   |  0  |  25  | 50  |  75  | 100 |
| :-------------: | :-: | :--: | :-: | :--: | :-: |
| $\mu_{fast}(z)$ |  0  | 0.2  | 0.5 | 0.8  |  1  |
|   $\mu_{out}$   |  0  | 0.12 | 0.3 | 0.48 | 0.6 |
This makes a slope of rising strength and "assuredness". The result looks like this:
![[Pasted image 20260319151423.png]]
### Defuzzifying
Getting an actual value out of this mess. There are a lot of methods for this like maximum height, mean of maximum or center of gravity