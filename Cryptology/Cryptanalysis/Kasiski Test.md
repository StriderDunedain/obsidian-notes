---
tags:
  - cryptanalysis/cipher-breaking
updated: 2026-07-11
created: 2026-07-11
---
Published in #history/1863 it was named after a Polish general, although first created by Charles Babbage 9 years prior to that[^1]. Used on [[Homophonic Cipher]]s to determine the length of the keyword.

### Description
Basically, look at the ciphertext and determine recurring trigraphs (or bigger, less is a bit too random for accurate results). Then determine the distance between respective n-graphs. The common GCD of all of them[^2]. This factor $f$ will probably restrict the length of the keyword to that factor's multiple (i.e. $f + 0 \cdot f,\ f + 1 \cdot f, \ f + 2 \cdot f\dots$)
### Example
Say, you've determined the repeating patterns in this [[Vigenère Cipher]][^3]. The GCD that is in **every** distance is 5. Which indicates that the keyword's length is a multiple of 5 (probably, not a 100% estimate, could still be an insane coincidence):
![[kasiski_test.png]]

[^1]: Clear application of [[Stigler's Law]]

[^2]: Love the [[Euclidean Algorithm]] and then also search for another common factor TT

[^3]: Courtesy of the amazing [[Cryptology]] book
