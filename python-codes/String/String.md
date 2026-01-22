# Strings in Python

## Introduction

A string is a sequence of characters enclosed in quotes (single `'`, double `"`, or triple `'''` or `"""`). Strings are immutable in Python, meaning once created, they cannot be changed.

```python
s = "Hello, World!"
s1 = 'Welcome to Python'
s2 = """Multi-line
string example"""
```

---

## Indexing and Slicing

### Indexing
Indexing allows you to access individual characters from a string using their position. Python uses 0-based indexing.

```python
s = "welcome to bhopal"
print(s[0])   # Output: w
print(s[1])   # Output: e
print(s[-1])  # Output: l (last character)
```

### Slicing
Slicing extracts a substring from a string using the syntax: `string[start:stop:step]`
- **start**: Starting index (default: 0)
- **stop**: Ending index (exclusive, default: end of string)
- **step**: Step value (default: 1)

```python
s = "welcome to bhopal"

print(s[::-1])      # Reverse the string
print(s[1::3])      # Every 3rd character starting from index 1
print(s[-1::-2])    # Every 2nd character in reverse
print(s[1:6:2])     # Characters from index 1 to 6 with step 2
print(s[0:7:])      # Characters from 0 to 7
print(s[-1:-14:-2]) # Characters in reverse with step -2
```

---

## Iteration

### Direct Iteration
Iterate through each character in a string directly.

```python
s = "decode"
for i in s:
    print(i)  # Prints each character on a new line
```

### Indirect Iteration
Iterate using indices and the `range()` function.

```python
s = "decode"
for i in range(len(s)):
    print(i, s[i])  # Prints index and character
```

---

## String Programs

### Reverse a String
```python
s = input("Enter any string: ")
rev = ""
for i in s:
    rev = i + rev
print(rev)      # Manual reversal
print(s[::-1])  # Using slicing
```

### Check if String is Palindrome
```python
s = input("Enter any string: ")
if s == s[::-1]:
    print(s, "is a palindrome")
else:
    print(s, "is not a palindrome")
```

### Count Vowels, Consonants, and Spaces
```python
s1 = "welcome to city of lakes"
vowels = 0
consonants = 0
spaces = 0

for i in s1:
    if i in "aeiouAEIOU":
        vowels += 1
    elif i == " ":
        spaces += 1
    else:
        consonants += 1

print("Vowels:", vowels)
print("Consonants:", consonants)
print("Spaces:", spaces)
```

---

## String Functions

### Length
```python
s = "decode"
print(len(s))  # Output: 6
```

### Character and ASCII Conversion
```python
# chr(number) - Convert ASCII value to character
print(chr(66))    # Output: B
print(chr(97))    # Output: a

# ord(character) - Convert character to ASCII value
print(ord("a"))   # Output: 97
print(ord("A"))   # Output: 65
print(ord("@"))   # Output: 64
```

### Maximum and Minimum Characters
```python
s = "decode"
print(max(s))  # Output: o (lexicographically largest)
print(min(s))  # Output: c (lexicographically smallest)
```

---

## String Methods

### Case Conversion

| Method | Description | Example |
|--------|-------------|---------|
| `upper()` | Convert to uppercase | `s.upper()` |
| `lower()` | Convert to lowercase | `s.lower()` |
| `title()` | Capitalize first letter of each word | `s.title()` |
| `capitalize()` | Capitalize first letter only | `s.capitalize()` |
| `swapcase()` | Swap case of all letters | `s.swapcase()` |

```python
s = "welcome to bhopal"
print(s.upper())       # WELCOME TO BHOPAL
print(s.lower())       # welcome to bhopal
print(s.title())       # Welcome To Bhopal
print(s.capitalize())  # Welcome to bhopal
```

### Checking Methods

| Method | Description | Returns |
|--------|-------------|---------|
| `isalpha()` | Check if all characters are alphabetic | Boolean |
| `isdigit()` | Check if all characters are digits | Boolean |
| `isalnum()` | Check if all characters are alphanumeric | Boolean |
| `isspace()` | Check if all characters are whitespace | Boolean |
| `islower()` | Check if all letters are lowercase | Boolean |
| `isupper()` | Check if all letters are uppercase | Boolean |
| `isidentifier()` | Check if string is valid identifier | Boolean |

```python
s = "decode"
s1 = "decode1234"

print(s.isalpha())        # True
print(s1.isalpha())       # False

print("1234".isdigit())   # True
print(s1.isalnum())       # True

print(s.islower())        # True
print(s.isupper())        # False
```

### String Search and Replace

| Method | Description |
|--------|-------------|
| `find()` | Find first occurrence of substring |
| `rfind()` | Find last occurrence of substring |
| `count()` | Count occurrences of substring |
| `replace()` | Replace substring with another string |
| `startswith()` | Check if string starts with prefix |
| `endswith()` | Check if string ends with suffix |

```python
s = "welcome to bhopal"

print(s.find("o"))          # First occurrence of 'o'
print(s.count("o"))         # Count of 'o'
print(s.replace("bhopal", "india"))  # Replace substring
print(s.startswith("wel"))  # True
print(s.endswith("pal"))    # True
```

### String Splitting and Joining

```python
s = "Hello, World, Python"

# split()
words = s.split(", ")  # ['Hello', 'World', 'Python']

# join()
result = " - ".join(words)  # 'Hello - World - Python'

# strip() - Remove leading/trailing whitespace
s2 = "  hello  "
print(s2.strip())  # 'hello'
```

---

## Alphabet Patterns

Using string methods and ASCII values to create patterns:

```python
# Pattern 1: Increasing alphabets
n = 5
for i in range(n):
    for j in range(i + 1):
        print(chr(65 + j), end=" ")
    print()

# Pattern 2: Right-aligned pyramid
n = 5
for i in range(n):
    for j in range(n - i - 1):
        print(" ", end=" ")
    for j in range(i + 1):
        print(chr(65 + j), end=" ")
    print()

# Pattern 3: Diamond pattern with letters
n = 5
for i in range(n):
    for j in range(n - i):
        print(" ", end=" ")
    for k in range(i + 1):
        print(chr(65 + k), end=" ")
    for l in range(k):
        print(chr(65 + l), end=" ")
    print()
```

---

## Key Points

- Strings are **immutable** - once created, they cannot be changed
- Use **indexing** to access individual characters (0-based indexing)
- Use **slicing** to extract substrings
- Python provides many built-in **string methods** for manipulation
- **ASCII values** can be converted using `ord()` and `chr()`
- Strings support **iteration** for processing each character
- **f-strings** (formatted strings) provide easy string formatting: `f"Hello {name}"`

---

