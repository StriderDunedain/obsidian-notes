---
tags:
  - cs/db
updated: 2026-06-14
created: 2026-06-14
---
Proposed by [[ANSI]] in the #history/1970 to represent databases and achieve data independence; expands to Standards Planning and Requirements Committee

#### External Level (User View)
Different users see only the data relevant to them. The latter is also called an external schema

#### Conceptual Level (Logical View)
That's the logical structure of the database, irrespective of the physical implementation. Pseudocode-level kinda

#### Internal Level (Physical View)
That's how the database is actually works: files, indexes, b-trees, hash tables, etc.