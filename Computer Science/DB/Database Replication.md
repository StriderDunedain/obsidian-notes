---
tags:
  - cs/db
updated: 2026-01-07
created: 2026-01-07
---
### Master / slave
A master / slave relationship is such a structure revolves around one DB (i.e. master) getting all create, update, etc. requests and slaves receiving new data from the master. Slaves in turn work only on read operations. And since usually there are a lot more read than writes, this means that usually there're more slaves than masters ()