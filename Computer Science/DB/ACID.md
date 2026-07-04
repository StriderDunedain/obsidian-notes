---
tags:
  - cs/db
updated: 2026-06-14
created: 2025-11-04
---
Guarantees good database work

#### Atomicity
The transaction is a unit and it either happens completely or doesn't at all (rolls back)

#### Consistency
Every transaction brings the database into a new stable state

#### Isolation
No two transactions may interfere with each other

#### Durability
Once a transaction is committed it will exist in the database / can be restored some other way, i.e. doesn't get lost