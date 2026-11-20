# Python — Week 001: Quiz 2

**Level:** Beginner → Intermediate  
**Questions:** 10  
**Scope:** Python collections and semantics, Vector API, pytest fixtures, Git, Two Sum, debugging and Big O.

Choose the best answer unless the question says otherwise.

## Questions

### 1. What does a shallow copy of a list copy?
A. The outer list and every nested object recursively  
B. Only the outer list; nested objects are still shared  
C. Only immutable elements  
D. A reference to the exact same list object

### 2. Which statements about Python dictionaries are true? *(Select all that apply.)*
A. Dictionary keys must be hashable  
B. A key can occur multiple times as separate entries  
C. Assigning an existing key replaces its associated value  
D. Dictionaries preserve insertion order in modern Python

### 3. What is the main risk of using a mutable object as a default argument?
A. Python rejects the function definition  
B. A new object is created on every call  
C. The same default object is reused across calls  
D. The argument becomes immutable

### 4. What is the difference between `is` and `==`?
A. Both always compare object identity  
B. `is` compares identity; `==` compares equality  
C. `is` compares values; `==` compares types  
D. They are interchangeable for all objects

### 5. What should `Vector.__add__` do when the other operand is not a compatible Vector?
A. Silently return the left operand  
B. Add the scalar to every component  
C. Return an unrelated empty list  
D. Reject the unsupported operation clearly

### 6. What is a pytest fixture primarily used for?
A. Replacing Python's import system  
B. Providing reusable setup (and optionally teardown) for tests  
C. Running tests in random order only  
D. Converting every test into a class

### 7. In the hash-map Two Sum algorithm, what value do we look up for the current number `x`?
A. `target + x`  
B. `target * x`  
C. `target - x`  
D. `x / target`

### 8. Which command shows the state of the working tree and staging area?
A. `git status`  
B. `git commit`  
C. `git log --push`  
D. `git init --status`

### 9. What happens in this code if the loop never assigns to `found`?

```python
for value in values:
    if value == target:
        found = value

print(found)
```

A. It prints `None`  
B. It prints an empty string  
C. It raises `NameError`  
D. It raises `UnboundLocalError`

### 10. What is the time complexity of this pattern?

```python
i = 1
while i < n:
    for _ in range(n):
        do_work()
    i *= 2
```

A. `O(n)`  
B. `O(log n)`  
C. `O(n log n)`  
D. `O(n²)`

---

## Answer Key and Explanations

| # | Correct | Explanation |
|---:|:---:|---|
| 1 | B | A shallow copy creates a new outer container but retains references to nested objects. |
| 2 | A, C, D | Keys must be hashable, assigning an existing key updates its value, and insertion order is preserved. |
| 3 | C | Default expressions are evaluated once when the function is defined, so a mutable default can retain state. |
| 4 | B | Identity asks whether two references point to the same object; equality asks whether values compare equal. |
| 5 | D | The class should define a clear supported operand contract rather than silently producing an incorrect result. |
| 6 | B | Fixtures centralize reusable test setup and can provide teardown after `yield`. |
| 7 | C | If the current value is `x`, its complement is `target - x`. |
| 8 | A | `git status` reports staged, unstaged and untracked changes. |
| 9 | D | Since `found` is a local variable that was never assigned, reading it raises `UnboundLocalError`. |
| 10 | C | The while loop executes `O(log n)` times and each pass performs `O(n)` work. |

## Hints

1. Consider whether nested objects are duplicated or merely referenced.
2. Think about hashability, replacement semantics and insertion order.
3. Compare mutable defaults with creating a new list inside the function.
4. Identity and equality answer different questions.
5. Make invalid operations explicit in an API.
6. Fixtures help avoid repeated setup code.
7. The complement is the amount needed to reach the target.
8. Git status is an inspection command.
9. Trace whether the variable is assigned on every possible path.
10. Count the outer loop iterations, then multiply by the work per iteration.
