**Methods & Functions — Readme**

**Overview**: This notebook contains concise examples of Python functions, set operations, recursion, lambda expressions, and higher-order functions (map/filter/reduce). Use this README as a quick reference for the examples in the accompanying notebook.

- Notebook: [methods&functions.ipynb](python-codes/methods%20&%20functions/methods&functions.ipynb)

**Contents**
- Sets: creation, add/remove, iteration, union/intersection/difference/symmetric_difference
- Function definitions: parameter/return variations
- Number theory helpers: prime checks, prime series, Armstrong numbers
- Recursion: sum, factorial, Fibonacci
- List utilities: distinct elements, sorting, maximum, mean/median/mode
- String utilities: palindrome checks
- Functional tools: lambda, map, filter, reduce, zip
- Small NumPy example (array creation)

**Functions & Examples (summary)**
- `def sum(a, b)`: returns a + b (simple function example).
- `def mult(a, b)`: returns a * b; example uses `input()` for interactive use.
- `def sub(a, b)`: returns a - b.
- `def leap_year(year)`: demonstrates forms with/without return values and with/without parameters; detects leap years.
- `def prime(n)`: checks whether `n` is prime; used with interactive input.
- `def prime_series(start, end)`: returns list of primes in a range.
- `def armstrong()` / `def arms(start, end)` / `def arm_strong(n)`: find Armstrong numbers and test a number.
- `def fibo()` / `def fibonacci()`: generate Fibonacci sequence or return nth term (iterative and recursive variants present).
- `def max_of_two(a, b)` and `def max_of_three(x, y, z)`: compute maximums (small helper composition example).
- `def sum(n)`: sums numbers in a list (note: shadows builtin `sum` in the notebook).
- `def palindrome()`: interactive palindrome tester; examples show slicing and manual reversal.
- `def fact()`: computes factorial using iterative approach (interactive version).
- `def distlist(l)`: returns a list with distinct elements preserving order.
- `def sort_list(l, reverse=False)`: custom sort implementation (illustrative; prefer `sorted()` or `list.sort()`).
- `def maximum(l)`: returns largest element by manual scan.
- Recursive examples: `sum(n)`, `facto(n)`, `fibo(n)` (recursive versions).
- `def mean_median_mode(l)`: returns (mean, median, mode) for a numeric list.
- Lambda examples: `a=lambda x: x**2`, `x=lambda a,b: a**b` and a ternary-lambda for largest of three numbers.
- Higher-order examples: `map`, `filter`, `reduce`, and `zip` usage with list comprehensions alternatives.

**How to use**
- Open the notebook link above and run cells in a Jupyter environment.
- Many functions use `input()`; to test programmatically, copy the function and call it with explicit arguments in a separate script or interpreter.
- To convert the notebook to a Python script: run `jupyter nbconvert --to script methods&functions.ipynb` and then run or edit the generated `.py` file.

**Notes & Recommendations**
- Several example functions shadow Python builtins (e.g., `sum`); rename those helpers before importing into larger projects.
- Use built-in functions (`sorted`, `max`, `sum`) or NumPy for production code — the notebook uses manual implementations for learning purposes.
- The notebook contains interactive `input()` calls; for automated testing, replace them with direct arguments or small test harnesses.


