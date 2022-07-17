# Python Style Guide

## Index

1. Introduction
2. Zen of Python
3. Python Programming Language
4. Peps
5. Style Guide
6. Structural Naming Conventions
    1. Project Name
    2. Packages
    3. Modules
    4. Main Module
    5. Test Module
7. Code Naming Conventions
    1. Variables
    2. Constants
    3. Functions
    4. Parameters
    5. Classes
    6. Methods
    7. Magic Methods
    8. Test Methods
    9. Unused Resources
    10. Errors
    11. Error Alias
    12. Reserved Words
8. Access Modifiers
    1. Module Variables
    2. Module Constants
    3. Module Functions
    4. Module Classes
    5. Class Variables
    6. Class Constants
    7. Class Attributes
    8. Class Methods
9. Strings
10. 

## Introduction

This Python style guide was made focusing in the essential to create a clean and maintainable code. I really encourage the usage of any style guide, since this guarantees that your code can be easily understood by developers. There are other styles guides made from big projects/companies, and I have to confess that some tips of this style guide was obtained from these documents, but, another tips I created by myself.

Avoid seeing this material as rules for your development, but use this as a convention to standardization. If you prefer to follow your style for coding some specific situation, go ahead! But, I just ask you to check and determine if this style you choose was the best choice, or if there is some situation that it could break somewhere. 

## Zen of Python

This document has used all of [Zen Of Python](https://peps.python.org/pep-0020/) principles. This is the law:

```text
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

## Python Programming Language

Python is a interpreted programming language that use the tabs or spaces as code blocks. The correct indentation is mandatory, and see this as a good advantage, because you know that for any Python code you see, it will be formatted correctly. If you are new in Python, and never have programmed in this spectacular language, please, take a look in my [Python Guide](https://github.com/vinibiavatti1/PythonGuide), where you can find a pocket documentation with examples that you can use to learn Python easily and faster. 

## PEPs

In this document I used everything of [PEP8](https://peps.python.org/pep-0008/), and more other styles that there aren't in it. PEP8 is the most known code style for python programmers, so, using this as the base for this style guide can guarantee that everyone can be adapted very well.

For typehints, this style follow the same of [PEP484](https://peps.python.org/pep-0484/).

For docstrings, I used some characteristics of [Google Style Guide](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings) and [PEP257](https://peps.python.org/pep-0257/). After comparing some ways to create docstrings using these conventions, I could see improvements and other modifications that could facilitate the documentation of the code. Because of that, I decided to change some of the conventions thinking more in code standardization. Don't forget the zen principle: _Simple is better than complex._

Document the code is extremely important, for the developers and for who will maintain this code in the future. But, we know that it is not everyone that like or can prioritize it, so I focused in the easiest way to avoid giving more work for do it, without spending a lot of time.

## Style Guide

This style guide is separated by sections, where each section corresponds to good practices for coding in a specific syntax/context. Here you can find naming conventions, indentation tips, comment hints, etc. You can also find reasons for the usage of some style, _do_ and _don'ts_, and examples.

If you have some suggestion/question, be free to open an issue to this repository, and we will evaluate your orders with all of will.

## Structural Naming Conventions

TODO description

### Project Name

> Project root folder

```python
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Do not use capital letters

# Do
my_project

# Don't
myproject

# Don't
MyProject
```

### Packages

> Folders with `__init__.py` file.

```python
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Do not use capital letters

# Do
my_package

# Don't
mypackage

# Don't
MyPackage
```

### Modules

> Files with `.py` extension.

```python
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Do not use capital letters

# Do
my_module.py

# Do
abc_.py

# Don't
mymodule.py

# Don't
MyModule.py
```

### Main Module

> Application entry-point file

```python
# Use the "main.py" for the main file

# Do
main.py

# Don't
app.py

# Don't
init.py
```

### Test Module

> Test entry-point file

```python
# Use the "" name for the main test file

# Do
test.py

# Don't
testing.py
```

## Code Naming Conventions

The naming convention follows the same of PEP8. Read this section to check more examples and situations for naming.

### Variables

```python
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Do not use capital letters

# Do
person_name = 'John Due'

# Don't
personName = 'John Due'

# Don't
personname = 'John Due'
```

### Constants

```python
# Use a good representation name
# Use underscore to separate
# Use all letters capitalized
# Do not use special symbols

# Do
PI = 3.14

# Don't
pi = 3.14 
```

### Functions

```python
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Do not use capital letters

# Do
def sum_numbers(x, y):
    return x + y

# Don't
def sumNumbers(x, y):
    return x + y
```

### Parameters

```python
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Do not use capital letters

# Do
def multiply(number_1, number_2):
    return number_1 * number_2

# Don't
def multiply(number1, n):
    return number1 * n
```

### Classes

```python
# Use a good representation name
# Do not use underscore to separate
# Use camel case
# Do not use special symbols
# Capitalize all letters of an abbreviation
# Do not use letters to represent the type, like "I" for interface

# Do
class HTTPServer:
    pass

# Don't
class HttpServer:
    pass

# Don't
class IClientServer(ABC):
    pass

# Don't
class ABCClientServer(ABC):
    pass
```

### Methods

```python
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Instance methods should have their first parameter named 'self'.
# Class methods should have their first parameter named 'cls'
# Static methods don't need to have a default first parameter
# Do not use capital letters

# Do
class DataProcessor:
    def process_data(self):
        pass

    @classmethod
    def create(cls):
        pass

    @staticmethod
    def version():
        pass
```

### Magic Methods

```python
# Use a good representation name
# Use dunder "__" as prefix and suffix
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Do not use capital letters

# Do
class DataProcessor:
    def __init__(self):
        pass

# Don't
class DataProcessor:
    def init(self):
        pass
```

### Test Methods (TestCase)

```python
# Use "test_" as prefix
# Use a good representation name
# Use underscore to separate
# Do not use camel case
# Do not use special symbols
# Must have their first parameter named 'self'.
# Do not use capital letters

# Do
class ListTest(unittest.TestCase):
    def test_append(self):
        pass

# Don't
class ListTest(unittest.TestCase):
    def append(self):
        pass
```

### Unused Resources

```python
# Use "_" as name
# If there is other unused variable named "_", add other underscore "__"

# Do
for _, value in object_map.items():
    pass

# Do
for _, inner in object_map.items():
    for __, value in inner.items():
        pass

# Don't
for unused, value in object_map.items():
    pass
```

### Errors

```python
# Use a good representation name
# Do not use underscore to separate
# Use camel case
# Do not use special symbols
# Do not use letters to represent the type like "E" for Error
# Use the 'Error' suffix in the exception class name
# Extends the Exception class or subclass
# Never extend the "BaseException" class. Use it for an specific situation

# Do
class ValidationError(Exception):
    pass

# Don't
class ValidationException(Exception):
    pass

# Don't
class EValidation(Exception):
    pass
```

### Error Alias

```python
# Use the 'err' name to reference the error
# When the 'err' name is already used, add an underscore as suffix

# Do
try:
    pass
except ValueError as err: 
    pass

# Do
try:
    pass
except ValueError as err: 
    try:
        pass
    except ValueError as err_: 
        pass

# Don't
try:
    pass
except ValueError as error: 
    pass
```

### Reserved Words

```python
# Never use a python reserved word or builtin word as name for any artifact
# Use underline "_" as suffix
# When the name is already used, add an underscore as suffix

# Do
from_ = 'Hello'

# Do
def input_(message):
    pass

# Don't
any = True

# Don't
def sum(x, y):
    return x + y
```

## Access Modifiers

Access Modifiers are the way to determinate the accessibility of the resources in a class or module. Python does't have any consistency validator to check it, only for private resources where it uses [Name Mangling](https://en.wikipedia.org/wiki/Name_mangling) to avoid direct calls. So, to ensure the comprehension of the accessibility in python, we can use some conventions. The conventions are:

|Accessibility|Prefix|Example|
|---|---|---|
|Public||`my_var`|
|Protected|`_`|`_my_var`|
|Private|`__`|`__my_var`|

### Module Variables

```python
person_name = 'John Due'  # Public
__person_name = 'John Due'  # Private
```

### Module Constants

```python
PI = 3.14  # Public
__PI = 3.14  # Private
```

### Module Functions

```python
# Public
def calc(x, y):  
    return x + y

# Private
def __calc(x, y):
    return x + y
```

### Module Classes

```python
# Public
class Person:
    pass

# Private
class __Person:
    pass
```

### Class Variables

```python
class Person:
    person_name = 'John Due'  # Public
    _person_name = 'John Due'  # Protected
    __person_name = 'John Due'  # Private
```

### Class Constants

```python
class Math:
    PI = 3.14  # Public
    _PI = 3.14  # Protected
    __PI = 3.14  # Private
```

### Class Attributes

```python
class Person:
    def __init__(self):
        self.name = 'John Due' # Public
        self._name = 'John Due' # Protected
        self.__name = 'John Due' # Private
```

### Class Methods

```python
class Person:
    # Public
    def talk():
        pass

    # Protected
    def _talk():
        pass

    # Private
    def __talk():
        pass
```

## Strings

```python
# Always use single-quote for strings

# Do
name = 'John Due'

# Don't
name = "John Due"
```

## Importation

### Location

```python
# Always import resources at the top of the file, or after the module docstring

# Do
import abc

# Do
"""
Module description...
"""
import abc

# Don't
name = 'John Due'
import abc

# Don't
def main():
    import abc
```

### Multiple Module Imports

```python
# When importing multiple modules, use different lines for each one

# Do
import abc
import sys

# Don't
import abc, sys
```

### Multiple Module Resource Imports

```python
# If the amount of resources that will be imported exceed 79 characters, use multiple line import

# Do
from abc import ABC

# Do
from typing import Final, Union

# Do
from typing import (
    Iterable,
    Final,
    Union,
    Optional,
    NamedTuple,
    ClassVar,
    TYPE_CHECKING,
)

# Don't
from typing import Iterable, Final, Union, Optional, NamedTuple, ClassVar, \
    TYPE_CHECKING
```

### Import Alias

```python
# Try to avoid using alias since it can difficult the understanding

# Do
import sys as system

# Do
from typing import TYPE_CHECKING as TYPE_CHECK

# Don't
from sys as s
```

### Order

```python
# Imports are sorted alphabetically, and should respect the import order
# The order is:
#   1º Module imports
#   2º Resource imports

# Do
import abc
import sys
from math import pi
from typing import (
    Union,
    Final,
)

# Don't
import sys
from typing import (
    Union,
    Final,
)
import abc
from math import pi
```