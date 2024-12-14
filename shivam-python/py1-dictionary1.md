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

Yeh sab **dictionary operations** hain jo aap apne code mein use kar sakte hain. Agar aapko koi specific concept samajhna ho, toh bataiye, main aur help kar dunga!
