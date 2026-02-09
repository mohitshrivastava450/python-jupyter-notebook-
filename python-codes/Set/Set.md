
# Set

## Overview

A set is an unordered, unindexed collection of unique items. Sets can contain heterogeneous immutable elements and are mutable (you can add or remove items).

## Creating sets

```python
# empty set
s = set()
print(type(s))

# literal with values
s = {10, 12.5, "hello", 100}
print(s)
```

## Key properties

- Unordered: no index, iteration order is arbitrary.
- Unique: duplicates are ignored.
- Mutable: elements can be added or removed (but elements must be hashable/immutable).

## Common methods and examples

- add(item): Add an element

```python
s = {10, 12.5, "hello", 100}
s.add(120)
print(s)
```

- pop(): Remove and return an arbitrary element

```python
item = s.pop()
print(item)
print(s)
```

- remove(item): Remove a specific element (raises KeyError if missing)

```python
s = {10, 12.5, "hello", 100}
s.remove(10)
print(s)
```

- discard(item): Remove a specific element (no error if missing)

```python
s = {10, 12.5, "hello", 100}
s.discard(10)
print(s)
```

- clear(): Remove all elements

```python
s.clear()
print(s)  # set()
```

- copy(): Shallow copy of the set

```python
a = s.copy()
```

## Set operations

- union(other): Elements in either set

```python
s = {10, 12.5, "hello", 100}
t = {10, 15, "hello", 120, 132}
print(s.union(t))
```

- intersection(other): Elements common to both

```python
print(s.intersection(t))
```

- difference(other): Elements in `s` but not in `t`

```python
print(s.difference(t))
```

- symmetric_difference(other): Elements in either set but not both

```python
print(s.symmetric_difference(t))
```

## Notes

- Iteration over a set is direct (for x in s) but order is arbitrary.
- Use `remove` when you want an error if the item is missing; use `discard` to avoid errors.

