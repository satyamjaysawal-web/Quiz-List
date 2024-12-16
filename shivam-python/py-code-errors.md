## List of common Python errors with examples and explanations:

---

### 1️⃣ **SyntaxError**
Occurs when the code violates Python's syntax rules.

**Example:**
```python
# Missing a colon in the if statement
if True
    print("Hello")
# SyntaxError: invalid syntax
```

---

### 2️⃣ **IndentationError**
Happens when the indentation is incorrect or inconsistent.

**Example:**
```python
def greet():
print("Hello")
# IndentationError: expected an indented block
```

---

### 3️⃣ **NameError**
Raised when referencing a variable or function that is not defined.

**Example:**
```python
print(unknown_variable)
# NameError: name 'unknown_variable' is not defined
```

---

### 4️⃣ **TypeError**
Occurs when an operation or function is applied to an object of an inappropriate type.

**Example:**
```python
print(5 + "string")
# TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

---

### 5️⃣ **ValueError**
Raised when a function receives an argument of the correct type but an inappropriate value.

**Example:**
```python
int("not_a_number")
# ValueError: invalid literal for int() with base 10: 'not_a_number'
```

---

### 6️⃣ **IndexError**
Happens when accessing an index that is out of range in a list or tuple.

**Example:**
```python
lst = [1, 2, 3]
print(lst[5])
# IndexError: list index out of range
```

---

### 7️⃣ **KeyError**
Occurs when trying to access a dictionary key that doesn’t exist.

**Example:**
```python
d = {"a": 1, "b": 2}
print(d["c"])
# KeyError: 'c'
```

---

### 8️⃣ **AttributeError**
Raised when an object does not have the attribute you’re trying to access.

**Example:**
```python
lst = [1, 2, 3]
lst.append(4)
lst.push(5)
# AttributeError: 'list' object has no attribute 'push'
```

---

### 9️⃣ **ZeroDivisionError**
Happens when dividing a number by zero.

**Example:**
```python
result = 10 / 0
# ZeroDivisionError: division by zero
```

---

### 🔟 **ImportError / ModuleNotFoundError**
Raised when trying to import a module that doesn’t exist or can’t be found.

**Example:**
```python
import non_existent_module
# ModuleNotFoundError: No module named 'non_existent_module'
```

---

### 1️⃣1️⃣ **FileNotFoundError**
Occurs when attempting to access a file that doesn’t exist.

**Example:**
```python
with open("non_existent_file.txt", "r") as file:
    content = file.read()
# FileNotFoundError: [Errno 2] No such file or directory: 'non_existent_file.txt'
```

---

### 1️⃣2️⃣ **TypeError: Missing Arguments**
Happens when calling a function without providing the required arguments.

**Example:**
```python
def greet(name):
    print(f"Hello, {name}!")

greet()
# TypeError: greet() missing 1 required positional argument: 'name'
```

---

### 1️⃣3️⃣ **RecursionError**
Raised when the maximum recursion depth is exceeded.

**Example:**
```python
def infinite_recursion():
    return infinite_recursion()

infinite_recursion()
# RecursionError: maximum recursion depth exceeded
```

---

### 1️⃣4️⃣ **MemoryError**
Occurs when the program runs out of memory.

**Example:**
```python
# Attempting to create an extremely large list
huge_list = [0] * (10 ** 10)
# MemoryError
```

---

### 1️⃣5️⃣ **OverflowError**
Raised when the result of an arithmetic operation is too large to be represented.

**Example:**
```python
import math
print(math.exp(1000))
# OverflowError: math range error
```

---

### 1️⃣6️⃣ **AssertionError**
Raised when an `assert` statement fails.

**Example:**
```python
x = 10
assert x > 20, "x must be greater than 20"
# AssertionError: x must be greater than 20
```

---

### 1️⃣7️⃣ **StopIteration**
Happens when there are no more items in an iterator.

**Example:**
```python
lst = [1, 2, 3]
it = iter(lst)
print(next(it))
print(next(it))
print(next(it))
print(next(it))
# StopIteration
```

---

### 1️⃣8️⃣ **PermissionError**
Occurs when the program doesn’t have permission to perform an action.

**Example:**
```python
with open("/root/protected_file.txt", "w") as file:
    file.write("Hello")
# PermissionError: [Errno 13] Permission denied: '/root/protected_file.txt'
```

---

### 1️⃣9️⃣ **UnicodeDecodeError**
Happens when trying to decode a string with an incompatible encoding.

**Example:**
```python
with open("file.txt", "r", encoding="utf-8") as file:
    content = file.read()
# UnicodeDecodeError (if the file is not in UTF-8 encoding)
```

---

### 2️⃣0️⃣ **RuntimeError**
A generic error indicating something went wrong during runtime.

**Example:**
```python
# Improper use of iterators
it = iter([1, 2, 3])
next(it)
del it
next(it)
# RuntimeError: generator ignored GeneratorExit
```

---


---

### 2️⃣1️⃣ **IndexError: String Index Out of Range**
Occurs when attempting to access a character in a string that doesn’t exist.

**Example:**
```python
s = "hello"
print(s[10])  # IndexError: string index out of range
```

---

### 2️⃣2️⃣ **MemoryError**
Raised when attempting operations that consume excessive memory.

**Example:**
```python
# Trying to create an excessively large object
big_list = [1] * (10 ** 9)
# MemoryError
```

---

### 2️⃣3️⃣ **FloatingPointError**
Rarely raised. Happens when performing an invalid operation on floating-point numbers (disabled by default).

**Example:**
```python
import sys
sys.float_info.epsilon / 0.0
# FloatingPointError: floating-point exception
```

---

### 2️⃣4️⃣ **LookupError**
A base class for errors raised when a lookup operation fails (`IndexError` and `KeyError` inherit from this).

**Example:**
```python
# Base class demonstration
d = {"key": "value"}
try:
    print(d["nonexistent_key"])
except LookupError as e:
    print(f"LookupError caught: {e}")
```

---

### 2️⃣5️⃣ **UnboundLocalError**
Occurs when trying to reference a local variable before it has been assigned.

**Example:**
```python
def example():
    print(x)
    x = 10
example()
# UnboundLocalError: local variable 'x' referenced before assignment
```

---

### 2️⃣6️⃣ **ModuleNotFoundError**
Raised when attempting to import a module that doesn’t exist.

**Example:**
```python
import nonexistent_module
# ModuleNotFoundError: No module named 'nonexistent_module'
```

---

### 2️⃣7️⃣ **NotImplementedError**
Raised when an abstract method in a base class is not implemented in a derived class.

**Example:**
```python
class Base:
    def action(self):
        raise NotImplementedError("Subclasses must implement this method")

class Derived(Base):
    pass

d = Derived()
d.action()
# NotImplementedError: Subclasses must implement this method
```

---

### 2️⃣8️⃣ **OverflowError**
Occurs when a numeric calculation exceeds the maximum representable value.

**Example:**
```python
import math
print(math.exp(1000))
# OverflowError: math range error
```

---

### 2️⃣9️⃣ **EnvironmentError (Base Class for IOError & OSError)**
A base class for exceptions caused by outside factors like operating system errors.

**Example:**
```python
try:
    open("/root/file.txt", "r")
except EnvironmentError as e:
    print(f"EnvironmentError caught: {e}")
```

---

### 3️⃣0️⃣ **IOError**
Raised when an I/O operation fails, like reading a file that doesn’t exist (merged into `OSError` in Python 3).

**Example:**
```python
with open("nonexistent_file.txt", "r") as file:
    pass
# IOError: [Errno 2] No such file or directory: 'nonexistent_file.txt'
```

---

### 3️⃣1️⃣ **OSError**
Raised for system-related errors like file not found, permission denied, etc.

**Example:**
```python
import os
os.rename("nonexistent_file.txt", "new_file.txt")
# OSError: [Errno 2] No such file or directory
```

---

### 3️⃣2️⃣ **StopAsyncIteration**
Occurs when an asynchronous generator has no more items to yield.

**Example:**
```python
class AsyncGen:
    async def __aiter__(self):
        return self

    async def __anext__(self):
        raise StopAsyncIteration

async def main():
    async for value in AsyncGen():
        print(value)

# No output; StopAsyncIteration occurs silently.
```

---

### 3️⃣3️⃣ **SystemExit**
Raised by the `sys.exit()` function.

**Example:**
```python
import sys
sys.exit("Exiting program")
# SystemExit: Exiting program
```

---

### 3️⃣4️⃣ **KeyboardInterrupt**
Raised when the user interrupts the program execution, typically by pressing `Ctrl+C`.

**Example:**
```python
while True:
    pass
# Press Ctrl+C to raise KeyboardInterrupt
```

---

### 3️⃣5️⃣ **GeneratorExit**
Raised inside a generator when `close()` is called.

**Example:**
```python
def generator():
    try:
        yield 1
    except GeneratorExit:
        print("Generator closed")

gen = generator()
next(gen)
gen.close()
# Output: Generator closed
```

---

### 3️⃣6️⃣ **ArithmeticError (Base Class for Math Errors)**
A base class for `ZeroDivisionError`, `OverflowError`, and others.

**Example:**
```python
try:
    1 / 0
except ArithmeticError as e:
    print(f"ArithmeticError caught: {e}")
# Output: ArithmeticError caught: division by zero
```

---

### 3️⃣7️⃣ **TimeoutError**
Raised when a system call times out (subclass of `OSError`).

**Example:**
```python
import socket
s = socket.socket()
s.settimeout(1)
s.connect(("example.com", 80))  # If network is slow, this can raise TimeoutError
# TimeoutError: [Errno 110] Connection timed out
```

---

### 3️⃣8️⃣ **AssertionError**
Occurs when an `assert` statement evaluates to `False`.

**Example:**
```python
x = 5
assert x > 10, "x is not greater than 10"
# AssertionError: x is not greater than 10
```

---

### 3️⃣9️⃣ **EOFError**
Raised when the `input()` function hits an end-of-file condition (no more input).

**Example:**
```python
input("Enter something: ")  # Press Ctrl+D (Linux/Mac) or Ctrl+Z (Windows) to trigger EOFError.
# EOFError
```

---

### 4️⃣0️⃣ **IsADirectoryError**
Occurs when a file operation is attempted on a directory.

**Example:**
```python
with open("/", "r") as f:
    pass
# IsADirectoryError: [Errno 21] Is a directory: '/'
```

---

### 4️⃣1️⃣ **TabError**
Occurs when there is a mix of tabs and spaces in indentation.

**Example:**
```python
def example():
	print("Tab Error")  # Indented with a tab
    print("Spaces")      # Indented with spaces
# TabError: inconsistent use of tabs and spaces in indentation
```

---

### 4️⃣2️⃣ **ConnectionError (Base Class for Network Errors)**
A base class for exceptions raised for connection-related issues.

**Example:**
```python
import requests
try:
    requests.get("http://nonexistent.url")
except requests.exceptions.ConnectionError as e:
    print(f"ConnectionError: {e}")
```

---

### 4️⃣3️⃣ **TypeError: Missing Required Positional Argument**
Occurs when calling a function without providing all the required arguments.

**Example:**
```python
def add(a, b):
    return a + b

add(10)
# TypeError: add() missing 1 required positional argument: 'b'
```

---

### 4️⃣4️⃣ **RuntimeWarning**
Raised as a warning during runtime, often for risky operations.

**Example:**
```python
import warnings
warnings.warn("This is a runtime warning", RuntimeWarning)
# Output: RuntimeWarning: This is a runtime warning
```

---

### 4️⃣5️⃣ **UnicodeEncodeError**
Occurs when trying to encode characters that cannot be handled by the given encoding.

**Example:**
```python
s = "é"
s.encode("ascii")
# UnicodeEncodeError: 'ascii' codec can't encode character '\xe9' in position 0
```

---

### 4️⃣6️⃣ **UnicodeDecodeError**
Occurs when decoding bytes into a string fails due to incompatible encoding.

**Example:**
```python
b = b"\xff"
b.decode("utf-8")
# UnicodeDecodeError: 'utf-8' codec can't decode byte 0xff in position 0
```








****
****
