# Lists in Python

A list is an ordered, mutable collection of items. Lists can hold items of different types (numbers, strings, other lists, objects, etc.). This document provides concise explanations, examples, and common operations.

## Creating lists

```python
# empty list
L = []

# from literals
nums = [1, 2, 3]
mix = [1, 'two', 3.0, [4, 5]]

# from iterable
chars = list('abc')  # ['a', 'b', 'c']
```

## Accessing items

```python
nums = [10, 20, 30, 40]
first = nums[0]
last = nums[-1]
slice_mid = nums[1:3]  # [20, 30]
```

## Common list methods

- `append(x)`: add `x` to the end
- `extend(iterable)`: extend list by each element from iterable
- `insert(i, x)`: insert `x` at index `i`
- `remove(x)`: remove first occurrence of `x` (raises `ValueError` if missing)
- `pop([i])`: remove and return item at `i` (defaults to last)
- `clear()`: remove all items
- `index(x[, start[, end]])`: return first index of `x`
- `count(x)`: count occurrences of `x`
- `sort(key=None, reverse=False)`: sort in-place
- `reverse()`: reverse in-place
- `copy()`: shallow copy of the list

Example:

```python
values = [3, 1, 4]
values.append(2)        # [3, 1, 4, 2]
values.sort()           # [1, 2, 3, 4]
val = values.pop()      # val=4, values=[1,2,3]
```

## List comprehensions

Concise and readable way to build lists:

```python
squares = [x*x for x in range(6)]  # [0,1,4,9,16,25]
evens = [x for x in range(20) if x % 2 == 0]
```

## Copying and mutability

Lists are mutable. Assignment copies the reference, not the contents:

```python
a = [1, 2]
b = a
b.append(3)
print(a)  # [1, 2, 3]

# To copy:
shallow = a.copy()        # shallow copy
import copy
deep = copy.deepcopy([[1]])  # use for nested structures
```




## Further reading

- Official docs: https://docs.python.org/3/tutorial/datastructures.html#more-on-lists

---
This file provides a focused reference and examples for working with lists in Python.
