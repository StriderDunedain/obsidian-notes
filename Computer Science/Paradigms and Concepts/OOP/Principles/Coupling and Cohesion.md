---
tags:
  - tba-place
---
> **Goal**: High cohesion, low coupling

These are two very important metrics that describe how well a class is structured and how dependent different classes are on each other

---

### Cohesion
> How related are the contents of an entity?

A high cohesion entity has a very closely-related content. This is good
```
EmailSender
```
This is bad
```
EmailSenderInvoiceGeneratorPdfExporterUserValidator
```

### Coupling
> How dependent are the different entities on each other?

A low coupling entity isn't really dependent on other entities. Like this
```
Service -> DatabaseInterface
```

This is high coupling and should be avoided
```
Service -> MySQLConnection -> SQLParser -> Socket
```