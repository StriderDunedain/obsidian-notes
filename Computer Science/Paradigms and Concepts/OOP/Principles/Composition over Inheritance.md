---
tags:
  - tba-place
---
> Prefer to make objects from objects rather then through inheritance

Since the inheritance is already notorious for its complexity, I'll illustrate only composition which allows to build the necessary behavior directly rather then derivatively through inheritance of inheritance of inheritance
```pseudo
class Bird
    movementBehavior


class FlyBehavior
    move()

class WalkBehavior
    move()

class SwimBehavior
    move()

sparrow.movement = FlyBehavior
penguin.movement = SwimBehavior
ostrich.movement = WalkBehavior
```