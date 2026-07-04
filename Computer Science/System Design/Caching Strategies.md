---
tags:
  - cs/sysdes
updated: 2026-01-14
"created ": 2026-01-12
---
The exact implementation should be decided based on the data and more importantly the *data access pattern* (i.e. the way data is handled). For handling expired cache, see [[Cache Eviction]]

### Strategies
 - **Cache Aside**
    - **Description**: the application is the middle man between the cache and the DB. Between the last two exists no connection. Your general implementation for read-heavy systems
    - **Flow**: Try to cache hit. If that misses, fetch from DB, give the client the answer and store it in the cache
    - **Examples**: Memcached and Redis
    - $ **Pros**: Resilient to cache failures and the structure of the data doesn't have to be the same as in the DB
    - ! **Cons**: When writing to DB there's the possible cache inconsistency. Fixable with a time to live (TTL) parameter

- **Read-Through Cache**
    - **Description**: the cache sits between the application and the DB. Also used for read-heavy systems. There's however the problem of the first hit being a 100% miss so ist Inches a penalty. That can dealt with using preheating or warming up the cache 
    - **Flow**: Application -> Cache and if we miss then a request to DB -> store it in cache and return it to application
    - $ **Pros**: None really. It's just mid
    - ! **Cons**: Data model can't be different from that of the DB

- **Write-Through Cache**
    - **Description**: the cache sits in-between the application and DB such that 2 write operations take place: to the cache first and the DB second
    - **Flow**: application -> cache -> DB
    - **Examples**: DynamoDB Accelerator
    - $ **Pros**: Eliminates the very concept of stale cache
    - ! **Cons**: Without a read-based cache as a supplement pretty useless as two write operations take place 

- **Write-Around Cache**
    - **Description**: First writes to DB and then to cache 
    - **Flow**: Application -> DB -> Cache
    - $ **Pros**: Useful when combined with other cases
    - ! **Cons**: ±

- **Write-Back / Write-Behind**
    - **Description**: First write to cache and then, at a later point in time, to DB asynchronously. Write-heavy hero
    - $ **Pros**: Feels fast despite being so 
    - ! **Cons**: If cache fails – everything goes to shit