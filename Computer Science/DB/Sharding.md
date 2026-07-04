---
tags:
  - cs/db
updated: 2026-01-11
"created ": 2026-01-05
---
A technique for splitting a monolith database into shards – small sub-databases that contain restricted info (another approach would be [[Partitioning]]. It's very important to choose the sharding / partition key by which the monolith will be split. Another important caveat to look out for is the celebrity problem when a few ultra-popular entries end up in the same shard which causes it to wear a lot faster. 

Cons:
- ! Shard problem as a SPOF of sorts

- ! Increasing hard to keep every shard up to date

- ! Increasingly hard to perform complex operations (like JOIN)

Pros:
- $ Makes it easy to horizontally scale and is very efficient in comparison to size

- $ Handling a multitude of operations