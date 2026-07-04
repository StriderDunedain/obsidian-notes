---
tags:
  - cs/python
date: 2025-10-28
---
### How @wraps() works:
```python
from functools import wraps


def i_am_decorator(func):
    @wraps(func)
    def wrapper():
        """Докстринг функции-обёртки."""
        print('Действия до вызова декорируемой функции.')
        func()  # Вызываем декорируемую функцию.
        print('Действия после вызова декорируемой функции.')
    return wrapper


@i_am_decorator
def just_function():
    """Докстринг из just_function()."""
    print('Действия из функции just_function()')


print(just_function.__doc__)

# Докстринг из just_function().
```
### Classes can also be decorated
### @Instance, @class & @static methods
```python
class Student:
    default_course = 'Python Developer'
    # Инициализатор класса (метод):
    def __init__(self, name, surname, age):
        self.name = name
        self.surname = surname
        self.age = age
    
    # Метод экземпляра:
    def get_full_name(self):
        return f'{self.name} {self.surname}'
        
    # Метод класса:
    @classmethod
    def get_default_course(cls):
        return cls.default_course

    # Статический метод:
    @staticmethod
    def get_greeting():
        return 'Привет, студент!'
```

## @property method is for treating methods that look & behave more like attributes

Tags: #cs/ #python #notes 