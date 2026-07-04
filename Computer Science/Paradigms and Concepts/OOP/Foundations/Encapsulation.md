---
tags:
  - tba-place
---
> Hide the externals and expose only that what is necessary

Essentially, don't give people control over stuff they don't need

---
Here users of `Bank` can't modify the balance directly, only by authorized means
```pseudo
class BankAccount
    private balance

    function deposit(amount)
        balance += amount

    function getBalance()
        return balance
```
