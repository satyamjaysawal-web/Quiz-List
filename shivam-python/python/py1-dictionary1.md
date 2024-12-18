Yeh raha ek **dictionary-related code snippets** ka collection jo aapko dictionary ke operations samajhne mein madad karega:

### 1. **Creating a Dictionary**
```python
# Create a simple dictionary
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}
print(person)
```

### 2. **Accessing Dictionary Values**
```python
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

# Access value using key
print(person['name'])  # Output: John
print(person.get('age'))  # Output: 30
```

### 3. **Modifying Dictionary Values**
```python
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

# Modifying existing key-value pair
person['age'] = 31
print(person)

# Adding a new key-value pair
person['job'] = 'Engineer'
print(person)
```

### 4. **Removing Items from Dictionary**
```python
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

# Removing key-value pair using del
del person['city']
print(person)

# Removing an item using pop()
job = person.pop('job', 'Not Found')  # Default value if key not found
print(person)
print('Job:', job)
```

### 5. **Iterating Through Dictionary**
```python
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

# Loop through keys
for key in person:
    print(key, ":", person[key])

# Using items() to loop through both key and value
for key, value in person.items():
    print(key, "->", value)
```

### 6. **Checking if Key Exists**
```python
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

# Check if a key exists
if 'age' in person:
    print('Age exists:', person['age'])

if 'job' not in person:
    print('Job key does not exist in dictionary')
```

### 7. **Merging Two Dictionaries**
```python
dict1 = {'name': 'John', 'age': 30}
dict2 = {'city': 'New York', 'job': 'Engineer'}

# Merging dictionaries using update()
dict1.update(dict2)
print(dict1)  # Output: {'name': 'John', 'age': 30, 'city': 'New York', 'job': 'Engineer'}
```

### 8. **Dictionary Comprehension**
```python
# Creating a dictionary using dictionary comprehension
squares = {x: x**2 for x in range(1, 6)}
print(squares)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

### 9. **Nested Dictionaries**
```python
# Creating a dictionary with another dictionary
person = {
    'name': 'John',
    'address': {
        'city': 'New York',
        'zip': '10001'
    }
}

# Accessing nested dictionary values
print(person['address']['city'])  # Output: New York
```

### 10. **Dictionary with Default Values**
```python
# Using defaultdict to set default values
from collections import defaultdict

# Creating a dictionary that defaults to 0
count = defaultdict(int)
count['apple'] += 1
count['banana'] += 2

print(count)  # Output: defaultdict(<class 'int'>, {'apple': 1, 'banana': 2})
```

### 11. **Sorting a Dictionary by Key or Value**
```python
# Sorting a dictionary by key
person = {'name': 'John', 'age': 30, 'city': 'New York'}
sorted_by_key = {k: person[k] for k in sorted(person)}
print(sorted_by_key)

# Sorting a dictionary by value
sorted_by_value = dict(sorted(person.items(), key=lambda item: item[1]))
print(sorted_by_value)
```

### 12. **Copying a Dictionary**
```python
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

# Using copy() method
person_copy = person.copy()
print(person_copy)

# Using dict() constructor
person_copy2 = dict(person)
print(person_copy2)
```

### 13. **Getting All Keys, Values, and Items**
```python
person = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

# Get all keys
keys = person.keys()
print(keys)  # Output: dict_keys(['name', 'age', 'city'])

# Get all values
values = person.values()
print(values)  # Output: dict_values(['John', 30, 'New York'])

# Get all items (key-value pairs)
items = person.items()
print(items)  # Output: dict_items([('name', 'John'), ('age', 30), ('city', 'New York')])
```

---
****

### **Comprehensive Overview of Dictionaries in Python**

A **dictionary** in Python is a mutable, unordered collection of key-value pairs. Each key in a dictionary is unique, and it maps to a specific value.

---

### **Key Properties of Dictionaries**
| **Property**              | **Explanation**                                            |
|--------------------------|----------------------------------------------------------|
| **Key-Value Pairs**       | Stores data as key-value pairs.                           |
| **Mutable**               | You can add, remove, or update key-value pairs.           |
| **Unique Keys**           | Keys must be unique; duplicate keys overwrite existing ones. |
| **Unordered (Pre-3.7)**   | Keys are not stored in order (insertion order maintained from Python 3.7+). |
| **Hashable Keys**         | Keys must be immutable types like strings, numbers, or tuples. |
| **Dynamic Size**          | Grows or shrinks dynamically as elements are added or removed. |
| **Efficient Access**      | Provides fast lookups, updates, and deletions with O(1) average time complexity. |

---

### **Creating a Dictionary**

#### 1. Using curly braces `{}`:
```python
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
```

#### 2. Using the `dict()` constructor:
```python
my_dict = dict(name="Alice", age=25, city="New York")
```

#### 3. Using a list of tuples:
```python
my_dict = dict([("name", "Alice"), ("age", 25), ("city", "New York")])
```

---

### **Accessing Elements**
Access values using their keys.

#### 1. Using square brackets `[]`:
```python
print(my_dict["name"])  # Alice
```
- **KeyError** if the key doesn’t exist.

#### 2. Using `.get()`:
```python
print(my_dict.get("age", "Key not found"))  # 25
```
- Returns a default value if the key doesn’t exist.

---

### **Adding or Updating Elements**
```python
# Adding a new key-value pair
my_dict["profession"] = "Engineer"

# Updating an existing key
my_dict["age"] = 26
```

---

### **Deleting Elements**

#### 1. Using `del`:
```python
del my_dict["city"]
```

#### 2. Using `.pop()`:
```python
age = my_dict.pop("age")  # Removes and returns the value
```

#### 3. Using `.popitem()`:
```python
key, value = my_dict.popitem()  # Removes and returns the last inserted key-value pair (3.7+)
```

#### 4. Using `.clear()`:
```python
my_dict.clear()  # Removes all elements
```

---

### **Iterating Through a Dictionary**

#### 1. Iterating through keys:
```python
for key in my_dict:
    print(key)
```

#### 2. Iterating through values:
```python
for value in my_dict.values():
    print(value)
```

#### 3. Iterating through key-value pairs:
```python
for key, value in my_dict.items():
    print(f"{key}: {value}")
```

---

### **Dictionary Comprehensions**
Create dictionaries using a concise syntax.

#### Example:
```python
squares = {x: x**2 for x in range(5)}
print(squares)  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

---

### **Built-in Methods**

#### 1. **`keys()`**:
Returns a view object of all keys.
```python
print(my_dict.keys())  # dict_keys(['name', 'age', 'city'])
```

#### 2. **`values()`**:
Returns a view object of all values.
```python
print(my_dict.values())  # dict_values(['Alice', 25, 'New York'])
```

#### 3. **`items()`**:
Returns a view object of key-value pairs.
```python
print(my_dict.items())  # dict_items([('name', 'Alice'), ('age', 25), ('city', 'New York')])
```

#### 4. **`update()`**:
Merges another dictionary or key-value pairs into the dictionary.
```python
my_dict.update({"age": 30, "country": "USA"})
```

#### 5. **`setdefault()`**:
Returns the value of a key. If the key doesn’t exist, it adds it with a default value.
```python
my_dict.setdefault("gender", "Female")
```

---

### **Dictionary Use Cases**

#### 1. **Mapping Relationships**:
```python
user_info = {"name": "Alice", "email": "alice@example.com"}
```

#### 2. **Counting Occurrences**:
```python
from collections import Counter
text = "hello world"
counter = Counter(text)
print(counter)  # {'h': 1, 'e': 1, 'l': 3, 'o': 2, ' ': 1, 'w': 1, 'r': 1, 'd': 1}
```

#### 3. **Group Data by Key**:
```python
data = [("fruit", "apple"), ("fruit", "banana"), ("vegetable", "carrot")]
grouped = {}
for category, item in data:
    grouped.setdefault(category, []).append(item)
print(grouped)  # {'fruit': ['apple', 'banana'], 'vegetable': ['carrot']}
```

#### 4. **Inverted Dictionaries**:
```python
my_dict = {"a": 1, "b": 2, "c": 3}
inverted = {v: k for k, v in my_dict.items()}
print(inverted)  # {1: 'a', 2: 'b', 3: 'c'}
```

---

### **Common Errors and Solutions**

#### 1. **KeyError**
Occurs when accessing a non-existent key.
```python
value = my_dict["nonexistent"]  # KeyError: 'nonexistent'
```
**Solution**:
Use `.get()` with a default value:
```python
value = my_dict.get("nonexistent", "Default")
```

#### 2. **Unhashable Keys**
Keys must be immutable.
```python
my_dict = {[1, 2]: "value"}  # TypeError: unhashable type: 'list'
```
**Solution**:
Use hashable types like tuples:
```python
my_dict = {(1, 2): "value"}
```

---

### **Advanced Techniques**

#### 1. **Defaultdict**
A dictionary subclass from `collections` that provides a default value for missing keys.
```python
from collections import defaultdict

dd = defaultdict(list)
dd["fruits"].append("apple")
print(dd)  # defaultdict(<class 'list'>, {'fruits': ['apple']})
```

#### 2. **OrderedDict**
A dictionary subclass from `collections` that maintains order in older Python versions (<3.7).
```python
from collections import OrderedDict

od = OrderedDict([("a", 1), ("b", 2)])
print(od)  # OrderedDict([('a', 1), ('b', 2)])
```

#### 3. **ChainMap**
Combines multiple dictionaries into a single view.
```python
from collections import ChainMap

dict1 = {"a": 1}
dict2 = {"b": 2}
chain = ChainMap(dict1, dict2)
print(chain["a"])  # 1
```

---

### **Best Practices**
1. Use descriptive and immutable keys (e.g., strings, numbers).
2. Use `.get()` to avoid `KeyError`.
3. Leverage `defaultdict` for missing keys with default values.
4. Use dictionary comprehensions for cleaner and more concise code.

---












****
****
****
****
****
