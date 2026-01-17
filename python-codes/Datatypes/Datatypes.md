# Python Data Types

This document provides an overview of the fundamental data types in Python.  
Understanding these types is essential for writing efficient and effective Python programs.

---

## 📌 Built-in Data Types

### 1. Numeric Types
- **int**: Integer numbers (e.g., `42`, `-7`)
- **float**: Floating-point numbers (e.g., `3.14`, `-0.001`)
- **complex**: Complex numbers with real and imaginary parts (e.g., `2 + 3j`)

### 2. Sequence Types
- **list**: Ordered, mutable collection (e.g., `[1, 2, 3]`)
- **tuple**: Ordered, immutable collection (e.g., `(1, 2, 3)`)
- **range**: Immutable sequence of numbers, often used in loops (e.g., `range(5)`)

### 3. Text Type
- **str**: Unicode string (e.g., `"Hello, World!"`)

### 4. Set Types
- **set**: Unordered collection of unique elements (e.g., `{1, 2, 3}`)
- **frozenset**: Immutable version of a set

### 5. Mapping Type
- **dict**: Key-value pairs (e.g., `{"name": "Alice", "age": 25}`)

### 6. Boolean Type
- **bool**: Represents truth values `True` or `False`

### 7. Binary Types
- **bytes**: Immutable sequence of bytes (e.g., `b"hello"`)
- **bytearray**: Mutable sequence of bytes
- **memoryview**: A view object exposing buffer protocol

---

## 🧩 Type Conversion

Python provides built-in functions to convert between types:
- `int("10")` → converts string to integer
- `float(5)` → converts integer to float
- `str(3.14)` → converts float to string
- `list("abc")` → converts string to list of characters

---

## 🔍 Checking Data Types

Use the `type()` function:
```python
x = 42
print(type(x))  # <class 'int'>