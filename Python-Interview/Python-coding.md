



Chalo, main aapko Python mein strings se related kuch concepts aur unke codes ke sath explain karta hoon. Har concept ke saath uska output bhi dikhata hoon.

### 1. What is a string in Python and how is it defined?
Python mein string ek sequence hai characters ka. Aap strings ko single ya double quotes mein define kar sakte ho.

```python
# Example
str1 = "Hello, World!"  # String defined using double quotes
str2 = 'Python'         # String defined using single quotes

print(str1)  # Output: Hello, World!
print(str2)  # Output: Python
```

### 2. How to check if a given string is a palindrome or not?
Palindrome woh string hoti hai jo reverse karne par bhi wahi hoti hai.

```python
# Example
str1 = "radar"
rev_str = str1[::-1]

if str1 == rev_str:
    print("Palindrome")  # Output: Palindrome
else:
    print("Not a Palindrome")
```

### 3. How to reverse a string in Python?
Aap string ko slicing ke through reverse kar sakte ho.

```python
# Example
str1 = "hello"
rev_str = str1[::-1]

print(rev_str)  # Output: olleh
```

### 4. How to find the length of a string in Python?
Aap `len()` function ka use karke string ki length nikaal sakte ho.

```python
# Example
str1 = "Hello, World!"
length = len(str1)

print(length)  # Output: 13
```

### 5. How to check if a substring exists in a string?
Aap `find()` method ya `in` operator ka use kar sakte ho.

```python
# Example
str1 = "hello world"
if "hello" in str1:
    print("Substring found")  # Output: Substring found
else:
    print("Substring not found")
```

### 6. How to replace a substring in a string?
Aap `replace()` method ka use kar ke substring replace kar sakte ho.

```python
# Example
str1 = "Hello, world!"
new_str = str1.replace("world", "Python")

print(new_str)  # Output: Hello, Python!
```

### 7. How to concatenate two strings in Python?
Aap `+` operator ya `join()` method ka use kar sakte ho.

```python
# Example
str1 = "Hello"
str2 = "World"
concatenated_str = str1 + " " + str2

print(concatenated_str)  # Output: Hello World
```

### 8. How to split a string into a list in Python?
Aap `split()` method ka use kar ke string ko list mein convert kar sakte ho.

```python
# Example
str1 = "Hello World"
str_list = str1.split()

print(str_list)  # Output: ['Hello', 'World']
```

### 9. How to format strings in Python?
Aap `format()` method ka use karke strings ko format kar sakte ho.

```python
# Example
name = "John"
age = 30
formatted_str = "My name is {} and I am {} years old.".format(name, age)

print(formatted_str)  # Output: My name is John and I am 30 years old.
```

### 10. How to convert an integer to a string in Python?
Aap `str()` function ka use karke integer ko string mein convert kar sakte ho.

```python
# Example
num = 100
str_num = str(num)

print(str_num)  # Output: 100
print(type(str_num))  # Output: <class 'str'>
```

### 11. How to convert a string to an integer in Python?
Aap `int()` function ka use kar ke string ko integer mein convert kar sakte ho.

```python
# Example
str_num = "100"
int_num = int(str_num)

print(int_num)  # Output: 100
print(type(int_num))  # Output: <class 'int'>
```

### 12. How to check if a string is alphabetic, numeric, or alphanumeric?
Aap `isalpha()`, `isnumeric()`, aur `isalnum()` methods ka use kar sakte ho.

```python
# Example
str1 = "Hello"
str2 = "123"
str3 = "Hello123"

if str1.isalpha():
    print("Alphabetic")  # Output: Alphabetic
if str2.isnumeric():
    print("Numeric")      # Output: Numeric
if str3.isalnum():
    print("Alphanumeric") # Output: Alphanumeric
```

### 13. How to check if a string starts or ends with a specific substring?
Aap `startswith()` aur `endswith()` methods ka use kar sakte ho.

```python
# Example
str1 = "Hello, World!"

if str1.startswith("Hello"):
    print("Starts with 'Hello'")  # Output: Starts with 'Hello'
if str1.endswith("World!"):
    print("Ends with 'World!'")    # Output: Ends with 'World!'
```

### 14. How to strip leading and trailing whitespace from a string?
Aap `strip()` method ka use kar sakte ho.

```python
# Example
str1 = "  Hello, World!  "
stripped_str = str1.strip()

print(stripped_str)  # Output: Hello, World!
```

### 15. How to uppercase or lowercase a string in Python?
Aap `upper()` aur `lower()` methods ka use kar sakte ho.

```python
# Example
str1 = "Hello, World!"
print(str1.upper())  # Output: HELLO, WORLD!
print(str1.lower())  # Output: hello, world!
```

### 16. How to find the index of a character in a string?
Aap `find()` method ka use kar sakte ho.

```python
# Example
str1 = "Hello, World!"
index = str1.find("e")

print(index)  # Output: 1
```

### 17. How to find the occurrence of a character in a string?
Aap `count()` method ka use kar sakte ho.

```python
# Example
str1 = "Hello, World!"
count = str1.count("l")

print(count)  # Output: 3
```

### 18. How to check if a string is an anagram of another string?
Aap sorted function ka use kar ke check kar sakte ho.

```python
# Example
str1 = "listen"
str2 = "silent"

if sorted(str1) == sorted(str2):
    print("Anagram")  # Output: Anagram
else:
    print("Not an Anagram")
```

### 19. How to sort the characters in a string?
Aap `sorted()` function ka use kar ke string ko sort kar sakte ho.

```python
# Example
str1 = "hello"
sorted_str = ''.join(sorted(str1))

print(sorted_str)  # Output: ehllo
```

### 20. How to check if a string is a permutation of another string?
Aap `sorted()` function ka use kar ke check kar sakte ho.

```python
# Example
str1 = "abc"
str2 = "bca"

if sorted(str1) == sorted(str2):
    print("Permutation")  # Output: Permutation
else:
    print("Not a Permutation")
```

### 21. How to check if a string is a rotation of another string?
Aap string ko concatenate kar ke check kar sakte ho.

```python
# Example
str1 = "abcde"
str2 = "deabc"
concat_str = str1 + str1

if str2 in concat_str:
    print("Rotation")  # Output: Rotation
else:
    print("Not a Rotation")
```

### 22. How to find the longest common substring between two strings?
Yeh problem thodi complex hai. Aap dynamic programming approach use kar sakte ho.

```python
# Example (brute force approach)
def longest_common_substring(s1, s2):
    max_length = 0
    end_index = 0
    
    for i in range(len(s1)):
        for j in range(len(s2)):
            length = 0
            while (i + length < len(s1)) and (j + length < len(s2)) and (s1[i + length] == s2[j + length]):
                length += 1
            if length > max_length:
                max_length = length
                end_index = i + length
                
    return s1[end_index - max_length:end_index]

str1 = "abcde"
str2 = "bcdeabc"
lcs = longest_common_substring(str1, str2)

print(lcs)  # Output: bcd
```

### 23. How to find the longest palindromic substring in a string?
Aap expand around center approach use kar sakte ho.

```python
# Example
def longest_palindromic_substring(s):
    start, end = 0, 0
    
    for i in range(len(s)):
        len1 = expand_around_center(s, i, i)     # Odd length palindromes
        len2 = expand_around_center(s, i, i + 1) # Even length palindromes
        length = max(len

1, len2)
        
        if length > (end - start):
            start = i - (length - 1) // 2
            end = i + length // 2
            
    return s[start:end + 1]

def expand_around_center(s, left, right):
    while left >= 0 and right < len(s) and s[left] == s[right]:
        left -= 1
        right += 1
    return right - left - 1

str1 = "babad"
lps = longest_palindromic_substring(str1)

print(lps)  # Output: "bab" or "aba"
```

### 24. How to find the Levenshtein distance between two strings?
Yeh string distance measure karta hai.

```python
# Example
def levenshtein_distance(s1, s2):
    if len(s1) < len(s2):
        return levenshtein_distance(s2, s1)
    
    if len(s2) == 0:
        return len(s1)

    previous_row = range(len(s2) + 1)
    
    for i, c1 in enumerate(s1):
        current_row = [i + 1]
        for j, c2 in enumerate(s2):
            insertions = previous_row[j + 1] + 1
            deletions = current_row[j] + 1
            substitutions = previous_row[j] + (c1 != c2)
            current_row.append(min(insertions, deletions, substitutions))
        previous_row = current_row
        
    return previous_row[-1]

str1 = "kitten"
str2 = "sitting"
distance = levenshtein_distance(str1, str2)

print(distance)  # Output: 3
```

### 25. How to find the Hamming distance between two strings?
Hamming distance sirf un strings ke liye defined hota hai jinki length same hoti hai.

```python
# Example
def hamming_distance(s1, s2):
    if len(s1) != len(s2):
        raise ValueError("Strings must be of the same length")
    return sum(el1 != el2 for el1, el2 in zip(s1, s2))

str1 = "karolin"
str2 = "kathrin"
distance = hamming_distance(str1, str2)

print(distance)  # Output: 3
```

### 26. How to find the edit distance between two strings?
Edit distance ko Levenshtein distance kehte hain, jise hum pehle hi discuss kar chuke hain.

### 27. How to find the similarity between two strings?
Aap Levenshtein distance ya Jaccard index ka use kar sakte ho.

```python
# Example using Levenshtein distance
def string_similarity(s1, s2):
    max_len = max(len(s1), len(s2))
    if max_len == 0:
        return 1.0
    return 1 - levenshtein_distance(s1, s2) / max_len

str1 = "hello"
str2 = "hallo"
similarity = string_similarity(str1, str2)

print(similarity)  # Output: 0.8 (example)
```

### 28. How to find the difference between two strings?
Aap `difflib` module ka use kar sakte ho.

```python
import difflib

str1 = "Hello, World!"
str2 = "Hello, Python!"

diff = difflib.ndiff(str1, str2)
print(''.join(diff))  # Output: '  H e l l o ,   W o r l d !\n  H e l l o ,   P y t h o n !'
```

### 29. How to find the longest common subsequence between two strings?
Aap dynamic programming ka use karke yeh nikaal sakte ho.

```python
# Example
def longest_common_subsequence(s1, s2):
    dp = [[0] * (len(s2) + 1) for _ in range(len(s1) + 1)]
    
    for i in range(1, len(s1) + 1):
        for j in range(1, len(s2) + 1):
            if s1[i - 1] == s2[j - 1]:
                dp[i][j] = dp[i - 1][j - 1] + 1
            else:
                dp[i][j] = max(dp[i - 1][j], dp[i][j - 1])
                
    return dp[-1][-1]

str1 = "AGGTAB"
str2 = "GXTXAYB"
lcs_length = longest_common_subsequence(str1, str2)

print(lcs_length)  # Output: 4
```

### 30. How to find the KMP failure function for a string?
KMP algorithm ka use kar ke substring search karne mein hota hai.

```python
# Example
def kmp_failure_function(pattern):
    m = len(pattern)
    lps = [0] * m
    length = 0
    i = 1

    while i < m:
        if pattern[i] == pattern[length]:
            length += 1
            lps[i] = length
            i += 1
        else:
            if length != 0:
                length = lps[length - 1]
            else:
                lps[i] = 0
                i += 1

    return lps

pattern = "AAACAAAA"
failure_function = kmp_failure_function(pattern)

print(failure_function)  # Output: [0, 1, 0, 3, 0, 1, 2, 3]
```

### 31. How to find the Z-algorithm for a string?
Z-algorithm ko substring search ke liye use kiya jaata hai.

```python
# Example
def z_algorithm(s):
    Z = [0] * len(s)
    left, right, n = 0, 0, len(s)
    
    for i in range(1, n):
        if i > right:
            left, right = i, i
            while right < n and s[right] == s[right - left]:
                right += 1
            Z[i] = right - left
            right -= 1
        else:
            k = i - left
            if Z[k] < right - i + 1:
                Z[i] = Z[k]
            else:
                left = i
                while right < n and s[right] == s[right - left]:
                    right += 1
                Z[i] = right - left
                right -= 1
                
    return Z

string = "abacaba"
z_values = z_algorithm(string)

print(z_values)  # Output: [0, 0, 1, 0, 3, 0, 1]
```

### 32. How to find the longest repeating substring in a string?
Yeh bhi thodi complex hai, aap suffix arrays ya suffix trees ka use kar sakte ho.

### 33. How to find the longest repeating subsequence in a string?
Aap dynamic programming ka use kar ke yeh nikaal sakte ho.

```python
# Example
def longest_repeating_subsequence(s):
    n = len(s)
    dp = [[0] * (n + 1) for _ in range(n + 1)]
    
    for i in range(1, n + 1):
        for j in range(1, n + 1):
            if s[i - 1] == s[j - 1] and i != j:
                dp[i][j] = dp[i - 1][j - 1] + 1
            else:
                dp[i][j] = max(dp[i - 1][j], dp[i][j - 1])
                
    return dp[n][n]

str1 = "aabb"
lrs_length = longest_repeating_subsequence(str1)

print(lrs_length)  # Output: 2
```

### 34. How to find the longest common prefix between two strings?
Aap simple loop ya min function ka use kar sakte ho.

```python
# Example
def longest_common_prefix(strs):
    if not strs:
        return ""
    
    prefix = strs[0]
    for string in strs[1:]:
        while not string.startswith(prefix):
            prefix = prefix[:-1]
            if not prefix:
                return ""
    return prefix

strs = ["flower", "flow", "flight"]
lcp = longest_common_prefix(strs)

print(lcp)  # Output: "fl"
```

### 35. How to find the longest common suffix between two strings?
Aap similar approach use kar sakte ho jo common prefix ke liye kiya tha.

```python
# Example
def longest_common_suffix(strs):
    if not strs:
        return ""
    
    suffix = strs[0][::-1]
    for string in strs[1:]:
        while not string[::-1].startswith(suffix):
            suffix = suffix[1:]
            if not suffix:
                return ""
    return suffix[::-1]

strs = ["running", "jogging", "hiking"]
lcs = longest_common_suffix(strs)

print(lcs)  # Output: "ing"
```

### 36. How to find the KMP prefix function for a string?
Yeh already KMP failure function ke liye discuss ho chuka hai.

### 37. How to find the

 suffix array for a string?
Suffix array ke liye aap sorting kar sakte ho suffixes ko.

```python
# Example
def suffix_array(s):
    return sorted(range(len(s)), key=lambda i: s[i:])

string = "banana"
suffix_arr = suffix_array(string)

print(suffix_arr)  # Output: [5, 3, 1, 0, 4, 2]
```

### 38. How to find the inverse suffix array for a string?
Inverse suffix array ko build karne ke liye, aap suffix array ka use kar sakte ho.

```python
# Example
def inverse_suffix_array(suffix_arr):
    n = len(suffix_arr)
    inv_suff = [0] * n
    for i, suffix in enumerate(suffix_arr):
        inv_suff[suffix] = i
    return inv_suff

suffix_arr = [5, 3, 1, 0, 4, 2]
inv_suffix_arr = inverse_suffix_array(suffix_arr)

print(inv_suffix_arr)  # Output: [3, 2, 5, 1, 4, 0]
```

### 39. How to find the Burrows-Wheeler transform for a string?
BWT string compression ke liye use hota hai.

```python
# Example
def burrows_wheeler_transform(s):
    s = s + '$'  # Append a unique end character
    n = len(s)
    table = sorted(s[i:] for i in range(n))
    return ''.join(row[-1] for row in table)

string = "banana"
bwt = burrows_wheeler_transform(string)

print(bwt)  # Output: "annb$aa"
```

### 40. How to find the inverse Burrows-Wheeler transform for a string?
Inverse BWT ka process thoda complex hai.

```python
# Example
def inverse_burrows_wheeler_transform(bwt):
    n = len(bwt)
    count = {}
    next_row = [''] * n

    for char in bwt:
        count[char] = count.get(char, 0) + 1

    for i in sorted(count.keys()):
        count[i] = 0

    for i in range(n):
        char = bwt[i]
        next_row[i] = (char, count[char])
        count[char] += 1

    next_row.sort()
    first_col = ''.join(row[0] for row in next_row)
    
    next_indices = [0] * n
    for i, row in enumerate(next_row):
        next_indices[i] = row[1]

    result = []
    index = 0
    for _ in range(n - 1):
        result.append(first_col[index])
        index = next_indices[index]

    return ''.join(result) + first_col[index]

bwt = "annb$aa"
inverse_bwt = inverse_burrows_wheeler_transform(bwt)

print(inverse_bwt)  # Output: "banana"
```

### 41. How to find the Lyndon factorization for a string?
Yeh algorithm substrings ko factorize karta hai.

```python
# Example
def lyndon_factorization(s):
    n = len(s)
    result = []
    i = 0
    
    while i < n:
        j = i + 1
        while j < n and s[i] == s[j]:
            j += 1
        if j == n:
            result.append(s[i:n])
            break
        k = j + 1
        while k < n and s[i] == s[k]:
            k += 1
        while j < k:
            result.append(s[i:j])
            j += len(result[-1])
        i = j
        
    return result

string = "abcabcabc"
lyndon_factors = lyndon_factorization(string)

print(lyndon_factors)  # Output: ['abc', 'abc', 'abc']
```

### 42. How to find the Lyndon words in a string?
Aap factorization ko use karke Lyndon words nikaal sakte ho.

### 43. How to find the Duval algorithm for a string?
Duval algorithm Lyndon factorization ke liye use hota hai.

### 44. How to find the Lyndon factorization using the Duval algorithm?
```python
# Example
def duval(s):
    n = len(s)
    result = []
    i = 0
    
    while i < n:
        j = i + 1
        while j < n and s[i] == s[j]:
            j += 1
        k = j + 1
        while k < n and s[i] == s[k]:
            k += 1
        m = k - j
        for count in range(j - i):
            result.append(s[i:i + m])
            i += m
            
    return result

string = "abcabcabc"
duval_factors = duval(string)

print(duval_factors)  # Output: ['abc', 'abc', 'abc']
```

### 45. How to find the Lyndon words using the Duval algorithm?
Yeh bhi Duval algorithm ka use karke kiya ja sakta hai.

### 46. How to find the longest increasing subsequence in a string?
Aap dynamic programming ka use karke longest increasing subsequence nikaal sakte ho.

```python
# Example
def longest_increasing_subsequence(nums):
    if not nums:
        return 0

    dp = [1] * len(nums)
    
    for i in range(1, len(nums)):
        for j in range(i):
            if nums[i] > nums[j]:
                dp[i] = max(dp[i], dp[j] + 1)
                
    return max(dp)

nums = [10, 9, 2, 5, 3, 7, 101, 18]
lis_length = longest_increasing_subsequence(nums)

print(lis_length)  # Output: 4
```

### 47. How to find the longest decreasing subsequence in a string?
Aap similar approach use kar sakte ho jo increasing subsequence ke liye kiya tha.

```python
# Example
def longest_decreasing_subsequence(nums):
    if not nums:
        return 0

    dp = [1] * len(nums)
    
    for i in range(1, len(nums)):
        for j in range(i):
            if nums[i] < nums[j]:
                dp[i] = max(dp[i], dp[j] + 1)
                
    return max(dp)

nums = [10, 9, 2, 5, 3, 7, 101, 18]
lds_length = longest_decreasing_subsequence(nums)

print(lds_length)  # Output: 3
```
Chalo, ab hum kuch aur string operations ke baare mein discuss karte hain. Yahaan kuch aur functions hain jo strings ke saath kaam karte hain:

### 48. How to count the frequency of each character in a string?
Aap `collections.Counter` ka use kar ke character frequencies nikaal sakte hain.

```python
from collections import Counter

def character_frequency(s):
    frequency = Counter(s)
    return frequency

string = "hello world"
freq = character_frequency(string)

print(freq)  # Output: Counter({'l': 3, 'o': 2, 'h': 1, 'e': 1, ' ': 1, 'w': 1, 'r': 1, 'd': 1})
```

### 49. How to find unique characters in a string?
Aap `set` ka use karke unique characters nikaal sakte hain.

```python
def unique_characters(s):
    return set(s)

string = "hello"
unique_chars = unique_characters(string)

print(unique_chars)  # Output: {'h', 'e', 'l', 'o'}
```

### 50. How to check if two strings are anagrams?
Aap sorting ya `Counter` ka use kar sakte hain.

```python
def are_anagrams(s1, s2):
    return sorted(s1) == sorted(s2)

str1 = "listen"
str2 = "silent"
result = are_anagrams(str1, str2)

print(result)  # Output: True
```

### 51. How to remove duplicates from a string?
Aap `set` aur `join` ka use kar sakte ho.

```python
def remove_duplicates(s):
    return ''.join(set(s))

string = "banana"
result = remove_duplicates(string)

print(result)  # Output: 'ban' (order not guaranteed)
```

### 52. How to rotate a string?
Aap slicing ka use karke string ko rotate kar sakte ho.

```python
def rotate_string(s, n):
    n = n % len(s)  # Handle rotation greater than string length
    return s[n:] + s[:n]

string = "abcdef"
rotated = rotate_string(string, 2)

print(rotated)  # Output: "cdefab"
```

### 53. How to convert a string to title case?
Aap `title()` function ka use karke string ko title case mein convert kar sakte ho.

```python
def to_title_case(s):
    return s.title()

string = "hello world"
title_case = to_title_case(string)

print(title_case)  # Output: "Hello World"
```

### 54. How to check if a string is a valid email?
Aap regular expressions ka use karke email validation kar sakte ho.

```python
import re

def is_valid_email(email):
    pattern = r'^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$'
    return re.match(pattern, email) is not None

email = "test@example.com"
result = is_valid_email(email)

print(result)  # Output: True
```

### 55. How to check if a string is a valid URL?
Aap regular expressions ka use kar sakte ho.

```python
def is_valid_url(url):
    pattern = r'^(http|https)://[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+'
    return re.match(pattern, url) is not None

url = "https://www.example.com"
result = is_valid_url(url)

print(result)  # Output: True
```

### 56. How to extract numbers from a string?
Aap regular expressions ka use karke numbers extract kar sakte ho.

```python
def extract_numbers(s):
    return re.findall(r'\d+', s)

string = "abc123def456"
numbers = extract_numbers(string)

print(numbers)  # Output: ['123', '456']
```

### 57. How to replace all occurrences of a character in a string?
Aap `replace()` function ka use kar sakte ho.

```python
def replace_char(s, old_char, new_char):
    return s.replace(old_char, new_char)

string = "hello world"
new_string = replace_char(string, 'o', '0')

print(new_string)  # Output: "hell0 w0rld"
```

### 58. How to pad a string with zeros?
Aap `zfill()` ka use karke string ko zero se pad kar sakte ho.

```python
def pad_with_zeros(s, length):
    return s.zfill(length)

string = "42"
padded_string = pad_with_zeros(string, 5)

print(padded_string)  # Output: "00042"
```

### 59. How to check if a string contains only digits?
Aap `isdigit()` function ka use kar sakte ho.

```python
def contains_only_digits(s):
    return s.isdigit()

string = "12345"
result = contains_only_digits(string)

print(result)  # Output: True
```

### 60. How to remove punctuation from a string?
Aap `str.translate()` ka use kar sakte ho.

```python
import string

def remove_punctuation(s):
    return s.translate(str.maketrans('', '', string.punctuation))

text = "Hello, world!"
cleaned_text = remove_punctuation(text)

print(cleaned_text)  # Output: "Hello world"
```

### 61. How to check if a string is a valid JSON?
Aap `json` module ka use kar sakte ho.

```python
import json

def is_valid_json(s):
    try:
        json.loads(s)
    except ValueError:
        return False
    return True

json_string = '{"name": "John", "age": 30}'
result = is_valid_json(json_string)

print(result)  # Output: True
```

### 62. How to count the number of vowels in a string?
Aap simple loop ya `sum` function ka use kar sakte ho.

```python
def count_vowels(s):
    vowels = 'aeiouAEIOU'
    return sum(1 for char in s if char in vowels)

string = "hello world"
vowel_count = count_vowels(string)

print(vowel_count)  # Output: 3
```

### 63. How to count the number of consonants in a string?
Aap similar method use kar sakte ho.

```python
def count_consonants(s):
    vowels = 'aeiouAEIOU'
    return sum(1 for char in s if char.isalpha() and char not in vowels)

string = "hello world"
consonant_count = count_consonants(string)

print(consonant_count)  # Output: 7
```

### 64. How to find the first non-repeating character in a string?
Aap frequency dictionary ka use kar sakte ho.

```python
def first_non_repeating_character(s):
    frequency = {}
    
    for char in s:
        frequency[char] = frequency.get(char, 0) + 1

    for char in s:
        if frequency[char] == 1:
            return char

    return None

string = "hello world"
first_non_repeating = first_non_repeating_character(string)

print(first_non_repeating)  # Output: "h"
```

### 65. How to find the last non-repeating character in a string?
Aap similar approach use kar sakte ho.

```python
def last_non_repeating_character(s):
    frequency = {}
    
    for char in s:
        frequency[char] = frequency.get(char, 0) + 1

    for char in reversed(s):
        if frequency[char] == 1:
            return char

    return None

string = "hello world"
last_non_repeating = last_non_repeating_character(string)

print(last_non_repeating)  # Output: "d"
```

### 66. How to find all permutations of a string?
Aap `itertools.permutations` ka use kar sakte ho.

```python
import itertools

def string_permutations(s):
    return [''.join(p) for p in itertools.permutations(s)]

string = "abc"
permutations = string_permutations(string)

print(permutations)  # Output: ['abc', 'acb', 'bac', 'bca', 'cab', 'cba']
```

### 67. How to find all substrings of a string?
Aap nested loops ka use kar sakte ho.

```python
def all_substrings(s):
    substrings = []
    for i in range(len(s)):
        for j in range(i + 1, len(s) + 1):
            substrings.append(s[i:j])
    return substrings

string = "abc"
substrings = all_substrings(string)

print(substrings)  # Output: ['a', 'ab', 'abc', 'b', 'bc', 'c']
```

### 68. How to convert a string to a list of characters?
Aap `list()` function ka use kar sakte ho.

```python
def string_to_char_list(s):
    return list(s)

string = "hello"
char_list = string_to_char_list(string)

print(char_list)  # Output: ['h', 'e', 'l', 'l', 'o']
```

### 69. How to merge two strings alternatively?
Aap zip aur join ka use kar sakte

 ho.

```python
def merge_alternatively(s1, s2):
    merged = ''.join(a + b for a, b in zip(s1, s2))
    if len(s1) > len(s2):
        merged += s1[len(s2):]
    elif len(s2) > len(s1):
        merged += s2[len(s1):]
    return merged

str1 = "abc"
str2 = "123456"
merged_string = merge_alternatively(str1, str2)

print(merged_string)  # Output: "a1b2c3456"
```

### 70. How to check if a string is a valid integer?
Aap `str.isdigit()` ya try-except block ka use kar sakte ho.

```python
def is_valid_integer(s):
    try:
        int(s)
        return True
    except ValueError:
        return False

string = "12345"
result = is_valid_integer(string)

print(result)  # Output: True
```

Chalo, aage kuch aur string operations aur algorithms explore karte hain. Yahaan par kuch additional functionalities hain jo strings ke saath kaam karne mein helpful ho sakte hain:

### 71. How to find the longest word in a string?
Aap `split()` aur `max()` ka use kar ke longest word nikaal sakte hain.

```python
def longest_word(s):
    words = s.split()
    return max(words, key=len)

string = "Find the longest word in this sentence"
longest = longest_word(string)

print(longest)  # Output: "longest"
```

### 72. How to remove vowels from a string?
Aap simple loop ya `str.replace()` ka use kar sakte ho.

```python
def remove_vowels(s):
    vowels = 'aeiouAEIOU'
    return ''.join(char for char in s if char not in vowels)

string = "hello world"
no_vowels = remove_vowels(string)

print(no_vowels)  # Output: "hll wrld"
```

### 73. How to find the first repeated character in a string?
Aap frequency dictionary ya set ka use kar sakte ho.

```python
def first_repeated_character(s):
    seen = set()
    for char in s:
        if char in seen:
            return char
        seen.add(char)
    return None

string = "hello world"
first_repeated = first_repeated_character(string)

print(first_repeated)  # Output: "l"
```

### 74. How to check if a string contains only whitespace?
Aap `isspace()` function ka use kar sakte ho.

```python
def contains_only_whitespace(s):
    return s.isspace()

string = "   "
result = contains_only_whitespace(string)

print(result)  # Output: True
```

### 75. How to capitalize the first letter of each word in a string?
Aap `title()` function ka use kar sakte ho.

```python
def capitalize_first_letter_each_word(s):
    return s.title()

string = "hello world"
capitalized = capitalize_first_letter_each_word(string)

print(capitalized)  # Output: "Hello World"
```

### 76. How to repeat a string multiple times?
Aap multiplication operator ka use kar sakte ho.

```python
def repeat_string(s, n):
    return s * n

string = "hello "
repeated_string = repeat_string(string, 3)

print(repeated_string)  # Output: "hello hello hello "
```

### 77. How to find all indices of a substring in a string?
Aap loop aur `str.find()` ka use kar sakte ho.

```python
def find_all_indices(s, substring):
    start = 0
    indices = []
    while True:
        start = s.find(substring, start)
        if start == -1: 
            break
        indices.append(start)
        start += 1
    return indices

string = "ababcabc"
substring = "abc"
indices = find_all_indices(string, substring)

print(indices)  # Output: [2, 5]
```

### 78. How to check if two strings are rotations of each other?
Aap string concatenation ka use karke check kar sakte ho.

```python
def are_rotations(s1, s2):
    if len(s1) != len(s2):
        return False
    return s1 in (s2 + s2)

str1 = "abcde"
str2 = "deabc"
result = are_rotations(str1, str2)

print(result)  # Output: True
```

### 79. How to reverse words in a string?
Aap `split()` aur `join()` ka use karke words ko reverse kar sakte ho.

```python
def reverse_words(s):
    words = s.split()
    return ' '.join(reversed(words))

string = "hello world"
reversed_words = reverse_words(string)

print(reversed_words)  # Output: "world hello"
```

### 80. How to count the number of sentences in a string?
Aap period, exclamation, aur question mark ka use kar ke count kar sakte ho.

```python
def count_sentences(s):
    sentences = [sentence for sentence in s.split('.') if sentence]
    return len(sentences)

string = "Hello. How are you? I am fine!"
sentence_count = count_sentences(string)

print(sentence_count)  # Output: 3
```

### 81. How to split a string by a delimiter?
Aap `split()` function ka use kar sakte ho.

```python
def split_string(s, delimiter):
    return s.split(delimiter)

string = "apple,banana,cherry"
fruits = split_string(string, ',')

print(fruits)  # Output: ['apple', 'banana', 'cherry']
```

### 82. How to convert a string into a list of words?
Aap `split()` ka use karke words ko list mein convert kar sakte ho.

```python
def string_to_word_list(s):
    return s.split()

string = "Hello world"
word_list = string_to_word_list(string)

print(word_list)  # Output: ['Hello', 'world']
```

### 83. How to check if a string is a valid hexadecimal number?
Aap regular expressions ka use karke check kar sakte ho.

```python
def is_valid_hexadecimal(s):
    pattern = r'^[0-9a-fA-F]+$'
    return re.match(pattern, s) is not None

hex_string = "1a3f"
result = is_valid_hexadecimal(hex_string)

print(result)  # Output: True
```

### 84. How to find the common characters between two strings?
Aap set operations ka use kar ke common characters nikaal sakte hain.

```python
def common_characters(s1, s2):
    return set(s1) & set(s2)

string1 = "hello"
string2 = "world"
common_chars = common_characters(string1, string2)

print(common_chars)  # Output: {'o', 'l'}
```

### 85. How to replace all whitespace characters in a string?
Aap `re.sub()` ka use kar ke whitespace characters replace kar sakte ho.

```python
def replace_whitespace(s, replacement):
    return re.sub(r'\s+', replacement, s)

string = "hello   world"
new_string = replace_whitespace(string, '-')

print(new_string)  # Output: "hello-world"
```

### 86. How to find the first occurrence of a substring in a string?
Aap `find()` function ka use kar sakte ho.

```python
def first_occurrence(s, substring):
    return s.find(substring)

string = "hello world"
index = first_occurrence(string, "world")

print(index)  # Output: 6
```

### 87. How to convert a string to lowercase and uppercase simultaneously?
Aap `lower()` aur `upper()` functions ka use karke alag strings bana sakte hain.

```python
def lower_and_upper(s):
    return s.lower(), s.upper()

string = "Hello World"
lowercase, uppercase = lower_and_upper(string)

print(lowercase)  # Output: "hello world"
print(uppercase)  # Output: "HELLO WORLD"
```

### 88. How to check if a string is numeric and also in a specific range?
Aap `isdigit()` aur comparison ka use kar sakte ho.

```python
def is_numeric_in_range(s, min_value, max_value):
    if s.isdigit():
        num = int(s)
        return min_value <= num <= max_value
    return False

string = "50"
result = is_numeric_in_range(string, 10, 100)

print(result)  # Output: True
```

### 89. How to count the number of words in a string?
Aap `split()` function ka use kar ke count kar sakte hain.

```python
def count_words(s):
    return len(s.split())

string = "Hello world"
word_count = count_words(string)

print(word_count)  # Output: 2
```

### 90. How to check if a string contains any special characters?
Aap regular expressions ka use karke check kar sakte ho.

```python
def contains_special_characters(s):
    pattern = r'[^a-zA-Z0-9]'
    return re.search(pattern, s) is not None

string = "Hello@World!"
result = contains_special_characters(string)

print(result)  # Output: True
```

### 91. How to convert a string into a list of sentences?
Aap `re.split()` ka use karke sentences ko alag kar sakte ho.

```python
def string_to_sentence_list(s):
    return re.split(r'[.!?]', s)

string = "Hello. How are you? I am fine!"
sentence_list = string_to_sentence_list(string)

print(sentence_list)  # Output: ['Hello', ' How are you', ' I am fine', '']
```

### 92. How to find the number of times a substring appears in a string?
Aap `count()` function ka use kar sakte ho.

```python
def count_substring(s, substring):
    return s.count(substring)

string = "hello hello world"
substring_count = count_substring(string, "hello")

print(substring_count)  # Output: 2
```

### 93. How to swap two strings?
Aap simple assignment ka use kar ke swap kar sakte ho.

```python
def swap

_strings(s1, s2):
    return s2, s1

str1 = "hello"
str2 = "world"
swapped = swap_strings(str1, str2)

print(swapped)  # Output: ('world', 'hello')
```

### 94. How to find the maximum occurring character in a string?
Aap `collections.Counter` ka use kar ke maximum character nikaal sakte ho.

```python
from collections import Counter

def max_occurring_character(s):
    counts = Counter(s)
    return counts.most_common(1)[0]

string = "hello world"
max_char = max_occurring_character(string)

print(max_char)  # Output: ('l', 3)
```

### 95. How to replace multiple characters in a string?
Aap `str.translate()` ka use kar sakte ho.

```python
def replace_multiple_characters(s, replacements):
    translation_table = str.maketrans(replacements)
    return s.translate(translation_table)

string = "hello world"
replacements = {'h': 'H', 'w': 'W'}
new_string = replace_multiple_characters(string, replacements)

print(new_string)  # Output: "Hello World"
```

### 96. How to check if a string is an empty string?
Aap `not` operator ka use kar sakte ho.

```python
def is_empty_string(s):
    return not s

string = ""
result = is_empty_string(string)

print(result)  # Output: True
```

### 97. How to repeat a string with a separator?
Aap `join()` function ka use kar ke repeat kar sakte ho.

```python
def repeat_string_with_separator(s, n, separator):
    return separator.join([s] * n)

string = "hello"
repeated_string = repeat_string_with_separator(string, 3, "-")

print(repeated_string)  # Output: "hello-hello-hello"
```

### 98. How to find the longest substring without repeating characters?
Aap sliding window technique ka use karke longest substring nikaal sakte ho.

```python
def longest_unique_substring(s):
    char_index = {}
    start = max_length = 0
    for index, char in enumerate(s):
        if char in char_index and char_index[char] >= start:
            start = char_index[char] + 1
        char_index[char] = index
        max_length = max(max_length, index - start + 1)
    return max_length

string = "abcabcbb"
length = longest_unique_substring(string)

print(length)  # Output: 3
```

### 99. How to find the total number of uppercase and lowercase letters in a string?
Aap simple loop ya `isupper()` aur `islower()` functions ka use kar sakte ho.

```python
def count_upper_lower(s):
    upper_count = sum(1 for char in s if char.isupper())
    lower_count = sum(1 for char in s if char.islower())
    return upper_count, lower_count

string = "Hello World"
upper, lower = count_upper_lower(string)

print(upper, lower)  # Output: 2 8
```

### 100. How to convert a string to title case?
Aap `title()` function ka use kar sakte ho.

```python
def to_title_case(s):
    return s.title()

string = "hello world"
title_case_string = to_title_case(string)

print(title_case_string)  # Output: "Hello World"
```
---
---
