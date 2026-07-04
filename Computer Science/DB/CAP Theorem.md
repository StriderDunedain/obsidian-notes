---
tags:
  - cs/db
updated: 2026-06-15
created: 2026-06-15
---
> [!abstract] Definition
> When a [[Network Partition]] occurs, a distributed system can guarantee at most two of three properties: consistency, availability, and partition tolerance

Formulated by Eric Brewer and later proven formally by Seth Gilbert and Nancy Lynch

### Consistency
Every node sees the same data at the same time. After a successful write, all reads have to return the same most recent value

### Availability
Every request receives a response, even if some nodes are down. The response doesn't necessarily contain the most recent data

### Partition tolerance
The system continues operating despite communication failure between nodes


### Why the restriction?
Strictly speaking it's not a two of three, it's a choice between consistency and partition tolerance or availability and partition tolerance, called CP and AP systems respectively. A example: if nodes A and B can't communicate and a write to A occurs followed by a read from B, you have a choice: either refuse answer from B until comms are restored (CP) or still answer even if with old data (AP)