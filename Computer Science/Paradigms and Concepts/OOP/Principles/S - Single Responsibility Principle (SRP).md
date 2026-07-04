---
tags:
  - tba-place
---
> A class should have only **one reason to change**

In practice, this means that class should only have **one responsibility**

---
### ❌ Bad Example
```pseudo
class UserManager  // Does everything
    function createUser()
    function sendEmail()
    function generatePdfReport()
    function saveToDatabase()
```

### ✅ Fixed Version
```pseudo

// Tasks 

class UserService
    function createUser()

class EmailService
    function sendEmail()

class ReportGenerator
    function generatePdf()

class UserRepository
    function save()
```