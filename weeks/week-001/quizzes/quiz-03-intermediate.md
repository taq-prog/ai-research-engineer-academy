# Python Week 001 — Quiz 3 (Intermediate)

**Level:** Intermediate  
**Questions:** 10  
**Scope:** Python control flow and unpacking, OOP, Vector behavior, pytest fixtures, Git, Two Sum, Big O and debugging.

Question types are indicated. Select all correct answers for multi-select questions.

## Questions

### 1. *(Single select)* What does this code print?

```python
for number in [1, 2, 3]:
    if number == 2:
        break
else:
    print("completed")
```

A. Nothing  
B. `completed`  
C. `2`  
D. It raises `SyntaxError`

### 2. *(Single select)* What are the values after this unpacking?

```python
head, *middle, tail = ["A", "B", "C"]
```

A. `head = "A"`, `middle = ["B"]`, `tail = "C"`  
B. `head = ["A"]`, `middle = "B"`, `tail = ["C"]`  
C. `head = "A"`, `middle = ["B", "C"]`, `tail = None`  
D. It raises `ValueError`

### 3. *(Single select)* What does this code print?

```python
class Counter:
    count = 0

    def increment(self):
        self.count += 1

a = Counter()
b = Counter()
a.increment()
print(Counter.count, a.count, b.count)
```

A. `1 1 1`  
B. `0 1 0`  
C. `2 1 1`  
D. `0 0 0`

### 4. *(Single select)* Assume `Vector.__mul__` returns a new Vector using a list comprehension. What happens here?

```v1 = Vector([1, 2, 3])`
```

```python
v2 = v1 * 2
```

A. `v1.values` becomes `[2, 4, 6]`  
B. `v1.values` becomes `[1, 2, 3, 1, 2, 3]`  
C. `v1.values` remains `[1, 2, 3]`  
D. Both variables must reference the same object

### 5. *(Single select)* Consider a pytest fixture:

```python
@pytest.fixture
def resource():
    print("setup")
    yield object()
    print("teardown")
```

When does teardown run for a test that uses this fixture?
A. Before setup  
B. Immediately when `yield` is reached  
C. After the test using the fixture finishes  
D. Only if the test fails

### 6. *(Single select)* Which command is the appropriate way to reverse a commit that has already been published and shared?
A. `git reset --hard HEAD~1`  
B. `git revert <commit>`  
C. `git restore --source=HEAD~1 .`  
D. `git clean -fd`

### 7. *(Multi-select)* Which statements should a correct Two Sum implementation satisfy?
A. It must return two distinct indices  
B. It should support negative numbers  
C. It should return `None` (or a documented no-solution result) when no pair exists  
D. It may use the same array index twice if the value is half the target

### 8. *(Single select)* What is the amortized time complexity of Python list `append`?
A. `O(n)`  
B. `O(log n)`  
C. `O(1)`  
D. `O(n²)`

### 9. *(True / False)* A `finally` block executes before a pending `return` completes when the return occurs inside the associated `try` block.

A. True  
B. False

### 10. *(True / False)* Python's `assert` statements can be removed when the interpreter runs with optimization enabled (for example, `python -O`).

A. True  
B. False

---

## Answer Key and Explanations

| # | Correct | Explanation |
|---:|:---:|---|
| 1 | A | A loop's `else` clause runs only when the loop completes without `break`. Here the loop breaks at 2. |
| 2 | A | The starred target collects the remaining middle items into a list. |
| 3 | B | `self.count += 1` creates/updates an instance attribute on `a`; the class attribute remains 0 and `b` still resolves to it. |
| 4 | C | A new list is built for the result, so the original vector's values are not mutated. |
| 5 | C | Code after `yield` is fixture teardown and runs after the dependent test completes. |
| 6 | B | `git revert` creates a new commit that reverses the selected change without rewriting shared history. |
| 7 | A, B, C | A valid pair uses distinct positions; integer inputs can be negative, and the no-solution behavior should be explicit. |
| 8 | C | Appends are amortized constant time; occasional resizing can take linear time. |
| 9 | A | The `finally` block runs during stack unwinding before the function actually returns. |
| 10 | A | Assertions are omitted under optimization, so they should not be used for essential runtime validation. |

## Hints

1. The loop stops early; ask whether it completed normally.
2. The starred target captures the middle portion as a list.
3. Augmented assignment through `self` may shadow a class attribute.
4. Distinguish returning a new object from mutating the original.
5. Read fixture code both before and after `yield`.
6. Prefer a new reversing commit for shared history.
7. Check the indices, not only the values.
8. Dynamic arrays occasionally resize, but append is amortized O(1).
9. `finally` is designed to run during cleanup.
10. Assertions are useful for debugging, not mandatory validation.
