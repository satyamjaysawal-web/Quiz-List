Here’s a **list of common Python errors** along with their causes and examples, just like the explanation for `NoneType` errors:

---

### **1. `SyntaxError`**
Occurs when there’s a mistake in the syntax of the Python code.

**Example**:
```python
if True
    print("Hello!")  # Missing colon at the end of the if statement
```

**Fix**:
```python
if True:
    print("Hello!")
```

---

### **2. `IndentationError`**
Happens when the indentation is inconsistent or incorrect.

**Example**:
```python
def greet():
print("Hello!")  # Indented incorrectly
```

**Fix**:
```python
def greet():
    print("Hello!")  # Properly indented
```

---

### **3. `NameError`**
Raised when a variable or function is not defined.

**Example**:
```python
print(message)  # 'message' is not defined
```

**Fix**:
```python
message = "Hello!"
print(message)
```

---

### **4. `TypeError`**
Occurs when an operation or function is applied to an object of an inappropriate type.

**Example**:
```python
result = 5 + "hello"  # Cannot add an integer and a string
```

**Fix**:
```python
result = 5 + int("10")  # Convert string to integer, or ensure compatible types
```

---

### **5. `IndexError`**
Raised when trying to access an index that is out of range in a list or other indexable object.

**Example**:
```python
my_list = [1, 2, 3]
print(my_list[5])  # Index out of range
```

**Fix**:
```python
if len(my_list) > 5:
    print(my_list[5])
else:
    print("Index out of range.")
```

---

### **6. `KeyError`**
Occurs when trying to access a key that doesn’t exist in a dictionary.

**Example**:
```python
my_dict = {"name": "Alice"}
print(my_dict["age"])  # Key 'age' does not exist
```

**Fix**:
```python
print(my_dict.get("age", "Key not found"))  # Use get() with a default value
```

---

### **7. `ValueError`**
Raised when a function receives an argument of the correct type but an invalid value.

**Example**:
```python
number = int("abc")  # Cannot convert 'abc' to an integer
```

**Fix**:
```python
try:
    number = int("abc")
except ValueError:
    print("Invalid value. Cannot convert to integer.")
```

---

### **8. `AttributeError`**
Occurs when you try to access an attribute or method that doesn’t exist for an object.

**Example**:
```python
my_number = 5
my_number.append(10)  # Integers do not have an 'append' method
```

**Fix**:
```python
my_list = [5]
my_list.append(10)
```

---

### **9. `ImportError` / `ModuleNotFoundError`**
Raised when an import statement fails because the module isn’t found or isn’t installed.

**Example**:
```python
import non_existent_module  # This module does not exist
```

**Fix**:
```bash
pip install module_name  # Install the required module
```
Or ensure the module exists in the environment.

---

### **10. `ZeroDivisionError`**
Occurs when attempting to divide a number by zero.

**Example**:
```python
result = 10 / 0  # Division by zero
```

**Fix**:
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

### **11. `FileNotFoundError`**
Raised when attempting to open a file that doesn’t exist.

**Example**:
```python
with open("non_existent_file.txt", "r") as file:
    content = file.read()
```

**Fix**:
```python
try:
    with open("non_existent_file.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("File not found.")
```

---

### **12. `RuntimeError`**
Occurs during runtime if no other error fits.

**Example**:
```python
def recursive():
    return recursive()  # Causes a stack overflow
recursive()
```

**Fix**:
- Check the runtime logic for unintended infinite loops or recursion.

---

### **13. `OverflowError`**
Raised when a numerical operation produces a result too large to be handled by Python.

**Example**:
```python
import math
result = math.exp(1000)  # Exceeds the maximum floating-point value
```

**Fix**:
- Limit the inputs to mathematical operations.

---

### **14. `RecursionError`**
Occurs when the recursion depth exceeds the allowed limit.

**Example**:
```python
def recursive():
    return recursive()
recursive()
```

**Fix**:
```python
import sys
sys.setrecursionlimit(1000)  # Set a higher recursion limit if necessary
```

---

### **15. `StopIteration`**
Occurs when the `next()` function is called on an iterator that has no items left.

**Example**:
```python
my_iter = iter([1, 2, 3])
for _ in range(4):
    print(next(my_iter))
```

**Fix**:
```python
my_iter = iter([1, 2, 3])
try:
    for _ in range(4):
        print(next(my_iter))
except StopIteration:
    print("End of iteration.")
```

---

If you'd like a detailed explanation or fix for any of these errors or others, let me know!
