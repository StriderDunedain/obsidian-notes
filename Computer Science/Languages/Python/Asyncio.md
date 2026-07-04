---
tags:
  - cs/python
date: 2025-10-29
---
Asynchronous execution of a programm implies realizing one of two(?) of the following paradigms:
1. **Concurrency (Конкурентность):**
     Uses many *threads* - a work branch for executing some piece of code - and switches between them, only one is in work - the others are stopped (`threading` module in Python)
2. **Parallelism (Параллелизм):**
	  Uses *processes* - something like a *thread* but bigger and more solid - actually allows you to run pieces of code simultaneously - needs processors (`multiprocessing` module in Python)
3. **Subroutine (???):**
     Regular piece of code that, when started, **must** be executed **to the end**
4. **Coroutine (Корутина / Сопрограмма):**
     A *subroutine* that can be entered, stopped & resumed at any time

Following: [[Multiprocessing]] | [[Threading]]

### Interesting Features about `asyncio` module & Python async syntax:
1. `async / await` syntax doesn't create *coroutines* by itself. *Tasks* have to be created in order to reach concurrency
2. All awaiting *tasks* will start as soon as an `await` has been met
3. 
### Questions to AsyncProgramming:
1. GIL - how where & when
2. pros & cons of `threading` & `multiprocessing` in Python
3. Stricter definitions of thread and process - a little vague on the how
4. `Asyncio` - difference between threading and multiprocessing
5. Are there any other ways of executing asynchronous code?
6. Потоки и процессы могут пересекаться?
7. How to stop async funcs in python the correct way?
8. Correctly handling exceptions?
9. Can / Should multiprocessing, threading and asyncio be used together?
10. When to choose a coroutine vs task & vice versa?
11. How do coroutines and tasks connected?
12. How does asyncio "wrap" coroutines in tasks?
13. How to stop coroutines?
14. Are tasks stopped after exceptions?

Tags: #cs/ #async #notes #python 