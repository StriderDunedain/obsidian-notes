---
tags:
  - math/logic
updated: 2026-06-25
created: 2026-03-18
"created ": 2026-03-29
---
Also called *KV-Diagramme* (for **K**arnaugh and **V**eitch) or *K-map* is a table used to visually solve expressions, conforming to [[Quine-McCluskey]]. Can be used on any number of variables but more than 4 is too tedious (since the number of cells is $2^n$). Every row and column correspond to a variable and the cell on the intersection their conjunction:

|          |       $A$        |       $\neg A$        |
| :------: | :--------------: | :-------------------: |
|   $B$    |   $A \land B$    |   $\neg A \land B$    |
| $\neg B$ | $A \land \neg B$ | $\neg A \land \neg B$ |

### Algorithm
The equation first has to be in DNF (more in [[CNF and DNF]])!
1. Map every combination of every variable of an expression on a table
2. Where a minterm on the map fits place a $1$
3. For every cell with a $1$ try connecting them with other $1$s and check which variables stay constant and which differ
4. Those that differ are left out, those that don't are essential
5. Write the simplified version

**Note**: The table also bends sideways and top-down (the different variables that make the same row in this "cylindrical" shape is ok, they are still counted as different albeit on the same line and neighbors now)
![[Pasted image 20260329153251.png]]
