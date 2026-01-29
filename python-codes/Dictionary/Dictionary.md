# DICTIONARY

## Introduction to Dictionary

A dictionary is an unordered collection of key-value pairs. It is mutable and allows for efficient lookup of values using their keys.

### Creating an Empty Dictionary

```python
d={}  # empty
print(d)
print(type(d))
```

## Creating and Accessing Dictionaries

### Creating a Dictionary with Values

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d)
print(d["name"])  # access values with the help of key
d["name"]="xyz"
print(d)
d["Name"]="xyz"
print(d)
```

### Adding Items to a Dictionary

```python
d={}
d["name"]="xyz"
print(d)
```

## Dictionary from Lists

### Creating a Dictionary by Squaring List Elements

```python
l=[1,5,6,4,3,7]
l1={}
for i in l:
    l1[i]=i**2
print(l1)
```

### Creating a Dictionary with ASCII Characters

```python
l={}
for i in range(1,6,1):
    l[chr(64+i)]=i**3
print(l)
```

### Counting Frequency of Elements

```python
l=["red","green","red","yellow","green","red","Yellow"]
l1={}
for i in l:
    if i in l1:
        l1[i]+=1
    else:
        l1[i]=1
print(l1)
```

## Iteration Through Dictionaries

### Basic Dictionary Iteration

```python
l={"name":["a","b","c"],"age":[13,23,42],"city":["bhopal","indore","ujjain"]}
print(l)
for i in l:
    print(l[i])
```

### Iterating Through Keys

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
for i in d:
    print(d[i])
```

### Nested Iteration (Key and Values)

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
for i in d:
    for j in d[i]:
        print(j)
```

## Dictionary Methods

### get() Method

The `get()` method returns the value for a given key.

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d.get("name"))
for i in d.get("name"):
    print(i)
```

### keys() Method

The `keys()` method returns all the keys in the dictionary.

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d.keys())
for i in (d.keys()):
    print(i)
```

### values() Method

The `values()` method returns all the values in the dictionary.

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d.values())
for i in (d.values()):
    print(i)
```

### items() Method

The `items()` method returns all key-value pairs as tuples.

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d.items())
for i in (d.items()):
    print(i)
```

### items() with Unpacking

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d.items())
for i,j in (d.items()):
    print(i,j)
```

## Finding Mode Using Dictionary

### Finding the Most Frequent Element

```python
l=[1,1,3,3,3,3,3,4,6,6,6]
d={}
for i in l:
    if i in d:
        d[i]+=1
    else:
        d[i]=1
print(d)
max_value=max(d.values())
print(max_value)
mode=[i for i,j in d.items() if j==max_value]
print(mode)
```

### Another Mode Example

```python
l=[1,5,3,4,5,1,6,7,7,5,9,11,5,8]
d={}
for i in l:
    if i in d:
        d[i]+=1
    else:
        d[i]=1
print(d)
max_value=max(d.values())
print(max_value)
mode=[i for i,j in d.items() if j==max_value]
print(mode)
```

## pop() Method

The `pop()` method removes and returns the value for a given key.

### Removing Dictionary Keys

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d.pop("name"))
print(d)
```

### Removing Items from List Values

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d["name"].pop())
print(d)
```

## popitem() Method

The `popitem()` method removes and returns the last key-value pair as a tuple.

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
print(d.popitem())
print(d)
```

## del Keyword

The `del` keyword removes a key-value pair from the dictionary.

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
del d["name"]
print(d)
```

## clear() Method

The `clear()` method removes all items from the dictionary.

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
d.clear()
print(d)
```

## update() Method

The `update()` method adds or updates key-value pairs in the dictionary.

### Using Dictionary Argument

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
d.update({"city":["jbp","bpl","gwl"]})
print(d)
```

### Using Keyword Arguments

```python
d={"name":["abc","def","pqr"],"courses":["DA","DS","DE"],"fees":[25000,35000,30000]}
d.update(city=["jbp","bpl","gwl"])
print(d)
```

## dict() Constructor

The `dict()` constructor creates a dictionary using keyword arguments.

```python
d=dict(name=["abc","def","pqr"],city=["jbp","bpl","gwl"])
print(d)
```

## Dictionary Comprehension

Dictionary comprehension is a concise way to create a new dictionary from an existing iterable.

### Basic Dictionary Comprehension

```python
d={}
for i in range(2,11,2):
    d[i]=i**2
print(d)
print({i:i**2 for i in range(2,11,2)})
```

### Dictionary Comprehension with List

```python
d={}
l=[1,2,3,4,5]
for i in l:
    d[i]=i**3
print(d)
print({i:i**3 for i in l})
```

### Dictionary Comprehension with Conditional

Mapping numbers to "even" or "odd" for numbers greater than 3:

```python
number=range(10)
d={}
for i in number:
    if i>3:
        if i%2==0:
            d[i]="even"
        else:
            d[i]="odd"
print(d)
print({i:("even" if i%2==0 else "odd") for i in number if i>3})
```
