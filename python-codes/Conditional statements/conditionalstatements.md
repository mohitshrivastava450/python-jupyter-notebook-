# Conditional Statements in Python

Conditional statements are used to make decisions in your program. They allow you to execute certain blocks of code depending on whether a condition evaluates to `True` or `False`.

---

## 🔹 Basic `if` Statement
```python
x = 10
if x > 5:
    print("x is greater than 5")
- Runs the block only if the condition is True.


## 🔹 Basic `if-else` Statement

x = 3
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
- The else block runs when the if condition is False.


## 🔹 if-elif-else Statement
x = 5
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")


- elif lets you check multiple conditions in sequence.
- Only the first True condition’s block will execute.

🔹 Example: Grading System
score = 82

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")


- This example shows how multiple elif conditions can be chained to handle different ranges.

📌 Summary
- Use if to check a condition.
- Use elif to check additional conditions if the previous ones are False.
- Use else to handle all remaining cases.
- Only one block runs per chain of if-elif-else.
Conditional statements are essential for decision-making and controlling the flow of your Python programs.

