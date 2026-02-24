# Pandas Library

## Introduction
Pandas is a powerful Python library for data manipulation and analysis. It provides data structures and tools for working with tabular data (like SQL tables or Excel spreadsheets).

## Installation

```python
pip install pandas
```

## Importing Pandas

```python
import pandas as pd
```

---

## Pandas Series

### Creating a Basic Series
A Pandas Series is a one-dimensional array-like object containing a sequence of values.

```python
s = pd.Series([10, 20, 30, 40, 50])
print(s)
print(s.dtype)
```

### Creating Series from a List

```python
l = [10, 20, 30, 40]
s = pd.Series(l)
print(s)
```

### Creating Series with Custom Index, Name, and Data Type

```python
l = [10, 20, 30, 40]
s = pd.Series(l, index=["A", "B", "C", "D"], name="python", dtype="float")
print(s)
```

### Creating Series from a Dictionary

```python
d = {"A": [10, 20, 30, 40, 50], "B": [100, 200, 300, 400]}
s1 = pd.Series(d)
print(s1)
print(type(s1))
print(s1["A"])
```

### Creating Series with Repeated Values

```python
s = pd.Series(12, index=[1, 2, 3, 4, 5, 6, 7])
print(s)
```

### Series Arithmetic Operations

```python
s1 = pd.Series(12, index=[1, 2, 3, 4, 5, 6, 7])
s2 = pd.Series(12, index=[1, 2, 3, 4])
s3 = s1 + s2
print(s3)
```

---

## Pandas DataFrame

### Creating a DataFrame from a Dictionary

```python
dic = {"A": [10, 20, 30, 40, 50], "B": [100, 200, 300, 400, 500]}
df = pd.DataFrame(dic)
print(df)
print(type(df))
print(df["A"])
```

### Creating DataFrame with Custom Parameters

```python
dic = {"A": [10, 20, 30, 40, 50], "B": [100, 200, 300, 400, 500], 
       1: [1000, 2000, 3000, 4000, 5000], "S": [1, 2, 3, 4, 5]}
df = pd.DataFrame(dic, columns=["A", 1], index=["a", "s", "d", "e", "f"], dtype="float")
print(df)
```

### Creating DataFrame from a List

```python
l = [[10, 20, 30, 40, 50], [100, 200, 300, 400, 500]]
df = pd.DataFrame(l)
print(df)
```

### Creating DataFrame from Series Dictionary

```python
d = {"A": pd.Series([1, 2, 3, 4]), "B": pd.Series([1, 2, 3, 4])}
df = pd.DataFrame(d)
print(df)
print(df["A"][2])
```

---

## DataFrame Arithmetic Operations

### Addition

```python
df = pd.DataFrame({"A": [10, 20, 30, 40, 50], "B": [1, 2, 3, 4, 5]})
df["C"] = df["A"] + df["B"]
print(df)
```

### Subtraction

```python
df["C"] = df["A"] - df["B"]
print(df)
```

### Multiplication

```python
df["C"] = df["A"] * df["B"]
print(df)
```

### Division

```python
df["C"] = df["A"] / df["B"]
print(df)
```

### Modulo

```python
df["C"] = df["A"] % df["B"]
print(df)
```

### Power

```python
df["C"] = df["A"] ** df["B"]
print(df)
```

---

## DataFrame Comparison Operations

```python
df = pd.DataFrame({"A": [10, 20, 30, 40, 50], "B": [1, 2, 3, 4, 5]})
df["python"] = df["A"] <= 30
df["python_1"] = df["B"] >= 3
print(df)
```

---

## Adding and Removing Columns

### Inserting a Column at a Specific Position

```python
df.insert(1, "python_2", df["A"])
print(df)
```

### Inserting a Column with Values

```python
df.insert(2, "python_3", [10, 20, 30, 40, 50])
print(df)
```

### Removing a Column with pop()

```python
py = df.pop("python_3")
print(py)
```

### Removing a Column with del

```python
del df["python_3"]
print(df)
```

---

## Reading and Writing CSV Files

### Reading a CSV File

```python
df = pd.read_csv(r"C:\Users\Rohit shrivastava\Downloads\previous_application.csv")
print(df)
```

### Writing a DataFrame to CSV

```python
df = pd.DataFrame({"A": [10, 20, 30, 40, 50], "B": [1, 2, 3, 4, 5]})
df.to_csv(r"C:\Users\Rohit shrivastava\Desktop\newfile.csv", index=False)
print(df)
```