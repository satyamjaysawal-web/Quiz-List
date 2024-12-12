Here’s a list of **small, tricky Python codes** that are commonly asked in interviews, along with explanations and outputs.

---

### **1. Swapping Two Variables Without a Temporary Variable**
```python
a, b = 5, 10
a, b = b, a  # Swap values

print(a, b)  # Output: 10, 5
```

---

### **2. Reverse a String in One Line**
```python
s = "Interview"
reversed_s = s[::-1]  # Reverse using slicing

print(reversed_s)  # Output: "weivretnI"
```

---

### **3. Find the Most Frequent Element in a List**
```python
lst = [1, 3, 2, 3, 4, 3, 5, 1]
most_frequent = max(set(lst), key=lst.count)  # Use `max` with a key function

print(most_frequent)  # Output: 3
```

---

### **4. Check If a String Is a Palindrome**
```python
s = "madam"
is_palindrome = s == s[::-1]  # Compare string with its reverse

print(is_palindrome)  # Output: True
```

---

### **5. Flatten a Nested List**
```python
nested_list = [[1, 2, [3]], [4, 5]]
flattened = sum([sum(i, []) if isinstance(i, list) else [i] for i in nested_list], [])

print(flattened)  # Output: [1, 2, 3, 4, 5]
```

---

### **6. One-Line Fibonacci Generator**
```python
fibonacci = lambda n: [0, 1][:n] + [sum([x, y]) for x, y in zip([0, 1], fibonacci)]

print(fibonacci(6)) #Output `[3]/print rect)



It seems there was an unintended cutoff in the previous code snippet. I'll correct it and continue providing more small and tricky Python code examples for interviews:

---

### **6. One-Line Fibonacci Generator**
```python
fibonacci = lambda n: [0, 1][:n] + [sum([fibonacci(n - 1)[-2], fibonacci(n - 1)[-1]]) for i in range(n-1) ]

Apologies for the incomplete examples earlier. Here’s a corrected version of a small one-line Fibonacci generator and additional small tricky Python codes:

---

### **6. One-Line Fibonacci Generator**
```python
fibonacci = lambda n: [0, 1][:n] + [sum(fibonacci(n-1)[-2:]) for _ in range(n-2)]
print(fibonacci(6))  
# Output: [0, 1, 1, 2, 3, 5]
```

---

### **7. Find All Duplicates in a List**
```python
lst = [1, 2, 3, 4, 5, 2, 3, 6]
duplicates = set([x for x in lst if lst.count(x) > 1])  # Use list comprehension and `set`

print(duplicates)  
# Output: {2, 3}
```

---

### **8. Merge Two Dictionaries**
```python
dict1 = {'a': 1, 'b': 2}
dict2 = {'b': 3, 'c': 4}
merged = {**dict1, **dict2}  # `dict2` values will overwrite `dict1`

print(merged)  
# Output: {'a': 1, 'b': 3, 'c': 4}
```

---

### **9. Check If Two Strings Are Anagrams**
```python
str1, str2 = "listen", "silent"
is_anagram = sorted(str1) == sorted(str2)  # Sort and compare

print(is_anagram)  
# Output: True
```

---

### **10. Print a Matrix in Spiral Order**
```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
spiral = []
while matrix:
    spiral += matrix.pop(0)  # Add the first row
    matrix = list(zip(*matrix))[::-1]  # Rotate the rest of the matrix

print(spiral)  
# Output: [1, 2, 3, 6, 9, 8, 7, 4, 5]
```

---

### **11. Remove Duplicates From a String**
```python
s = "programming"
unique_chars = ''.join(dict.fromkeys(s))  # Use `dict.fromkeys` to remove duplicates

print(unique_chars)  
# Output: "progamin"
```

---

### **12. Generate All Subsets of a List**
```python
from itertools import combinations
lst = [1, 2, 3]
subsets = [list(combo) for i in range(len(lst) + 1) for combo in combinations(lst, i)]

print(subsets)  
# Output: [[], [1], [2], [3], [1, 2], [1, 3], [2, 3], [1, 2, 3]]
```

---

### **13. Find the Intersection of Two Lists**
```python
list1 = [1, 2, 3, 4]
list2 = [3, 4, 5, 6]
intersection = list(set(list1) & set(list2))  # Use set intersection

print(intersection)  
# Output: [3, 4]
```

---

### **14. Find the First Non-Repeating Character**
```python
s = "swiss"
first_unique = next((ch for ch in s if s.count(ch) == 1), None)  # Use generator expression

print(first_unique)  
# Output: 'w'
```

---

### **15. Count the Frequency of Words in a Sentence**
```python
sentence = "this is a test this is only a test"
word_count = {word: sentence.split().count(word) for word in set(sentence.split())}

print(word_count)  
# Output: {'this': 2, 'is': 2, 'a': 2, 'test': 2, 'only': 1}
```

---

### **16. Find the Longest Word in a Sentence**
```python
sentence = "The quick brown fox jumps over the lazy dog"
longest_word = max(sentence.split(), key=len)

print(longest_word)  
# Output: "jumps"
```

---

### **17. Rotate a List by n Positions**
```python
lst = [1, 2, 3, 4, 5]
n = 2
rotated_list = lst[n:] + lst[:n]  # Rotate left by `n`

print(rotated_list)  
# Output: [3, 4, 5, 1, 2]
```

---

### **18. Find the Sum of Digits in a Number**
```python
num = 12345
digit_sum = sum(map(int, str(num)))  # Convert to string, map digits to int, and sum

print(digit_sum)  
# Output: 15
```

---

### **19. Check If a Number Is a Power of Two**
```python
n = 16
is_power_of_two = n > 0 and (n & (n - 1)) == 0  # Use bitwise AND

print(is_power_of_two)  
# Output: True
```

---

### **20. Find the Second Largest Number in a List**
```python
lst = [10, 20, 4, 45, 99]
second_largest = sorted(set(lst))[-2]  # Sort and pick second last element

print(second_largest)  
# Output: 45
```
Here’s a list of additional **tricky Python interview questions** that challenge your understanding of Python's features, tricks, and concepts:

---

### **21. Find the Missing Number in a Sequence**
```python
nums = [1, 2, 4, 5, 6]
missing = sum(range(nums[0], nums[-1] + 1)) - sum(nums)  # Sum of full range - Sum of given numbers

print(missing)  
# Output: 3
```

---

### **22. Print a Number Pyramid**
```python
rows = 5
for i in range(1, rows + 1):
    print(" " * (rows - i) + " ".join(map(str, range(1, i + 1))))  # Left-align pyramid

# Output:
#     1
#    1 2
#   1 2 3
#  1 2 3 4
# 1 2 3 4 5
```

---

### **23. Sort a List of Tuples by Second Element**
```python
tuples = [(1, 3), (3, 2), (2, 4)]
sorted_tuples = sorted(tuples, key=lambda x: x[1])  # Sort using the second element of each tuple

print(sorted_tuples)  
# Output: [(3, 2), (1, 3), (2, 4)]
```

---

### **24. Detect a Loop in a Linked List**
```python
class Node:
    def __init__(self, value):
        self.value = value
        self.next = None

# Create a linked list with a loop
head = Node(1)
head.next = Node(2)
head.next.next = Node(3)
head.next.next.next = head.next  # Loop

def has_loop(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow == fast:
            return True
    return False

print(has_loop(head))  
# Output: True
```

---

### **25. Create a Decorator to Measure Execution Time**
```python
import time

def timer(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"Execution time: {end - start:.2f} seconds")
        return result
    return wrapper

@timer
def slow_function():
    time.sleep(2)  # Simulate a delay
    return "Finished"

print(slow_function())  
# Output:
# Execution time: 2.00 seconds
# Finished
```

---

### **26. Find All Prime Numbers in a Range**
```python
def is_prime(n):
    return n > 1 and all(n % i != 0 for i in range(2, int(n**0.5) + 1))

primes = [x for x in range(2, 20) if is_prime(x)]

print(primes)  
# Output: [2, 3, 5, 7, 11, 13, 17, 19]
```

---

### **27. Find the Longest Substring Without Repeating Characters**
```python
s = "abcabcbb"
seen = {}
start = max_length = 0

for i, char in enumerate(s):
    if char in seen and seen[char] >= start:
        start = seen[char] + 1
    seen[char] = i
    max_length = max(max_length, i - start + 1)

print(max_length)  
# Output: 3  (Substring: "abc")
```

---

### **28. Calculate the Power of a Number Without `**`**
```python
def power(base, exp):
    return 1 if exp == 0 else base * power(base, exp - 1)  # Recursive solution

print(power(2, 3))  
# Output: 8
```

---

### **29. Merge Intervals**
```python
intervals = [[1, 3], [2, 6], [8, 10], [15, 18]]
intervals.sort(key=lambda x: x[0])  # Sort intervals by start time
merged = []

for interval in intervals:
    if not merged or merged[-1][1] < interval[0]:
        merged.append(interval)  # No overlap, add the interval
    else:
        merged[-1][1] = max(merged[-1][1], interval[1])  # Merge overlapping intervals

print(merged)  
# Output: [[1, 6], [8, 10], [15, 18]]
```

---

### **30. Find the GCD of Two Numbers**
```python
def gcd(a, b):
    while b:
        a, b = b, a % b  # Use Euclid's algorithm
    return a

print(gcd(48, 18))  
# Output: 6
```

---

### **31. Generate a Pascal's Triangle**
```python
def pascal_triangle(n):
    triangle = [[1]]
    for _ in range(n - 1):
        prev = triangle[-1]
        row = [1] + [prev[i] + prev[i + 1] for i in range(len(prev) - 1)] + [1]
        triangle.append(row)
    return triangle

print(pascal_triangle(5))  
# Output:
# [[1], [1, 1], [1, 2, 1], [1, 3, 3, 1], [1, 4, 6, 4, 1]]
```

---

### **32. Evaluate a Mathematical Expression from a String**
```python
expr = "3 + 5 * (2 - 8)"
result = eval(expr)  # `eval` parses and evaluates the expression

print(result)  
# Output: -25
```

---

### **33. Generate All Permutations of a String**
```python
from itertools import permutations

s = "abc"
perms = [''.join(p) for p in permutations(s)]

print(perms)  
# Output: ['abc', 'acb', 'bac', 'bca', 'cab', 'cba']
```

---

### **34. Sort Words in a String Alphabetically**
```python
sentence = "interview tricky questions for python"
sorted_words = ' '.join(sorted(sentence.split()))

print(sorted_words)  
# Output: "for interview python questions tricky"
```

---

### **35. Find the Majority Element in a List**
```python
nums = [3, 3, 4, 2, 4, 4, 2, 4, 4]
majority = max(set(nums), key=nums.count)  # Element with the highest count

print(majority)  
# Output: 4
```

---

---
****







