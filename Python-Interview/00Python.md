

---
---

---
---

## Python Topics :

### **Python Basics:**
1. **Syntax and Semantics**
   - Python Interpreter
   - Python Environment Setup
   - Python Code Structure (Indentation, Comments)
   - Variables and Data Types
   - Print Statements
   - Input from User

2. **Operators:**
   - Arithmetic Operators
   - Comparison Operators
   - Logical Operators
   - Assignment Operators
   - Bitwise Operators
   - Membership Operators (`in`, `not in`)
   - Identity Operators (`is`, `is not`)

3. **Data Types:**
   - Numbers (int, float, complex)
   - Strings
   - Lists
   - Tuples
   - Sets
   - Dictionaries
   - Boolean

4. **Control Flow:**
   - If-else Conditions
   - For Loops
   - While Loops
   - Nested Loops
   - `break`, `continue`, `pass` statements

5. **Functions:**
   - Defining Functions
   - Function Parameters and Arguments
   - Return Statements
   - Lambda Functions
   - Recursion
   - Scope of Variables (`global`, `local`, `nonlocal`)

6. **Exception Handling:**
   - `try`, `except`, `finally` blocks
   - Raising Exceptions
   - Custom Exceptions
   - `else` in exception handling

### **Intermediate Python Topics:**

7. **Data Structures and Algorithms:**
   - Lists, Tuples, Dictionaries, Sets: Operations and Methods
   - Sorting, Searching, Merging
   - Stack, Queue, Linked List (implementations)
   - Trees, Graphs (basics)
   - Recursion
   - Time Complexity (Big O notation basics)

8. **Comprehensions:**
   - List Comprehension
   - Dictionary Comprehension
   - Set Comprehension
   - Generator Comprehension

9. **File Handling:**
   - Opening Files: `open()`
   - Reading and Writing Files
   - File Modes (`r`, `w`, `a`, `rb`, `wb`)
   - Context Manager (`with` statement)
   - Working with Text and Binary Files
   - CSV File Handling

10. **Modules and Packages:**
    - Importing Modules
    - Standard Library Modules (`math`, `random`, `datetime`, etc.)
    - Writing Custom Modules
    - Packages and `__init__.py`
    - Installing and using third-party packages with `pip`

11. **Object-Oriented Programming (OOP):**
    - Classes and Objects
    - Constructors and Destructors (`__init__()`, `__del__()`)
    - Instance Variables and Class Variables
    - Methods (Instance Methods, Class Methods, Static Methods)
    - Inheritance
    - Encapsulation
    - Polymorphism (Method Overloading, Method Overriding)
    - Abstraction
    - Special Methods (`__str__()`, `__repr__()`, `__len__()`, etc.)

12. **Decorators:**
    - Function Decorators
    - Class Decorators
    - `@staticmethod`, `@classmethod`

13. **Iterators and Generators:**
    - Iterators: `__iter__()`, `__next__()`
    - Generators: `yield` keyword
    - Generator Expressions

14. **Regular Expressions (RegEx):**
    - `re` module
    - Pattern Matching
    - Search, Match, Findall
    - Substitution (`sub`)
    - Grouping and Splitting

### **Advanced Python Topics:**

15. **Functional Programming:**
    - `map()`, `filter()`, `reduce()`
    - Lambda Functions
    - Closures
    - Higher-Order Functions
    - `functools` module (`partial`, `wraps`, etc.)

16. **Concurrency:**
    - Multithreading
    - Multiprocessing
    - Global Interpreter Lock (GIL)
    - `threading` and `multiprocessing` module
    - `asyncio` (Asynchronous Programming)
    - Coroutines

17. **Networking and Socket Programming:**
    - `socket` module
    - TCP/UDP Sockets
    - Client-Server Communication
    - HTTP Requests using `requests` module

18. **Database Interaction:**
    - SQLite with `sqlite3`
    - MySQL, PostgreSQL with `mysql-connector`, `psycopg2`
    - ORM (Object Relational Mapping) using SQLAlchemy
    - Database Transactions

19. **Web Development with Python:**
    - Flask (Micro Web Framework)
    - Django (Full-Stack Web Framework)
    - URL Routing, Templates, Forms, and Views
    - REST APIs using Flask/Django REST Framework
    - Templating Languages: Jinja2

20. **Testing:**
    - Unit Testing with `unittest`, `pytest`
    - Mocking
    - Test-Driven Development (TDD)
    - Automation Testing with `selenium`

21. **Data Serialization:**
    - JSON: `json` module
    - XML: `xml.etree.ElementTree`
    - CSV: `csv` module
    - Pickle: `pickle` module
    - YAML Parsing

22. **Memory Management:**
    - Garbage Collection
    - `gc` module
    - Memory Profiling (`tracemalloc`, `memory_profiler`)

23. **Metaprogramming:**
    - Metaclasses
    - Dynamic Class Creation
    - Reflection using `getattr()`, `setattr()`, `hasattr()`
    - Monkey Patching

24. **Type Hints and Annotations:**
    - Static Typing with `typing` module
    - Type Annotations
    - `mypy` for type checking

25. **File and Directory Management:**
    - `os` module
    - File paths, Directory handling, `os.walk()`
    - Working with Paths using `pathlib`

### **Specialized Topics in Python:**

26. **Data Science and Machine Learning:**
    - NumPy (Numerical Computation)
    - Pandas (Data Manipulation)
    - Matplotlib and Seaborn (Data Visualization)
    - Scikit-learn (Machine Learning)
    - TensorFlow, PyTorch (Deep Learning)

27. **Web Scraping:**
    - BeautifulSoup
    - Scrapy
    - Selenium for dynamic content scraping

28. **GUI Development:**
    - Tkinter (Standard Python GUI)
    - PyQt5, Kivy (Advanced GUI Frameworks)

29. **Game Development:**
    - Pygame

30. **Deployment and Environment:**
    - Virtual Environments (`venv`, `virtualenv`)
    - Dockerizing Python Applications
    - Deploying on Cloud (AWS, Heroku)
    - CI/CD Pipelines with Python (GitHub Actions, Jenkins)

31. **Security:**
    - Cryptography (`cryptography` module)
    - Hashing and Encryption
    - Secure Password Handling
    - JWT (JSON Web Tokens)

32. **Machine Learning and AI:**
    - Libraries: TensorFlow, Keras, PyTorch
    - Data Preprocessing
    - Model Building and Training
    - Neural Networks and Deep Learning

### **Miscellaneous:**

33. **Design Patterns:**
    - Singleton, Factory, Observer, Decorator Patterns

34. **Advanced Libraries:**
    - OpenCV (Image Processing)
    - PyPDF2 (PDF Handling)
    - PIL (Image Processing)
    - PyAutoGUI (Automation)

35. **Python in Embedded Systems:**
    - MicroPython
    - CircuitPython
    - Raspberry Pi with Python

---
---



## In Python, **Magic Methods** (ya "Dunder Methods") 
wo special methods hain jo double underscores (`__`) ke saath start aur end hote hain. Ye methods predefined hote hain Python ke built-in classes mein aur inka major use **operator overloading** ke liye hota hai. "Dunder" ka matlab "Double Under (Underscores)" hota hai.

### Magic Methods ko Kaise Dekhein
Kisi bhi class ke inherited magic methods ko dekhne ke liye `dir()` function use kar sakte hain:

```python
print(dir(int))
```

Ye code `int` class ke magic methods ko list karega.

Ya cmd/terminal pe Python console open karke `dir(int)` type kar sakte hain:

```python
>>> dir(int)
```

### Magic Methods in Python
Python mein kuch commonly used magic methods aur unke uses neeche diye gaye hain:

---

#### **Initialization and Construction**
- **`__new__`**: Object ki instantiation pe call hota hai.
- **`__init__`**: `__new__` ke baad initialize karta hai object ko.
- **`__del__`**: Destructor ka kaam karta hai jo object destroy hone par call hota hai.

#### **Numeric Magic Methods**
- **`__trunc__`**: `math.trunc()` ke behavior ko implement karta hai.
- **`__ceil__`**: `math.ceil()` ke behavior ko implement karta hai.
- **`__floor__`**: `math.floor()` ke behavior ko implement karta hai.
- **`__round__(self, n)`**: `round()` ke behavior ko define karta hai.
- **`__invert__`**: Inversion behavior ko `~` operator ke liye implement karta hai.
- **`__abs__`**: `abs()` function ke behavior ko implement karta hai.
- **`__neg__`**: Negation ke behavior ko define karta hai.
- **`__pos__`**: Unary positive ke behavior ko define karta hai.

#### **Arithmetic Operators**
- **`__add__`**: `+` operator ke liye behavior define karta hai (addition).
- **`__sub__`**: `-` operator ke liye behavior define karta hai (subtraction).
- **`__mul__`**: `*` operator ke liye behavior define karta hai (multiplication).
- **`__floordiv__`**: `//` operator ke liye behavior define karta hai (floor division).
- **`__truediv__`**: `/` operator ke liye behavior define karta hai (true division).
- **`__mod__`**: `%` operator ke liye behavior define karta hai (modulus).
- **`__divmod__`**: `divmod()` function ke behavior ko implement karta hai.
- **`__pow__`**: `**` operator ke liye behavior define karta hai (exponentiation).
- **`__lshift__`**, **`__rshift__`**: Bitwise shift operators `<<` aur `>>` ke behavior ko implement karte hain.
- **`__and__`**, **`__or__`**, **`__xor__`**: Bitwise AND, OR aur XOR operators `&`, `|`, `^` ke behavior ko implement karte hain.
- **`__invert__`**: Bitwise NOT operator `~` ke behavior ko define karta hai.
- **`__neg__`** aur **`__pos__`**: Unary negation aur unary positive operators ko handle karte hain.

#### **String Magic Methods**
- **`__str__`**: `str()` call hone par instance ka readable string representation return karta hai.
- **`__repr__`**: `repr()` ka machine-readable representation return karta hai.
- **`__unicode__`**: Unicode string representation return karta hai.
- **`__format__`**: Custom formatting provide karta hai.
- **`__hash__`**: Hashing ke liye integer return karta hai (dictionaries mein fast key comparison ke liye).
- **`__nonzero__`** (ya `__bool__` in Python 3): `bool()` call hone par instance ka boolean value return karta hai.
- **`__dir__`**: Class ke attributes ki list return karta hai.
- **`__sizeof__`**: Object ka size return karta hai.

#### **Comparison Magic Methods**
- **`__eq__`**: Equality operator `==` ka behavior define karta hai.
- **`__ne__`**: Inequality operator `!=` ka behavior define karta hai.
- **`__lt__`**, **`__gt__`**: Less-than `<` aur greater-than `>` operators ke behavior ko define karte hain.
- **`__le__`**, **`__ge__`**: Less-than-or-equal-to `<=` aur greater-than-or-equal-to `>=` operators ke behavior ko define karte hain.

Ye magic methods Python ke objects ko more functional aur expressive banate hain aur kisi bhi object ke behavior ko customize karna aasaan bana dete hain.

---
---







---
---



| **Category**                     | **Concepts/Modules**                                                                                                            |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Core Concepts**                | Variables, Data Types (int, float, str, list, dict, set, tuple), Control Flow (if, elif, else), Loops (for, while), Functions (def, lambda), Scope, List Comprehensions |
| **Data Structures**              | Lists, Tuples, Sets, Dictionaries, Arrays (using `array` module), Stacks, Queues, Linked Lists, Heaps                             |
| **Modules and Packages**         | Importing modules (import, from ... import), Creating packages, `__init__.py`, pip (Package Installer), virtualenv, requirements.txt  |
| **File Handling**                | Open/Close Files, Read/Write Methods (read(), write(), readline(), readlines()), File Modes (r, w, a, r+, w+, b), Context Managers (`with` statement) |
| **Error Handling**               | Try-Except Blocks, Finally Clause, Raising Exceptions (raise), Custom Exceptions, Assertions                                     |
| **Built-in Functions**           | `print()`, `len()`, `type()`, `int()`, `float()`, `str()`, `list()`, `dict()`, `set()`, `tuple()`, `map()`, `filter()`, `zip()`, `sum()`, `any()`, `all()` |
| **Object-Oriented Programming**  | Classes, Objects, Inheritance, Encapsulation, Polymorphism, Method Overriding, Magic Methods (dunder methods)                    |
| **Functional Programming**       | First-Class Functions, Higher-Order Functions, `map()`, `filter()`, `reduce()`, Lambda Functions                                   |
| **Regular Expressions**          | `re` module, Patterns, Search, Match, Substitute, Split                                                                         |
| **Modules for Data Science**     | NumPy, Pandas, Matplotlib, Seaborn, SciPy, Scikit-learn, Statsmodels, TensorFlow, PyTorch                                         |
| **Web Development**              | Flask, Django, FastAPI, Requests, BeautifulSoup, Jinja2, SQLAlchemy                                                              |
| **Networking**                   | `socket` module, HTTP Requests (using `requests`), `http.server`, `urllib`, WebSockets (using `websockets` library)             |
| **Database Connectivity**        | SQLite (using `sqlite3`), MySQL (using `mysql-connector`), PostgreSQL (using `psycopg2`), ORM (SQLAlchemy, Django ORM)           |
| **Testing**                      | `unittest`, `pytest`, `doctest`, Mocking (using `unittest.mock`), Assertions                                                    |
| **Concurrency and Parallelism**  | Threads (using `threading`), Multiprocessing (using `multiprocessing`), AsyncIO, Coroutines (using `async` and `await`)          |
| **Logging**                      | `logging` module, Log Levels (DEBUG, INFO, WARNING, ERROR, CRITICAL), Custom Logging Handlers                                   |
| **Configuration Management**     | Environment Variables (using `os.environ`), `.env files` (using `python-dotenv`)                                                |
| **Web Scraping**                 | `BeautifulSoup`, `requests`, `Scrapy`, `lxml`                                                                                  |
| **API Development**              | REST APIs (using Flask or Django REST Framework), GraphQL (using Graphene), JSON Handling (using `json` module)                 |
| **Security**                     | Hashing (using `hashlib`), Encryption (using `cryptography`), JWT (using `PyJWT`), Secure Connections (SSL)                     |
| **Machine Learning**             | Scikit-learn, TensorFlow, Keras, PyTorch, Model Training and Evaluation, Data Preprocessing                                     |
| **Data Visualization**           | Matplotlib, Seaborn, Plotly, Bokeh, Dash                                                                                       |
| **Scientific Computing**         | NumPy, SciPy, SymPy, Matplotlib                                                                                                  |
| **GUI Development**              | Tkinter, PyQt, Kivy, wxPython                                                                                                   |
| **Scripting and Automation**     | Writing scripts, using `os` and `shutil` modules, Task Scheduling (using `schedule`, `APScheduler`)                            |
| **Version Control**              | Git (using `gitpython`), Command Line Integration                                                                               |
| **Development Tools**            | Jupyter Notebook, Anaconda, Integrated Development Environments (IDEs) like PyCharm, VS Code                                   |
| **Code Quality and Formatting**  | PEP 8, `black`, `flake8`, `pylint`, Type Checking (using `mypy`), Docstring Standards                                           |


---
---
Here’s a comprehensive list of Python keywords, built-in functions, standard library modules, and commonly used concepts, organized into a table format:

| **Category**                     | **Python Words**                                                                                                             |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Keywords**                     | `False`, `None`, `True`, `and`, `as`, `assert`, `async`, `await`, `break`, `class`, `continue`, `def`, `del`, `elif`, `else`, `except`, `finally`, `for`, `from`, `global`, `if`, `import`, `in`, `is`, `lambda`, `nonlocal`, `not`, `or`, `pass`, `raise`, `return`, `try`, `while`, `with`, `yield` |
| **Built-in Functions**           | `abs()`, `all()`, `any()`, `ascii()`, `bin()`, `bool()`, `breakpoint()`, `bytearray()`, `bytes()`, `callable()`, `chr()`, `classmethod()`, `compile()`, `complex()`, `copyright()`, `copyright()`, `delattr()`, `dict()`, `dir()`, `divmod()`, `enumerate()`, `eval()`, `exec()`, `exit()`, `filter()`, `float()`, `format()`, `frozenset()`, `getattr()`, `globals()`, `hasattr()`, `hash()`, `help()`, `hex()`, `id()`, `input()`, `int()`, `isinstance()`, `issubclass()`, `iter()`, `len()`, `license()`, `list()`, `locals()`, `map()`, `max()`, `memoryview()`, `min()`, `next()`, `object()`, `oct()`, `open()`, `ord()`, `pow()`, `print()`, `property()`, `quit()`, `range()`, `repr()`, `reversed()`, `round()`, `set()`, `setattr()`, `slice()`, `sorted()`, `staticmethod()`, `str()`, `sum()`, `super()`, `tuple()`, `type()`, `vars()`, `zip()` |
| **Exception Types**              | `ArithmeticError`, `AttributeError`, `BufferError`, `EOFError`, `ImportError`, `IndexError`, `KeyError`, `KeyboardInterrupt`, `MemoryError`, `NameError`, `OSError`, `OverflowError`, `ReferenceError`, `RuntimeError`, `StopIteration`, `SyntaxError`, `TypeError`, `ValueError`, `Warning` |
| **Data Types**                   | `int`, `float`, `str`, `list`, `tuple`, `set`, `dict`, `bool`, `NoneType`                                                  |
| **Standard Library Modules**     | `os`, `sys`, `math`, `random`, `datetime`, `time`, `re`, `json`, `csv`, `sqlite3`, `collections`, `itertools`, `functools`, `multiprocessing`, `threading`, `http`, `urllib`, `requests`, `BeautifulSoup`, `Flask`, `Django` |
| **Control Flow Statements**      | `if`, `elif`, `else`, `for`, `while`, `break`, `continue`, `pass`, `try`, `except`, `finally`, `raise`                  |
| **Built-in Constants**           | `True`, `False`, `None`, `NotImplemented`, `Ellipsis`, `__debug__`                                                          |
| **Magic Methods**                | `__init__`, `__str__`, `__repr__`, `__len__`, `__getitem__`, `__setitem__`, `__delitem__`, `__iter__`, `__next__`, `__call__`, `__add__`, `__sub__`, `__mul__`, `__truediv__`, `__floordiv__`, `__mod__`, `__pow__`, `__lt__`, `__le__`, `__eq__`, `__ne__`, `__gt__`, `__ge__`, `__contains__`, `__enter__`, `__exit__` |
| **File Handling Modes**          | `r` (read), `w` (write), `a` (append), `r+` (read and write), `b` (binary)                                               |
| **Common Libraries for Data Science** | `NumPy`, `Pandas`, `Matplotlib`, `Scikit-learn`, `SciPy`, `TensorFlow`, `Keras`, `PyTorch`                           |
| **Common Libraries for Web Development** | `Flask`, `Django`, `Requests`, `BeautifulSoup`, `SQLAlchemy`                                                      |
| **Common Testing Libraries**     | `unittest`, `pytest`, `doctest`, `mock`, `coverage`, `hypothesis`                                                         |
| **Common GUI Frameworks**        | `Tkinter`, `PyQt`, `Kivy`, `wxPython`                                                                                     |
| **Common Tools for Virtual Environments** | `venv`, `virtualenv`, `conda`                                                                                        |
| **Common Code Quality Tools**    | `pylint`, `flake8`, `black`, `mypy`                                                                                       |

This table provides a detailed overview of various Python-related terms and functionalities. If you need more information on any specific category or term, feel free to ask!




---
---
Here's a table of commonly used Python keywords and built-in functions. Python keywords are reserved words that have special meaning in the language and cannot be used as identifiers. Built-in functions are available by default in Python.

### Python Keywords

| Keyword       | Description                                      |
|---------------|--------------------------------------------------|
| `False`       | Boolean value representing false                 |
| `None`        | Represents the absence of a value                |
| `True`        | Boolean value representing true                  |
| `and`         | Logical AND operator                             |
| `as`          | Used to create an alias                           |
| `assert`      | Used for debugging; tests a condition           |
| `async`       | Used to declare an asynchronous function          |
| `await`       | Used to call an asynchronous function            |
| `break`       | Exits a loop                                     |
| `class`       | Defines a class                                  |
| `continue`    | Continues to the next iteration of a loop       |
| `def`         | Defines a function                               |
| `del`         | Deletes a reference to an object                 |
| `elif`        | Used in conditional statements (else if)       |
| `else`        | Defines an alternative condition                  |
| `except`      | Used to catch exceptions                          |
| `finally`     | A block of code that runs after try/except      |
| `for`         | Used to create a for loop                        |
| `from`        | Imports specific parts of a module              |
| `global`      | Declares a global variable                       |
| `if`          | Used for conditional statements                   |
| `import`      | Imports a module                                 |
| `in`          | Tests for membership                             |
| `is`          | Tests for object identity                        |
| `lambda`      | Creates an anonymous function                     |
| `nonlocal`    | Declares a non-local variable                   |
| `not`         | Logical NOT operator                             |
| `or`          | Logical OR operator                              |
| `pass`        | A null statement, does nothing                  |
| `raise`       | Raises an exception                              |
| `return`      | Exits a function and returns a value            |
| `try`         | Specifies exception handling                     |
| `while`       | Creates a while loop                             |
| `with`        | Used to wrap the execution of a block           |
| `yield`       | Used to make a generator function                |

### Python Built-in Functions

| Function          | Description                                      |
|-------------------|--------------------------------------------------|
| `abs()`           | Returns the absolute value of a number          |
| `all()`           | Returns True if all elements of an iterable are true |
| `any()`           | Returns True if any element of an iterable is true |
| `bin()`           | Converts an integer to a binary string          |
| `bool()`          | Converts a value to a Boolean                   |
| `bytearray()`     | Returns a new array of bytes                    |
| `bytes()`         | Returns a new "bytes" object                    |
| `callable()`      | Checks if the object appears callable           |
| `chr()`           | Converts an integer to a character              |
| `classmethod()`   | Transforms a method into a class method         |
| `compile()`       | Compiles source into a code object              |
| `complex()`       | Creates a complex number                         |
| `delattr()`       | Deletes an attribute from an object             |
| `dict()`          | Creates a dictionary                             |
| `dir()`           | Returns a list of attributes and methods        |
| `divmod()`        | Returns the quotient and remainder               |
| `enumerate()`     | Returns an enumerate object                     |
| `eval()`          | Evaluates a string as a Python expression       |
| `exec()`          | Executes the Python code in the given string    |
| `filter()`        | Constructs an iterator from elements of an iterable |
| `float()`         | Converts a value to a floating point number     |
| `format()`        | Formats a specified value                        |
| `frozenset()`     | Returns a frozenset object                      |
| `getattr()`       | Returns the value of a named attribute          |
| `globals()`       | Returns a dictionary representing the current global symbol table |
| `hasattr()`       | Checks if an object has a named attribute       |
| `hash()`          | Returns the hash value of an object             |
| `help()`          | Invokes the built-in help system                |
| `id()`            | Returns the identity of an object               |
| `input()`         | Reads a line from input                          |
| `int()`           | Converts a value to an integer                  |
| `isinstance()`    | Checks if an object is an instance of a class   |
| `issubclass()`    | Checks if a class is a subclass of another      |
| `len()`           | Returns the length of an object                 |
| `list()`          | Creates a list                                  |
| `locals()`        | Returns a dictionary representing the current local symbol table |
| `map()`           | Applies a function to all items in an iterable   |
| `max()`           | Returns the largest item in an iterable         |
| `memoryview()`    | Returns a memory view object                    |
| `min()`           | Returns the smallest item in an iterable        |
| `next()`          | Retrieves the next item from an iterator        |
| `object()`        | Returns a new featureless object                |
| `oct()`           | Converts an integer to an octal string          |
| `open()`          | Opens a file and returns a file object         |
| `ord()`           | Converts a character to its integer value       |
| `pow()`           | Returns the value of x to the power of y       |
| `print()`         | Prints the specified message to the screen      |
| `property()`      | Returns a property attribute                     |
| `range()`         | Returns a sequence of numbers                   |
| `repr()`          | Returns a string representing an object         |
| `reversed()`      | Returns a reversed iterator                     |
| `round()`         | Rounds a number to a specified number of decimals |
| `set()`           | Creates a set                                   |
| `setattr()`       | Sets the value of a named attribute             |
| `slice()`         | Returns a slice object                          |
| `sorted()`        | Returns a sorted list                           |
| `staticmethod()`  | Transforms a method into a static method       |
| `str()`           | Converts an object to a string                  |
| `sum()`           | Sums the items of an iterable                   |
| `super()`         | Returns a proxy object that delegates method calls to a parent or sibling class |
| `tuple()`         | Creates a tuple                                 |
| `type()`          | Returns the type of an object                   |
| `vars()`          | Returns the `__dict__` attribute for a module, class, instance, or any other object |
| `zip()`           | Returns an iterator of tuples                   |



---
---


















---
---




---
---
