# Tuples in Python

## What is a Tuple?

A **tuple** is a collection of elements in Python that is:
- **Ordered**: Elements maintain their position and can be accessed by index
- **Immutable**: Once created, tuples cannot be modified (no adding, removing, or changing elements)
- **Heterogeneous**: Can contain elements of different data types in a single tuple
- **Denoted by parentheses**: Use `()` to define a tuple

## Creating Tuples

### Empty Tuple
```python
empty_tuple = ()
print(empty_tuple)  # Output: ()
print(type(empty_tuple))  # Output: <class 'tuple'>
```

### Single Value Tuple
When creating a tuple with a single element, you must include a comma after the value:
```python
single_tuple = (1,)
print(single_tuple)  # Output: (1,)
print(type(single_tuple))  # Output: <class 'tuple'>
```

### Multiple Element Tuple (Heterogeneous)
```python
my_tuple = (12, "hello", 13, 14, 14.5, 15)
print(my_tuple)  # Output: (12, 'hello', 13, 14, 14.5, 15)
print(type(my_tuple))  # Output: <class 'tuple'>
```

## Accessing Tuple Elements

Tuples are **indexed** (0-based indexing) and **ordered**:
```python
my_tuple = (12, "hello", 13, 14, 14.5, 15)
print(my_tuple[0])  # Output: 12 (first element)
```

### Iterating Through a Tuple
```python
my_tuple = (12, "hello", 13, 14, 14.5, 15)
for i in my_tuple:
    print(i)
```

## Immutability

Tuples are immutable, meaning you cannot modify their elements:
```python
my_tuple = (1, 2, 3)
my_tuple[0] = 1000  # TypeError: 'tuple' object does not support item assignment
```

## Tuple Operations

### Finding Length
```python
t = (10, 20, 30, "hello", 10.5)
print(len(t))  # Output: 5
```

You can also count elements manually:
```python
t = (10, 20, 30, "hello", 10.5)
count = 0
for i in t:
    count = count + 1
print(count)  # Output: 5
```

### Finding Maximum Value
```python
t = (10, 20, 30, 100, 10.5)
max_value = t[0]
for i in t:
    if i > max_value:
        max_value = i
print(max_value)  # Output: 100
```

### Finding Minimum Value
```python
t = (10, 20, 30, 100, 10.5)
min_value = t[0]
for i in t:
    if i < min_value:
        min_value = i
print(min_value)  # Output: 10
```

### Sorting a Tuple

Sort in ascending order (returns a list):
```python
t = (10, 20, 30, 100, 10.5)
t1 = sorted(t)
print(t1)  # Output: [10, 10.5, 20, 30, 100]
```

Sort in descending order (returns a list):
```python
t = (10, 20, 30, 100, 10.5)
t1 = sorted(t, reverse=True)
print(t1)  # Output: [100, 30, 20, 10.5, 10]
```

Reverse a tuple manually:
```python
t = (10, 20, 30, 100, 10.5)
t1 = sorted(t)
t2 = ()
for i in t1[::-1]:
    t2 = t2 + (i,)
print(t2)  # Output: (100, 30, 20, 10.5, 10)
```

## Key Characteristics

| Feature | Description |
|---------|-------------|
| **Type** | Collection data structure |
| **Syntax** | Enclosed in parentheses `()` |
| **Ordered** | Yes - maintains element position |
| **Mutable** | No - immutable (cannot be changed) |
| **Indexed** | Yes - 0-based indexing |
| **Heterogeneous** | Yes - can contain mixed data types |
| **Indexable** | Yes - access elements by index |
| **Iterable** | Yes - can loop through elements |

## Summary

Tuples are useful when you need to:
- Store multiple values of different types together
- Ensure data cannot be accidentally modified
- Use as dictionary keys (unlike lists)
- Return multiple values from a function
