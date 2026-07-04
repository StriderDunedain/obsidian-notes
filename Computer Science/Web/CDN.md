---
tags:
  - cs/web
updated: 2026-01-14
"created ": 2026-01-05
---
A Content Delivery Network is kind of like a [[DNS]] but for static files. Here even the geolocation is important for latency. In the HTTP header for requesting a resource from a server one can add an option Time-To-Live (TTL) param so as to say how long that cache should be available for 