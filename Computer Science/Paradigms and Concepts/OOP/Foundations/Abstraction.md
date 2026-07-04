---
tags:
  - tba-place
---
> Show **what** the object does, not **how** the object does it

This is where interfaces come into play. In `paymentProcessor` the caller doesn't care how and by what means the payment is being handled, just that it is being handled

```pseudo
interface PaymentMethod
	pay(amount)
```