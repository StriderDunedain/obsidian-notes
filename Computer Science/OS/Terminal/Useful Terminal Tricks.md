---
tags:
  - cs/terminal
---
1. To append lines to a file, use:
```bash
echo "line" >> file
```
2. To remove the last line from a file, use:
```bash
sed -i '$d' file
```