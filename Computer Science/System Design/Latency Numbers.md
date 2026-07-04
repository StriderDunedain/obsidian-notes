---
tags:
  - cs/sysdes
updated: 2026-01-31
created: 2026-01-31
---
Google's latency numbers from 2010, partially outdated

| Operation                           | Time                    |
| ----------------------------------- | :---------------------: |
| L1 cache reference                  | 0.5 ns                  |
| Branch mispredict                   | 5 ns                    |
| L2 cache reference                  | 7 ns                    |
| L2 cache miss                       | 100 ns                  |
| Mutex lock/unlock                   | 100 ns                  |
| Main memory reference               | 100 ns                  |
| Compress 1K bytes with Zippy        | 10,000 ns = 10 µs       |
| Send 2K bytes over 1Gbit/s network  | 20,000 ns = 20 µs       |
| Read 1 MB sequentially from memory  | 250,000 ns = 250 µs     |
| Round trip within same datacenter   | 500,000 ns = 500 µs     |
| Disk seek                           | 10,000,000 ns = 10 ms   |
| Read 1 MB sequentially from network | 10,000,000 ns = 10 ms   |
| Read 1 MB sequentially from disk    | 30,000,000 ns = 30 ms   |
| Read 1 MB randomly from disk        | 30,000,000 ns = 30 ms   |
| Send packet (CA → Netherlands → CA) | 150,000,000 ns = 150 ms |
***
**Conversion and Legend:**
ns = nanosecond
µs = microsecond
ms = millisecond

1 ns = 10^-9 seconds
1 µs= 10^-6 seconds = 1,000 ns
1 ms = 10^-3 seconds = 1,000 µs = 1,000,000 ns