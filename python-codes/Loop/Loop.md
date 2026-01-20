# Loops in Python

Loops in Python allow you to execute a block of code repeatedly until a condition is met. They are essential for automating repetitive tasks and iterating over data structures.

---

## 🔄 Types of Loops in Python

### 1. `for` Loop
- Used to iterate over a sequence (list, tuple, string, dictionary, or range).
- Syntax:
  ```python
  for item in sequence:
      # code block
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)


2. while Loop
- Executes a block of code as long as the condition is True.
- Syntax:
while condition:
    # code block
- 
count = 0
while count < 5:
    print("Count:", count)
    count += 1

⏹ Loop Control Statements

break
- Terminates the loop prematurely.
- Example:
for num in range(10):
    if num == 5:
        break
    print(num)


continue
- 
- Skips the current iteration and moves to the next.
- Example:

for num in range(5):
    if num == 2:
        continue
    print(num)

pass
- Acts as a placeholder; does nothing.
- Example:
for num in range(3):
    pass  # to be implemented later




🔁 Nested Loops
- Loops inside loops.
- Example:

for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")


📌 Summary
- for loop → iterate over sequences.
- while loop → repeat until condition is false.
- Control statements (break, continue, pass) modify loop behavior.
- Nested loops allow complex iterations.

✅ Best Practices
- Avoid infinite loops by ensuring conditions eventually become False.
- Use break and continue wisely to keep code readable.
- Prefer for loops when iterating over known sequences.
- Use while loops for conditions that depend on dynamic states.
