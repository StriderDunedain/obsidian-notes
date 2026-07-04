---
tags:
  - cs/paradigm
  - oop
updated: 2025-11-02
created: 2025-11-02
---
A programming paradigm dictating that data can and will be processed according to it logically belonging in one "class" with its corresponding "methods" - how the data can be processed. From OOP comes [[Aspect-Oriented Programming]]

The four main pillars are
1. [[Encapsulation]]
2. [[Abstraction]]
3. Inheritance
4. [[Polymorphism]]

On those 4 pillars there stand numerous other rules and guidelines, including but not limited to
1. [[Coupling and Cohesion]]
2. [[Composition over Inheritance]]
3. [[Dependency Injection]]
4. [[The Law of Demeter]]

There also exist whole [[Design Patterns]] of how OOP programs should be structured and how they use the methods and data at their disposal
	...

#tba To be created

Here’s a **copyable checklist** of everything you’re missing / should add next, grouped so you can work through it later without losing structure.

---

# 🧠 OOP Vault Expansion Checklist

## 🔴 1. Design Patterns (BIG PRIORITY)

### Creational

-  Factory Method
    
-  Abstract Factory
    
-  Builder
    
-  Prototype
    
-  Singleton
    

### Structural

-  Adapter
    
-  Decorator ⭐
    
-  Facade
    
-  Composite
    
-  Proxy
    
-  Bridge
    

### Behavioral

-  Strategy ⭐
    
-  Observer ⭐
    
-  Command
    
-  State ⭐
    
-  Template Method
    
-  Iterator
    
-  Mediator
    
-  Chain of Responsibility
    

---

## 🔴 2. Domain-Driven Design (DDD)

### Core concepts

-  Entity
    
-  Value Object ⭐
    
-  Aggregate Root ⭐
    
-  Repository
    
-  Domain Service
    
-  Factory (DDD version)
    
-  Bounded Context ⭐⭐
    

### Modeling concepts

-  Domain vs Application vs Infrastructure layers
    
-  Ubiquitous Language
    

---

## 🔴 3. Architecture Concepts

-  Clean Architecture
    
-  Hexagonal Architecture (Ports & Adapters)
    
-  Layered Architecture (MVC style)
    
-  CQRS (Command Query Responsibility Segregation)
    
-  Event-driven architecture basics
    

---

## 🟠 4. Important OOP Thinking Tools

-  Tell, Don’t Ask principle
    
-  Message Passing (objects communicate via behavior)
    
-  Object Lifecycle (creation → use → destruction)
    
-  Invariants (rules objects must always obey)
    
-  Design by Contract (preconditions / postconditions)
    
-  Static vs Instance methods (when to use each)
    
-  Access modifiers deep dive (public/private/protected/etc.)
    

---

## 🟠 5. Core Concept Gaps

-  Immutability ⭐
    
-  Object Identity vs Equality ⭐
    
-  Message passing vs method calls (clarification note)
    
-  Composition patterns (Strategy usage in practice)
    
-  Polymorphism in real systems (not just theory)
    

---

## 🟠 6. Anti-patterns (VERY IMPORTANT)

-  Anemic Domain Model ⭐
    
-  God Object
    
-  Inheritance abuse
    
-  Tight coupling as design failure
    
-  Feature envy
    
-  Shotgun surgery (code change ripple problem)
    

---

## 🟡 7. Coupling / Cohesion Deepening

-  Types of coupling (data, control, stamp, etc.)
    
-  Coupling vs architecture-level dependency flow
    
-  Cohesion types (functional cohesion, etc.)
    

---

## 🟡 8. Missing “Bridge” Understanding Notes

These are high-value comparison notes:

-  Composition vs Inheritance (deep version)
    
-  Interface vs Abstract Class
    
-  Dependency vs Association vs Composition
    
-  Dependency Injection vs Dependency Inversion (DIP)
    
-  Polymorphism vs Inheritance
    
-  Coupling vs Cohesion
    

---

## 🟡 9. Law & Principles (add connections)

-  Law of Demeter (link properly to coupling + encapsulation)
    
-  Tell, Don’t Ask (link to encapsulation)
    
-  SOLID interconnections map (one note explaining all relations)
    

---

## 🟢 10. Optional / Advanced Concepts

-  Event-driven design (publish/subscribe)
    
-  Immutability patterns in OOP systems
    
-  Object role modeling (conceptual modeling style)
    
-  Dependency graph thinking
    
-  Law of Leaky Abstractions
    
-  Static typing vs dynamic polymorphism tradeoffs
    

---

## 🟢 11. Missing “meta” understanding notes

-  Why composition replaced inheritance in modern systems
    
-  Why SOLID exists (historical motivation)
    
-  When NOT to use design patterns
    
-  When NOT to use inheritance
    
-  When OOP breaks down (limits of the paradigm)
    

---

# ⭐ Priority Legend

- ⭐ = high impact (do these first)
    
- ⭐⭐ = very high impact / system-level understanding
    

---