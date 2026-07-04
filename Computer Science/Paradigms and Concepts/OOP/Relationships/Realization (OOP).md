---
tags:
  - tba-place
---
A class promises to provide the behavior defined by an interface or abstract contract. An "implements" relationship. Unfortunately, none of the languages I know use this so here's a general example
```pseudo
interface PaymentMethod
	function pay(amount)

interface CreditCard implements PaymentMethod
	function pay(amount)
		...
```
