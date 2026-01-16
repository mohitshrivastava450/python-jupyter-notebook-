# Python Operators

Operators in Python are special symbols or keywords used to perform operations on values and variables. They are the building blocks of expressions and allow manipulation of data.

---

## Types of Operators in Python

### 1. Arithmetic Operators
Used to perform mathematical operations.

| Operator | Description        | Example (`a=10, b=5`) | Result |
|----------|--------------------|-----------------------|--------|
| `+`      | Addition           | `a + b`               | 15     |
| `-`      | Subtraction        | `a - b`               | 5      |
| `*`      | Multiplication     | `a * b`               | 50     |
| `/`      | Division           | `a / b`               | 2.0    |
| `%`      | Modulus (remainder)| `a % b`               | 0      |
| `**`     | Exponentiation     | `a ** b`              | 100000 |
| `//`     | Floor Division     | `a // b`              | 2      |

---

### 2. Comparison (Relational) Operators
Used to compare values; returns `True` or `False`.

| Operator | Description       | Example (`a=10, b=5`) | Result |
|----------|-------------------|-----------------------|--------|
| `==`     | Equal to          | `a == b`              | False  |
| `!=`     | Not equal to      | `a != b`              | True   |
| `>`      | Greater than      | `a > b`               | True   |
| `<`      | Less than         | `a < b`               | False  |
| `>=`     | Greater or equal  | `a >= b`              | True   |
| `<=`     | Less or equal     | `a <= b`              | False  |

---

### 3. Logical Operators
Used to combine conditional statements.

| Operator | Description | Example (`a=10, b=5`) | Result |
|----------|-------------|-----------------------|--------|
| `and`    | True if both are true | `(a > 5 and b < 10)` | True |
| `or`     | True if at least one is true | `(a > 5 or b > 10)` | True |
| `not`    | Negates the condition | `not(a > 5)` | False |

---

### 4. Assignment Operators
Used to assign values to variables.

| Operator | Description | Example (`a=10`) | Result |
|----------|-------------|------------------|--------|
| `=`      | Assign      | `a = 10`         | 10     |
| `+=`     | Add & assign| `a += 5`         | 15     |
| `-=`     | Subtract & assign | `a -= 5`   | 5      |
| `*=`     | Multiply & assign | `a *= 2`   | 20     |
| `/=`     | Divide & assign | `a /= 2`     | 5.0    |
| `%=`     | Modulus & assign | `a %= 3`    | 1      |
| `**=`    | Exponent & assign | `a **= 2`  | 100    |
| `//=`    | Floor divide & assign | `a //= 3` | 3   |

---

### 5. Bitwise Operators
Work on bits (binary representation).

| Operator | Description | Example (`a=10, b=5`) | Result |
|----------|-------------|-----------------------|--------|
| `&`      | AND         | `a & b`               | 0      |
| `|`      | OR          | `a | b`               | 15     |
| `^`      | XOR         | `a ^ b`               | 15     |
| `~`      | NOT         | `~a`                  | -11    |
| `<<`     | Left shift  | `a << 2`              | 40     |
| `>>`     | Right shift | `a >> 2`              | 2      |

---

### 6. Identity Operators
Used to compare memory locations.

| Operator | Description | Example (`a=10, b=10`) | Result |
|----------|-------------|------------------------|--------|
| `is`     | True if both refer to same object | `a is b` | True |
| `is not` | True if not same object | `a is not b` | False |

---

### 7. Membership Operators
Used to test if a value is in a sequence.

| Operator | Description | Example | Result |
|----------|-------------|---------|--------|
| `in`     | True if value exists | `5 in [1,2,3,4,5]` | True |
| `not in` | True if value does not exist | `10 not in [1,2,3,4,5]` | True |

---

## Summary
Python operators are categorized into:
- Arithmetic
- Comparison
- Logical
- Assignment
- Bitwise
- Identity
- Membership

They allow manipulation of data and control flow in programs.