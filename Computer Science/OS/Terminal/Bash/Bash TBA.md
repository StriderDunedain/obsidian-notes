---
tags:
  - cs/terminal
---
#tba Why does the first version cause the same effect as `clear` on the terminal and exists only with the second `exit()` call but the second one is fine:

```bash
# Num. 1
[ $# -eq 0 ] && python

# Num. 2
if [ $# -eq 0 ]; then
	python
	return
fi
```