---
tags:
  - cs/db
updated: 2026-06-14
created: 2026-06-14
---
#### Functional dependency
Basically if you have a piece of data you can reliably and uniquely identify the object related to it (X determines Y). Like having an ID for students

#### Inclusion Dependency
One set of attributes has to be in another set of attributes. Like all students' IDs in the school have to be in enrollment. That's what foreign keys enforce

The basic operations are: selection (which rows), projection (which columns) and join