# Python — Week 001: Knowledge Check

**Level:** Beginner  
**Questions:** 10  
**Scope:** Python fundamentals, functions, virtual environments, pytest, Vector, Git, Two Sum, Big O.

Choose one answer for each question.

## Questions

### 1. What is the primary purpose of `__init__` in a Python class?
A. Destroy an object when it is no longer used  
B. Initialize a newly created instance  
C. Define a class-level constant  
D. Run a test before the class is imported

### 2. What does a Python function return when execution reaches the end without a `return` statement?
A. An empty list  
B. The value of the last expression  
C. `None`  
D. A `RuntimeError`

### 3. Which command creates a virtual environment named `.venv`?
A. `python -m venv .venv`  
B. `python --venv .venv`  
C. `pip install venv .venv`  
D. `pytest --venv .venv`

### 4. Which function name follows pytest's default test-discovery convention?
A. `check_vector_addition`  
B. `VectorAdditionCheck`  
C. `test_vector_addition`  
D. `vector_addition_test_case`

### 5. Given two same-length vectors `a = [1, 2]` and `b = [3, 4]`, what should `a + b` produce?
A. `[4, 6]`  
B. `[3, 8]`  
C. `[1, 2, 3, 4]`  
D. `[2, 2]`

### 6. Which command records staged changes in the local Git repository?
A. `git push`  
B. `git commit`  
C. `git fetch`  
D. `git status`

### 7. For Two Sum, `nums = [3, 3]` and `target = 6`. Which indices form a valid answer?
A. `[0, 0]`  
B. `[1, 1]`  
C. `[0, 1]`  
D. No solution exists

### 8. What is a sensible behavior when adding vectors with different dimensions?
A. Pad the shorter vector with zeros automatically  
B. Truncate the longer vector  
C. Raise a meaningful `ValueError`  
D. Return an empty vector

### 9. What does `git add file.py` do?
A. Commits the file  
B. Pushes the file to GitHub  
C. Stages the file for the next commit  
D. Deletes the file from the working tree

### 10. What is the time complexity of two nested loops that each iterate over an input of size `n`?
A. `O(1)`  
B. `O(log n)`  
C. `O(n)`  
D. `O(n²)`

---

## Answer Key and Explanations

| # | Correct | Explanation |
|---:|:---:|---|
| 1 | B | `__init__` initializes instance state after an object is created. |
| 2 | C | Python functions implicitly return `None` if no value is returned explicitly. |
| 3 | A | The standard-library `venv` module creates an isolated environment. |
| 4 | C | By default, pytest discovers test functions whose names start with `test_`. |
| 5 | A | Vector addition is component-wise: `[1 + 3, 2 + 4] = [4, 6]`. |
| 6 | B | `git commit` stores the staged snapshot in the local repository. |
| 7 | C | The two equal values are at distinct indices 0 and 1. |
| 8 | C | Vector addition is defined for equal dimensions; an explicit exception makes the contract clear. |
| 9 | C | `git add` updates the index (staging area); it does not commit or push. |
| 10 | D | The inner loop runs approximately `n` times for each of `n` outer iterations. |

## Hints

1. Think about instance initialization, not object destruction.
2. Remember Python's implicit function return value.
3. Use the standard library module dedicated to virtual environments.
4. Check pytest's default naming pattern.
5. Add corresponding components, not concatenate the lists.
6. A commit is local until you push it.
7. Two Sum requires two different indices, even when values are equal.
8. A vector's dimension is part of its mathematical shape.
9. Staging, committing and pushing are separate Git operations.
10. Multiply the iteration counts of nested loops.
