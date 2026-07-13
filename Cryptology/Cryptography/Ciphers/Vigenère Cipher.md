---
tags:
  - cryptography/cipher
updated: 2026-07-11
created: 2026-07-11
---
A [[Homophonic Cipher]] was created by some Italian guy in #history/1553 and was considered to be unbreakable for around three centuries until [[Kasiski Test]] and [[Friedman Test]] advanced it to the point of being somewhat pliable to cryptanalysis

### Work mechanism
It takes a square filled with all possible circular [[Permutation]]s[^1] of an alphabet using the [[Caesar Cipher]] and a keyword (shorter ones are easier to break as well as tremendously big ones). You then write the keyword repeatedly above the cleartext and the current letter of the keyword is the "index" of the row (in the meaning that the row starts from this letter) and the "index" of the ciphertext letter is determined by the current cleartext letter:

![[vegenere_cipher.png]]

[^1]: I wonder whether this has anything to do with a [[Circulant Matrix]]? Seem close in name #tba

#tba Is it still that unbreakable today or are any keywords susceptible to cryptanalysis?