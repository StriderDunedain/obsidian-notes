---
tags:
  - tba-place
---
> Depend on abstractions, not concretions

Depend on (abstract) interfaces, not (concrete) implementations

---
### ❌ Bad Example
```pseudo
class NotificationService
	email = EmailSender()  // Tightly coupled with email
```

### ✅ Fixed Version
Now implementations can be switched without changing `NotificationService`
```pseudo
interface MessageSender
	send(message)

class EmailSender implements MessageSender
class SmsSender implements MessageSender

class NotificationService
	sender: MessageSender
```