# Python Style Guide

## Table of Contents

1. [Introduction](#introduction)
2. [Zen of Python](#zen-of-python)
3. [Python Programming Language](#python-programming-language)
4. [PEPs](#peps)
5. [Type Hints](#type-hints)
6. [Style Guide](#style-guide)
7. [Structural Naming Conventions](#structural-naming-conventions)
    1. [Project Name](#project-name)
    2. [Packages](#packages)
    3. [Modules](#modules)
    4. [Main Module](#main-module)
    5. [Test Module](#test-module)
8. [Format Conventions](#format-conventions)
    1. [Line Length 79](#line-length-79)
    2. [Blank Lines](#blank-lines)
    3. [Indentation](#indentation)
    4. [Spaces](#spaces)
    5. [Backslash](#backslash)
    6. [End of File EOF](#end-of-file-eof)
8. [Code Naming Conventions](#code-naming-convetions)
    1. [Variables](#variables)
    2. [Constants](#constants)
    3. [Functions](#functions)
    4. [Parameters](#parameters)
    5. [Classes](#classes)
    6. [Methods](#methods)
    7. [Magic Methods](#magic-methods)
    8. [Test Methods](#test-methods)
    9. [Unused Resources](#unused-resources)
    10. [Errors](#errors)
    11. [Error Alias](#error-alias)
    12. [Reserved Words](#reserved-words)
9. [Access Modifiers](#access-modifiers)
    1. [Module Variables](#module-variables)
    2. [Module Constants](#module-constants)
    3. [Module Functions](#module-functions)
    4. [Module Classes](#module-classes)
    5. [Class Variables](#class-variables)
    6. [Class Constants](#class-constants)
    7. [Class Attributes](#class-attributes)
    8. [Class Methods](#class-methods)
10. [Strings](#strings)
11. [Importation](#importation)
    1. [Import Location](#import-location)
    2. [Multiple Module Imports](#multiple-module-imports)
    3. [Multiple Module Resource Imports](#multiple-module-resource-imports)
    4. [Import Alias](#import-alias)
    5. [Order](#order)
12. [Functions and Methods](#function-and-methods)
    1. [Parameters](#parameters)
    2. [Arguments](#arguments)
    3. [Function and Method Calls](#function-and-method-calls)
    4. [Static Methods](#static-methods)
    5. [Class Methods](#class-methods)
    6. [Instance Methods](#instance-methods)
13. [Documentation](#documentation)
    1. [Inline Comments](#inline-comments)
    2. [Multiple Line Comments](#multiple-line-comments)
    3. [Section Comments](#section-comments)
    4. [Docstrings](#docstrings)
    5. [Docstring Template](#docstring-template)
    6. [Comment Snippets](#comment-snippets)

## Introduction

This Python style guide was made focusing in the essential to create a clean and maintainable code. I really encourage the usage of any style guide, since this guarantees that your code can be easily understood by developers. There are other styles guides made from big projects/companies, and I have to confess that some tips of this style guide was obtained from these documents, but, another tips I created by myself.

Avoid seeing this material as rules for your development, but use this as a convention to standardization. If you prefer to follow your style for coding some specific situation, go ahead! But, I just ask you to check and determine if this style you choose was the best choice, or if there is some situation that it could break somewhere.

[Back to Top](#table-of-contents)

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

[Back to Top](#table-of-contents)

## Python Programming Language

Python is a interpreted programming language that use the tabs or spaces as code blocks. The correct indentation is mandatory, and see this as a good advantage, because you know that for any Python code you see, it will be formatted correctly. If you are new in Python, and never have programmed in this spectacular language, please, take a look in my [Python Guide](https://github.com/vinibiavatti1/PythonGuide), where you can find a pocket documentation with examples that you can use to learn Python easily and faster. 

[Back to Top](#table-of-contents)

## PEPs

In this document I used everything of [PEP8](https://peps.python.org/pep-0008/), and more other styles that there aren't in it. PEP8 is the most known code style for python programmers, so, using this as the base for this style guide can guarantee that everyone can be adapted very well.

For typehints, this style follow the same of [PEP484](https://peps.python.org/pep-0484/) and [PEP526](https://peps.python.org/pep-0526/).

For docstrings, I used some characteristics of [Google Style Guide](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings) and [PEP257](https://peps.python.org/pep-0257/). After comparing some ways to create docstrings using these conventions, I could see improvements and other modifications that could facilitate the documentation of the code. Because of that, I decided to change some of the conventions thinking more in code standardization. Don't forget the zen principle: _Simple is better than complex._

Document the code is extremely important, for the developers and for who will maintain this code in the future. But, we know that it is not everyone that like or can prioritize it, so I focused in the easiest way to avoid giving more work for do it or make it become an _overkill_.

[Back to Top](#table-of-contents)

## Type Hints

All of examples count on type hints. However, you can use this style guide without using type hints, but it is not recommended. Types are always the best option to document the code. _Explicit is better than implicit._. Check [PEP484](https://peps.python.org/pep-0484/) For more details.

[Back to Top](#table-of-contents)

## Style Guide

This style guide is separated by sections, where each section corresponds to good practices for coding in a specific syntax/context. Here you can find naming conventions, indentation tips, comment hints, etc. You can also find reasons for the usage of some style, _do_ and _don'ts_, and examples.

If you have some suggestion/question, be free to open an issue to this repository, and we will evaluate your orders with all of will.

[Back to Top](#table-of-contents)

## Structural Naming Conventions

Structural name conventions are rules for the project structure, like name of modules, packages, and the project name.

### Project Name

> Project root folder

* Use a good representation name
* Use underscore to separate
* Do not use camel case
* Do not use special symbols
* Do not use capital letters

**✅ Do**
```python
my_project
```

**❌ Don't**
```python
myproject
MyProject
```

[Back to Top](#table-of-contents)

### Packages

> Folders with `__init__.py` file.

* Use a good representation name
* Use underscore to separate
* Do not use camel case
* Do not use special symbols
* Do not use capital letters

**✅ Do**
```python
my_package
```

**❌ Don't**
```python
mypackage
MyPackage
```

[Back to Top](#table-of-contents)

### Modules

> Files with `.py` extension.

* Use a good representation name
* Use underscore to separate
* Do not use camel case
* Do not use special symbols
* Do not use capital letters

**✅ Do**
```python
my_module.py
abc_.py
```

**❌ Don't**
```python
mymodule.py
MyModule.py
```

[Back to Top](#table-of-contents)

### Main Module

> Application entry-point file

* Use the `main.py` for the main file

**✅ Do**
```python
main.py
```

**❌ Don't**
```python
app.py
init.py
```

[Back to Top](#table-of-contents)

### Test Module

> Test entry-point file

* Use the `test.py` name for the main test file

**✅ Do**
```python
test.py
```

**❌ Don't**
```python
testing.py
```

[Back to Top](#table-of-contents)

## Format Conventions

For format conventions we see some generic conventions that can be applied for any part of the code. This section counts on the line length rule, spaces, lines, and other formats.

As defined in PEP8, we use 79 characters as the limit for the code lines. Why? Because it facilitate for the developers to read the code. In the first sight it looks strange, but after practicing this convention little by little you will see that the code will look be much better.

### Line Length 79

* Use 79 columns as line length
* Never exceed this length
* Use backslash to wrap the line
* When line wrap, use the same column after declaration for the second line

**✅ Do**
```python
text: str = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. ' \
            'Aliquam a elit nisl.'
```

**❌ Don't**
```python
text: str = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam a elit nisl.'
```

[Back to Top](#table-of-contents)

### Blank Lines

* Use two blank lines to separate imports, functions and classes
* For inside a class, use only one line to separate the methods
* Avoid using unnecessary blank lines 

**✅ Do**
```python
import abc


class Person:
    ...


def main():
    ...


class Person:

    def __init__(self) -> None:
        ...

    def talk(self, message: str) -> None:
        ...
```

**❌ Don't**
```python
import abc
class Person:
    ...
def main():
    ...

class Person:


    def __init__(self) -> None:
        ...


    def talk(self, message: str) -> None:
        ...
```

[Back to Top](#table-of-contents)

### Indentation

* Always use spaces for indentation
* Always use 4 (four) spaces to indent the code

**✅ Do**
```python
if True:
    pass  # 4 spaces (right)
```

**❌ Don't**
```python
if True:
 pass  # 1 space (wrong)
```

[Back to Top](#table-of-contents)

### Inline Expressions

* Never use inline expressions for conditions and loops

**✅ Do**
```python
if True:
    pass

for i in range(10):
    pass
```

**❌ Don't**
```python
if True: pass

for i in range(10): pass
```

[Back to Top](#table-of-contents)

### Spaces

* Do not use unnecessary spaces (Except for inline comments)
* Do not align the content vertically

**✅ Do**
```python
values = [1, 2, 3, 4]

name = 'John'
surname = 'Due'
```

**❌ Don't**
```python
values = [ 1, 2, 3, 4 ]

name    = 'John'
surname = 'Due'
```

[Back to Top](#table-of-contents)

### Backslash

* Use backslash for value data
* Avoid the usage of backslash for other resources like functions params, lists, etc
* Do not use backslash to separate strings inside a dict

**✅ Do**
```python
def calculate_numbers(number_1: int, number_2: int, number_3: int,
                      number_4: int) -> int:
    ...

messages = {
    'lorem': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. '
             'Aliquam a elit nisl.'
}
```

**❌ Don't**
```python
def calculate_numbers(number_1: int, number_2: int, number_3: int, \
                      number_4: int) -> int:
    ...

messages = {
    'lorem': 'Lorem ipsum dolor sit amet, consectetur adipiscing ' \
             'elit. Aliquam a elit nisl.'
}
```

[Back to Top](#table-of-contents)

### End of File EOF

* Always terminate a python file with a blank line

**✅ Do**
```python
exit()
EOF
```

**❌ Don't**
```python
exit() EOF
```

[Back to Top](#table-of-contents)

## Code Naming Conventions

The naming convention follows the same of PEP8. Read this section to check more examples and situations for naming.

### Variables

* Use a good representation name
* Use underscore to separate
* Use the type hint for variables
* Do not use camel case
* Do not use special symbols
* Do not use capital letters

**✅ Do**
```python
person_name: str = 'John Due'
```

**❌ Don't**
```python
person_name = 'John Due'
personName = 'John Due'
personname = 'John Due'
```

[Back to Top](#table-of-contents)

### Constants

* Use a good representation name
* Use underscore to separate
* Use all letters capitalized
* Use type hints
* Do not use special symbols

**✅ Do**
```python
PI: float = 3.14
```

**❌ Don't**
```python
PI = 3.14
pi = 3.14 
```

[Back to Top](#table-of-contents)

### Functions

* Use a good representation name
* Use underscore to separate
* Use type hints
* Do not use camel case
* Do not use special symbols
* Do not use capital letters

**✅ Do**
```python
def sum_numbers(x: int, y: int) -> int:
    ...
```

**❌ Don't**
```python
def sum_numbers(x, y):
    ...

def sumNumbers(x: int, y: int) -> int:
    ...
```

[Back to Top](#table-of-contents)

### Parameters

* Use a good representation name
* Use underscore to separate
* Use type hints
* Do not use camel case
* Do not use special symbols
* Do not use capital letters

**✅ Do**
```python
def multiply(number_1: int, number_2: int) -> int:
    ...
```

**❌ Don't**
```python
def multiply(number1: int, n: int) -> int:
    ...
```

[Back to Top](#table-of-contents)

### Classes

* Use a good representation name
* Use camel case
* Capitalize all letters of an abbreviation
* Do not use underscore to separate
* Do not use special symbols
* Do not use letters to represent the type, like "I" for interface

**✅ Do**
```python
class HTTPServer:
    ...
```

**❌ Don't**
```python
class HttpServer:
    ...

class IClientServer(ABC):
    ...

class ABCClientServer(ABC):
    ...
```

[Back to Top](#table-of-contents)

### Methods

* Use a good representation name
* Use underscore to separate
* Use type hints
* Do not use camel case
* Do not use special symbols
* Instance methods should have their first parameter named 'self'.
* Class methods should have their first parameter named 'cls'
* Static methods don't need to have a default first parameter
* Do not use capital letters

**✅ Do**
```python
class DataProcessor:
    def process_data(self) -> None:
        ...

    @classmethod
    def create(cls) -> 'DataProcessor':
        ...

    @staticmethod
    def version() -> float:
        ...
```

[Back to Top](#table-of-contents)

### Magic Methods

* Use a good representation name
* Use two underscores (aka dunder) "__" as prefix and suffix
* Use underscore to separate
* Use type hints
* Do not use camel case
* Do not use special symbols
* Do not use capital letters

**✅ Do**
```python
class DataProcessor:
    def __init__(self) -> None:
        ...
```

**❌ Don't**
```python
class DataProcessor:
    def init(self) -> None:
        ...
```

[Back to Top](#table-of-contents)

### Test Methods (TestCase)

* Use "test_" as prefix
* Use a good representation name
* Use underscore to separate
* Use type hints
* Do not use camel case
* Do not use special symbols
* Must have their first parameter named 'self'.
* Do not use capital letters

**✅ Do**
```python
class ListTest(unittest.TestCase):
    def test_append(self) -> None:
        ...
```

**❌ Don't**
```python
class ListTest(unittest.TestCase):
    def append(self) -> None:
        ...
```

[Back to Top](#table-of-contents)

### Unused Resources

* Use "_" as name
* If there is other unused variable named "_", append other underscore "__"

**✅ Do**
```python
for _, value in object_map.items():
    ...

for _, inner in object_map.items():
    for __, value in inner.items():
        ...
```

**❌ Don't**
```python
for unused, value in object_map.items():
    ...
```

[Back to Top](#table-of-contents)

### Errors

* Use a good representation name
* Do not use underscore to separate
* Use camel case
* Do not use special symbols
* Do not use letters to represent the type like "E" for Error
* Use the 'Error' suffix in the exception class name
* Extends the Exception class or subclass
* Never extend the "BaseException" class. Use it for an specific situation only

**✅ Do**
```python
class ValidationError(Exception):
    ...
```

**❌ Don't**
```python
class ValidationException(Exception):
    ...

class EValidation(Exception):
    ...
```

[Back to Top](#table-of-contents)

### Error Alias

* Use the 'err' name to reference the error
* When the 'err' name is already used, add an underscore as suffix

**✅ Do**
```python
try:
    ...
except ValueError as err: 
    ...


try:
    ...
except ValueError as err: 
    try:
        ...
    except ValueError as err_: 
        ...
```

**❌ Don't**
```python
try:
    ...
except ValueError as error: 
    ...
```

[Back to Top](#table-of-contents)

### Reserved Words

* Never replace a python reserved word or builtin word as name for any artifact
* Use underscore "_" as suffix
* When the name is already used, add an underscore as suffix

**✅ Do**
```python
from_: str = 'Hello'

def input_(message: str) -> Any:
    ...
```

**❌ Don't**
```python
any: bool = True  # any is a builtin function

def sum(x: int, y: int) -> int:  # sum is a builtin function
    ...
```

[Back to Top](#table-of-contents)

## Access Modifiers

Access Modifiers are the way to determinate the accessibility of the resources in a class or module. Python does't have any consistency validator to check it, only for private resources where it uses [Name Mangling](https://en.wikipedia.org/wiki/Name_mangling) to avoid direct calls. So, to ensure the comprehension of the accessibility in Python, we can use some conventions.In general, we use underscores to define the accessibility of the resource:

|Accessibility|Prefix|Example|
|---|---|---|
|Public||`my_var`|
|Protected|`_`|`_my_var`|
|Private|`__`|`__my_var`|

### Module Variables

**✅ Do**
```python
person_name: str = 'John Due'  # Public
__person_name: str = 'John Due'  # Private
```

[Back to Top](#table-of-contents)

### Module Constants

**✅ Do**
```python
PI: float = 3.14  # Public
__PI: float = 3.14  # Private
```

[Back to Top](#table-of-contents)

### Module Functions

**✅ Do**
```python
# Public
def calc(x: int, y: int) -> int:  
    ...

# Private
def __calc(x: int, y: int) -> int:
    ...
```

[Back to Top](#table-of-contents)

### Module Classes

**✅ Do**
```python
# Public
class Person:
    ...

# Private
class __Person:
    ...
```

[Back to Top](#table-of-contents)

### Class Variables

**✅ Do**
```python
class Person:
    person_name: str = 'John Due'  # Public
    _person_name: str = 'John Due'  # Protected
    __person_name: str = 'John Due'  # Private
```

[Back to Top](#table-of-contents)

### Class Constants

**✅ Do**
```python
class Math:
    PI: float = 3.14  # Public
    _PI: float = 3.14  # Protected
    __PI: float = 3.14  # Private
```

[Back to Top](#table-of-contents)

### Class Attributes

**✅ Do**
```python
class Person:
    def __init__(self):
        self.name: str = 'John Due' # Public
        self._name: str = 'John Due' # Protected
        self.__name: str = 'John Due' # Private
```

[Back to Top](#table-of-contents)

### Class Methods

**✅ Do**
```python
class Person:
    # Public
    def talk() -> None:
        ...

    # Protected
    def _talk() -> None:
        ...

    # Private
    def __talk() -> None:
        ...
```

[Back to Top](#table-of-contents)

## Strings

* Always use single quotes `''` for strings

**✅ Do**
```python
name: str = 'John Due'
```

**❌ Don't**
```python
name: str = "John Due"  # Used double quotes
```

[Back to Top](#table-of-contents)

## Importation

In this section conventions for module and package importation will be declared to facilitate the organization and the comprehension of the code.

### Import Location

* Always import resources at the top of the file, after the module docstring

**✅ Do**
```python
"""
Module description...
"""
import abc
```

**❌ Don't**
```python
name = 'John Due'
import abc

def main():
    import functools
```

[Back to Top](#table-of-contents)

### Multiple Module Imports

* When importing multiple modules, use different lines for each one

**✅ Do**
```python
import abc
import sys
```

**❌ Don't**
```python
import abc, sys
```

[Back to Top](#table-of-contents)

### Multiple Module Resource Imports

* If the amount of resources pass 2 (two) imports, or exceeds the line length, use multiple line imports

**✅ Do**
```python
from typing import (
    Iterable,
    Final,
    Union,
    Optional,
    NamedTuple,
    ClassVar,
    TYPE_CHECKING,
)
```

**❌ Don't**
```python
from typing import Iterable, Final, Union, Optional, NamedTuple, ClassVar, \
    TYPE_CHECKING
```

[Back to Top](#table-of-contents)

### Import Alias

* Try to avoid using alias since it can difficult the understanding of the imported resource usage
* If it is needed, use good representation names, not acronyms 

**✅ Do**
```python
import sys as system

from typing import TYPE_CHECKING as TYPE_CHECK
```

**❌ Don't**
```python
from sys as s

from typing import TYPE_CHECKING as TC
```

[Back to Top](#table-of-contents)

### Order

* Imports are sorted alphabetically, and should respect the import order
* The order is:
    * 1º Module imports
    * 2º Resource imports

**✅ Do**
```python
import abc
import sys
from math import pi
from typing import (
    Union,
    TYPE_CHECKING as TYPE_CHECK,
)
```

**❌ Don't**
```python
import sys
from typing import (
    Union,
    TYPE_CHECKING as TYPE_CHECK,
)
import abc
from math import pi
```

[Back to Top](#table-of-contents)

## Functions and Methods

Some conventions will be applied for function and methods, to make some consistency for organization, line breaks and alignments.

### Parameters

* When some function exceeds the line length, use break-line
* Adjust the next line params to the same position of first line params
* Never keep the parameter with the type hint in other line 
* When only the return type hint exceeds the line length, break only the return type hint with the parenthesis

**✅ Do**
```python
def calculate_numbers(number_1: float, number_2: float, number_3: float,                
                      number_6: float) -> float:
    ...

def calculate_numbers(number_1: float, number_2: float, number_3: float                
                      ) -> float:
    ...
```

**❌ Don't**
```python
def calculate_numbers(number_1: float, number_2: float, number_3: float,                
    number_6: float) -> float:
    ...

def calculate_numbers(number_1: float, number_2: float, number_3: \
                      float, number_6: float) -> float:
    ...

def calculate_numbers(
    number_1: float, 
    number_2: float, 
    number_3: float,                
    ) -> float:
    ...
```

[Back to Top](#table-of-contents)

### Arguments

* When some function call exceeds the line length, use break-line
* Adjust the next line args to the same position of first line args

**✅ Do**
```python
function('argument1', 'argument2', 'argument3', 'argument4', 'argument5',
         'argument6', 'argument7')
```

**❌ Don't**
```python
function('argument1', 'argument2', 'argument3', 'argument4', 'argument5',
    'argument6', 'argument7')

function(
    'argument1', 
    'argument2', 
    'argument3',
)
```

[Back to Top](#table-of-contents)

### Function and Method Calls

* When some function call exceeds the line length, use break-line
* Put arguments in the next line when function exceed the line length

**✅ Do**
```python
big_function_name_that_almost_exceed_the_line_length_and_has_a_big_name(
    'argument1', 'argument2', 'argument3',
)
```

**❌ Don't**
```python
big_function_name_that_almost_exceed_the_line_length_and_has_a_big_name(
    'argument1', 
    'argument2', 
    'argument3',
)
```

[Back to Top](#table-of-contents)

### Static Methods

* Use the @staticmethod decorator

**✅ Do**
```python
class Person:
    @staticmethod
    def version(type_: int) -> int:
        ...
```

[Back to Top](#table-of-contents)

### Class Methods

* Always use "cls" as the first argument
* Use the @classmethod decorator
* Do not need to set type hint for "cls" variable

**✅ Do**
```python
class Person:
    @classmethod
    def create(cls, name: str) -> 'Person':
        ...
```

[Back to Top](#table-of-contents)

### Instance Methods

* Always use "self" as the first argument
* Do not need to set type hint for "self" variable

**✅ Do**
```python
class Person:
    def talk(self, message: str) -> None:
        pass
```

[Back to Top](#table-of-contents)

## Documentation

In Python we have three types of comments that can be used into Python code: inline Comments, multiple line comments and docstrings. We use these comments to document the code for more readability, or to help the developers about some complex routine. 

### Inline Comments

* Use one space after the `#` (number sign)
* After expressions, use two spaces to separate the code and the comment
* Never exceed the 79 line length
* If the line length will be exceeded, create other inline comment below
* To describe a function, method, or a class, use docstrings

**✅ Do**
```python
values = [1, 2, 3]  # Important values

# Check some important thing
if True:
    pass
```

**❌ Don't**`
```python
values = [1, 2, 3] #Important values
values = [1, 2, 3] # Important values (without 2 spaces)

# Main function (use docstring in this case)
def main():
    ...
```

[Back to Top](#table-of-contents)

### Multiple Line Comments

* Avoid to use multiple line comments. Use multiple [inline comments](#inline-comments) if it is possible, or, use docstrings to document modules, classes, functions and methods

**✅ Do**
```python
# Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi feugiat nisi
# non quam facilisis vehicula. In hac habitasse platea dictumst. Cras
# maximus dolor et nunc consectetur, sed commodo nisi blandit.
```

**❌ Don't**`
```python
"""
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi feugiat nisi non quam facilisis vehicula. In hac habitasse platea dictumst. Cras maximus dolor et nunc consectetur, sed commodo nisi blandit.
"""
```

[Back to Top](#table-of-contents)

### Section Comments

* Use `#` (number sign) to make section comments lines
* Use the first and an end line full with `#` (number sign)
* Respect the indentation 

> HINT: Use the [Comment Snippets](#comment-snippets) to facilitate the creation of section comments

**✅ Do**
```python
###############################################################################
# Section Comment
###############################################################################

class Person:

    ###########################################################################
    # Section Comment
    ###########################################################################
    
    def __init__(self):
        ...
```

**❌ Don't**`
```python
# -----------------------------------------------------------------------------
# Section Comment
# -----------------------------------------------------------------------------

"""
Section Comment
"""

"""
###############################################################################
Section Comment
###############################################################################
"""

class Person:

###############################################################################
# Section Comment
###############################################################################
    
    def __init__(self):
        ...
```

[Back to Top](#table-of-contents)

### Docstrings

* Use double quote `""` for docstrings
* Always finish the line with period `.`
* Always break the first and the end line `"""\n<doc>\n"""`. This makes better to edit the docstring. If you want to process the docstring in your code, you can `strip()` the content to remove the break lines.
* Try to always use docstrings to document your code for modules, functions, methods and classes
* Use only relevant content in docstrings. If you don't need to document the parameters of a function for example, don't do it. 
* If you use docstring for an empty class, function or method, don't use ellipses `...` or the `pass` keyword. It is not necessary
* Do not create blank lines between the documented resource and the docstring

> You can use the [docstring template](#docstring-template) to facilitate the creation of the docstring

**✅ Do**
```python
"""
Module description.
"""


def function() -> None:
    """
    Function description.
    """


class Person:
    """
    Class description.
    """

    def method(self) -> None:
        """
        Method description.
        """
```

**❌ Don't**
```python
def function() -> None:
    """Function description."""

def function() -> None:
    """Function description.
    """

def function() -> None:  # Without line period
    """
    Function description
    """

def function() -> None:  # Blank line between the resource and the docstring

    """
    Function description
    """
```

[Back to Top](#table-of-contents)

### Docstring Template

* Remove the content that will not be used
* Try to always follow this template to keep the same organization

`Docstring Template`
```python
"""
Summary of the resource here.

Attributes:
    name: Class attribute description here

Args:
    value: Positional argument description with some information and with
        break line for multi-line description.
    *values: Arbitraty argument description.
    **kwvalue: Keyword argument description.

Returns:
    Return type description.

Yields:
    Return type description used when the function is a generator.

Raises:
    IOError: Error description and some information.

Examples:
    Sum two integer or float numbers and returns the result
    add(1, 3) -> 4

See Also:
    math.pi: Example of module constant documentation.

Notes:
    Some notes here.

Authors:
    John Due: john.due@email.com

References:
    Python website: https://www.python.org/

Tests:
    Sum two integer or float numbers and returns the result
    >>> add(1, 3)
    4
"""
```

[Back to Top](#table-of-contents)

### Comment Snippets

If you are using [VSCode](https://code.visualstudio.com/) as the IDE for the development, you can use some snippets to facilitate the generation of docstrings and section comments. 

To create a snippet, just create a file with the name `python.code-snippets.json` into `.vscode` folder with the content below. After configure it, you can start using the snippets following table:

|Snippet|Description|
|---|---|
|`""`|Docstring Comment|
|`##`|Section Comment|
|`###`|Sub Section Comment|

`python.code-snippets.json`

```json
{
    "Docstring Comment": {
        "scope": "python",
        "prefix": "\"\"",
        "body": [
            "\"\"\"",
            "${1:comment}",
            "\"\"\""
        ],
        "description": "Create a docstring comment"
    },
    "Section Comment": {
        "scope": "python",
        "prefix": "##",
        "body": [
            "###############################################################################",
            "# ${1:comment}",
            "###############################################################################"
        ],
        "description": "Create a top-level section comment"
    },
    "Sub Section Comment": {
        "scope": "python",
        "prefix": "###",
        "body": [
            "###########################################################################",
            "# ${1:comment}",
            "###########################################################################"
        ],
        "description": "Create a second-level section comment"
    }
}
```

[Back to Top](#table-of-contents)