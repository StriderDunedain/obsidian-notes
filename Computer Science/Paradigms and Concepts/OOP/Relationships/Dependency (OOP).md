---
tags:
  - tba-place
---
This is a "temporarily uses" relationship. One class merely uses the other as a call parameter, for example. Considered the weakest relationship
```python
class ReportGenrator:
	def generate(printer: Printer):
		printer.print(report)
```