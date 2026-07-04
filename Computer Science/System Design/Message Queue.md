---
tags:
  - cs/sysdes
updated: 2026-01-12
"created ": 2026-01-05
---
A system for handling tasks where the producer gives them out and somebody else processes them. Extremely fault-tolerant, asynchronous, automatically load-balancing — essentially the best way to organize task execution between different services. Much like anything else can be *transient* or *persistent*

#### Actors and Objects:
- **Publisher / Producer**: an entity that *publishes* messages to queue
- **Consumer / Subscriber**: an entity that retrieves (i.e. *consumes*) those messages sent by the publisher
- **Broker / Manager**: exactly what it sounds like

#### Types
- **Point-to-point (P2P) Queue**
    One producer sends messages to one consumer. The default basically. Can't go lower
- **Publish / Subscribe (Pub/Sub) Queue**
    Messages are published to a *topic* from which all the consumers subscribed to it get those messages. Useful for real-time chat updates to all users. Kinda reminds me of FK in databases 
- **Priority Queue**
    The more urgent -> the faster the processing. Critical error in log systems
- **Dead Letter Queue (DLQ)**
    A queue for all messages that couldn't be processed. Like logging errors is useful for later reviews of what went wrong and why

