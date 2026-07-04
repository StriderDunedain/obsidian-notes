---
tags:
  - cs/db
updated: 2026-01-11
"created ": 2026-01-11
---
A technique for splitting databases' tables by some criteria (instead of databases themselves using [[Sharding]]) like a table of orders partitioned by months

Pros:
- $ Relatively easy to maintain 

- $ Useful for splitting one huge dataset when sharding doesn't make sense

Cons:
- ! Still harder to make JOINs and generally keep it up than a monolithic architecture