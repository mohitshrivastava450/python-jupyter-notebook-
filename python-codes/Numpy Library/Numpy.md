
# NumPy — Basics and Examples

This document summarizes examples from the notebook `NUMPY.ipynb` and shows common NumPy usage with runnable code snippets.

## Installation

Install NumPy (and plotting libs when needed):

```bash
pip install numpy matplotlib seaborn
```

## Import

```python
import numpy as np
```

## Creating arrays

```python
# from Python list
l = [1, 2, 3, 4, 5, 6]
arr = np.array(l)
print(arr)
print(type(arr))
```

## Array attributes

```python
arr = np.array([1, 2, 3, 4])
print(arr.ndim)    # number of dimensions
print(arr.shape)   # tuple with dimension sizes
print(arr.size)    # total number of elements
print(arr.dtype)   # element data type
```

## Multi-dimensional arrays

```python
arr = np.array([[1,2,3,4],[5,6,7,8],[9,10,11,12]])
print(arr)
print(arr.ndim)
print(arr.shape)
```

## Iteration

```python
arr = np.array([1,2,3,4])
for x in arr:
	print(x)

for i in range(len(arr)):
	print(arr[i])
```

## arange, reshape and nditer

```python
arr = np.arange(1, 28).reshape(3,3,3)
print(arr)
for x in np.nditer(arr):
	print(x)

for idx, x in np.ndenumerate(arr):
	print(idx, x)
```

## Indexing and slicing

```python
arr = np.arange(1, 10)
print(arr[0])
print(arr[-1])
print(arr[::-1])
print(arr[1::3])

arr2 = np.arange(1,13).reshape(3,4)
print(arr2[0])
print(arr2[0][1])
print(arr2[2,-1])
print(arr2[::-1])
```

You can also create arrays with a minimum number of dimensions:

```python
arr = np.array([1,2,3,4], ndmin=4)
print(arr)
```

## Special filled arrays

```python
np.zeros(4, dtype=int)
np.zeros((4,4,4))
np.ones((3,3,3))
np.full((3,3), 5)
np.eye(3)
```

## Evenly spaced values

```python
np.linspace(0, 10, 5)    # 5 values including endpoints
np.linspace(0, 10)       # default 50 values
```

## Random arrays

```python
np.random.randint(20, 30, (2,2,5))
np.random.rand(2,2,5)    # uniform [0,1)
np.random.randn(2,2,5)   # standard normal
```

## Data types

```python
arr = np.array([10,20,30,40])
print(arr.dtype)

arr = np.array([10,20,30,40], dtype=np.int8)
arr = np.array([10.6, 10.2, 11.6], dtype=np.float32)

# convert types
arr1 = arr.astype(np.int8)
```

## Element-wise arithmetic

```python
arr = np.array([1,2,3,4,5])
print(arr + 2)
print(arr - 2)
print(arr * 2)
print(arr / 2)
print(arr ** 2)

arr0 = np.array([6,7,8,9,10])
print(np.add(arr, arr0))
print(np.subtract(arr, arr0))
print(np.multiply(arr, arr0))
print(np.divide(arr, arr0))
```

Some ufunc examples:

```python
np.reciprocal(np.arange(1, 19, 0.5))
np.power(np.array([10,20,30,40,45]), 2)
```

## Array functions and reductions

```python
arr = np.array([10,2,20,11,78,43,45,23,21,3,19,21])
print(np.max(arr), np.argmax(arr))
print(np.min(arr), np.argmin(arr))
print(np.sqrt(arr))
print(np.cumsum(np.array([1,0,10,20,30,5,2])))
```

For multi-dimensional arrays you can compute along axes:

```python
arr = np.array([[10,5,3],[11,1,6],[17,98,23],[99,12,16]])
print(np.max(arr, axis=0))  # column-wise
print(np.min(arr, axis=1))  # row-wise
```

## Basic statistics and outlier detection

```python
age = np.array([3,23,24,23,25,26,27,27,24,27,21,23,28,29,26,25,24,22,21,26,25,56])
print(np.mean(age))
print(np.median(age))

Q1 = np.quantile(age, 0.25)
Q2 = np.quantile(age, 0.50)
Q3 = np.quantile(age, 0.75)
IQR = Q3 - Q1
lower_fence = Q1 - 1.5 * IQR
upper_fence = Q3 + 1.5 * IQR
outliers = [x for x in age if x < lower_fence or x > upper_fence]
print('outliers:', outliers)
```

You can visualize distributions with matplotlib/seaborn (example: boxplot):

```python
import matplotlib.pyplot as plt
import seaborn as sns
sns.boxplot(x=age, color='orange')
plt.show()
```

---



