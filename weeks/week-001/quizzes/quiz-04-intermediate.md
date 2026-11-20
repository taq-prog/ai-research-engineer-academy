# Python Week 001 — Quiz 4

**Level:** Intermediate  
**Questions:** 10  
**Scope:** Python semantics, OOP, Vector protocol, pytest, Git workflow, Two Sum, Big O, hashability and debugging.

These questions extend the first three quizzes with new scenarios.

## Questions

### 1. *(Single select)* What does this function return on its second call?

```python
def collect(value, items=[]):
    items.append(value)
    return items

first = collect(1)
second = collect(2)
```

A. `[2]`  
B. `[1, 2]`  
C. `[1]`  
D. It raises `TypeError`

### 2. *(Single select)* A child class overrides a method but still needs the parent's implementation. Which expression is normally used?
A. `parent.method(self)` is the only valid option  
B. `super().method()`  
C. `self.base.method()`  
D. `override.method()`

### 3. *(Single select)* If a Vector class implements `__len__`, what does `len(vector)` do?
A. Calls `vector.__size__()`  
B. Returns the vector's magnitude  
C. Calls `vector.__len__()`  
D. Always returns 1

### 4. *(Multi-select)* Which statements about pytest's `tmp_path` fixture and fixture lifecycle are correct?
A. `tmp_path` provides a temporary directory unique to a test invocation  
B. Code after `yield` in a yield-fixture is teardown  
C. A fixture function should normally be called directly like an ordinary helper to obtain its value  
D. Pytest injects requested fixtures into test function parameters

### 5. *(Single select)* You staged a file with `git add` but have not committed it. Which command removes it from the staging area while keeping the working-tree changes?
A. `git restore --staged file.py`  
B. `git restore file.py`  
C. `git clean -f file.py`  
D. `git reset --hard file.py`

### 6. *(Single select)* Why should a hash-map Two Sum implementation check whether the complement exists before inserting the current value?
A. To keep dictionary keys sorted  
B. To avoid using the same element index twice  
C. To make dictionary lookup O(n)  
D. To support only positive integers

### 7. *(Single select)* What is the time complexity of this membership check inside a loop over a list?

```python
result = []
for value in values:
    if value not in result:
        result.append(value)
```

Assume `result` can grow proportionally to the input size.

A. `O(1)`  
B. `O(log n)`  
C. `O(n)`  
D. `O(n²)`

### 8. *(Multi-select)* Which statements about `__eq__` and `__hash__` are correct?
A. Defining `__eq__` may make instances unhashable by default  
B. Equal objects must have equal hash values when they are hashable  
C. Defining `__eq__` automatically guarantees that every instance remains hashable  
D. A class can explicitly set `__hash__ = None` to mark instances as unhashable

### 9. *(True / False)* Pytest guarantees that test functions in a module run in the order in which they appear in the source file.

A. True  
B. False

### 10. *(Single select)* What is the main problem with modifying a list using `pop` while iterating over a range created from its original length?

```python
values = [10, 20, 30, 40]
for i in range(len(values)):
    if values[i] < 30:
        values.pop(i)
```

A. `range` automatically adjusts its indices after a removal  
B. Removing elements shifts later indices, which can cause skipped elements or `IndexError`  
C. `pop` always returns `None`  
D. Python forbids modifying lists inside loops

---

## Answer Key and Explanations

| # | Correct | Explanation |
|---:|:---:|---|
| 1 | B | Default argument objects are created once when the function is defined; both calls mutate the same list. |
| 2 | B | `super()` follows the method resolution order and delegates to the next implementation. |
| 3 | C | `len(obj)` uses the object's `__len__` protocol method. |
| 4 | A, B, D | `tmp_path` is per-test temporary storage; yield fixtures support teardown; pytest injects fixtures by parameter name. Fixture functions should not be called directly. |
| 5 | A | `git restore --staged` unstages the file but leaves its working-tree edits intact. |
| 6 | B | Looking up first ensures the current element cannot match itself at the same index. |
| 7 | D | List membership is linear; performing it for each of n values yields quadratic worst-case work. |
| 8 | A, B, D | Defining equality can disable the default hash; the equality/hash contract requires equal hashes for equal objects. |
| 9 | B | Tests should be independent; default execution order is not a guarantee to rely on. |
| 10 | B | `pop` shifts subsequent elements left while the precomputed range keeps its original indices. |

## Hints

1. Mutable defaults live beyond a single function call.
2. Think about cooperative inheritance and the method resolution order.
3. `len` is a Python data-model protocol.
4. Fixtures are requested through test parameters and may manage cleanup.
5. Unstaging is different from discarding working-tree edits.
6. The algorithm must return two distinct positions.
7. A list membership operation scans elements.
8. Remember the equality/hash contract for dictionary and set keys.
9. Tests should not depend on execution order.
10. The range is fixed before the list starts shrinking.
