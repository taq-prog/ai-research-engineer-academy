# Week 001 Quiz — Python & Linear Algebra Foundations

Use this quiz after completing the Week 001 materials. It checks only the topics introduced in [the Week 001 guide](README.md): Python fundamentals, vectors and their basic operations, tests, and Two Sum.

**Suggested time:** 45–60 minutes  
**Total:** 100 points

## Instructions

- Try every question before opening the answer key.
- For multiple-select questions, select all correct choices; points are awarded only for the complete correct set.
- Show calculations for vector questions.
- For short answers, explain your reasoning in your own words.
- For the coding question, use plain Python and the techniques covered this week. Do not use NumPy.

## Questions

### 1. Python collections — Multiple choice · Easy · 5 points

Which statement about these Python values is correct?

```python
values = [1, 2]
pair = (1, 2)
lookup = {"a": 1}
unique = {1, 2}
```

A. `values` is immutable and `pair` is mutable.  
B. `values` is mutable and `pair` is immutable.  
C. `lookup` stores values by numeric position.  
D. `unique` preserves duplicate values.

---

### 2. Functions and return values — Multiple choice · Easy · 5 points

What does this function return when called as `add(2, 3)`?

```python
def add(left: int, right: int) -> int:
    result = left + right
```

A. `5`  
B. `None`  
C. `result`  
D. A `TypeError`

---

### 3. Mutability and references — Code tracing · Medium · 8 points

What is printed, and why?

```python
def add_item(items: list[int]) -> None:
    items.append(3)

numbers = [1, 2]
add_item(numbers)
print(numbers)
```

---

### 4. Vector addition — Calculation · Easy · 7 points

Let (a = [2, 3, 4]) and (b = [1, 5, 2]). Compute (a+b). State one condition required for vector addition.

---

### 5. Dot product and Euclidean norm — Calculation · Medium · 8 points

For (a=[2,3,4]) and (b=[1,5,2]):

1. Compute (a \cdot b).
2. Compute the Euclidean norm (|a|_2). An exact answer with a radical is acceptable.

---

### 6. Linear combinations and dot product — Multiple select · Medium · 6 points

Select both correct statements.

A. (a+b) is a linear combination of (a) and (b).  
B. The dot product of two vectors is another vector with the same dimension.  
C. The dot product is a scalar formed from pairwise products and addition; geometrically, it helps describe how vectors align.  
D. A linear combination can only use one vector.

---

### 7. Dimension validation — Short answer · Medium · 7 points

A `Vector.__add__` method loops over matching positions only up to the length of the shorter vector and returns those paired sums.

What bug can this cause? What should the method do when dimensions differ?

---

### 8. Implement a vector operation — Coding · Hard · 10 points

Write a function with type hints that returns the dot product of two lists of numbers. It must reject vectors of different lengths by raising `ValueError`. You may assume both lists contain numbers.

---

### 9. Testing behavior — Multiple choice · Easy · 6 points

Which pytest assertion checks that `Vector([1, 2]) + Vector([3, 4])` equals `Vector([4, 6])`, assuming `Vector.__eq__` is implemented?

A. `assert Vector([1, 2]) + Vector([3, 4]) == Vector([4, 6])`  
B. `assert pytest(Vector([1, 2]) + Vector([3, 4]))`  
C. `assert Vector([4, 6]) = Vector([1, 2]) + Vector([3, 4])`  
D. `assert raises(Vector([1, 2]) + Vector([3, 4]))`

---

### 10. Two Sum with duplicates — Code tracing · Medium · 7 points

What indices should a correct Two Sum function return for `nums = [3, 3]` and `target = 6)? Explain why the two indices must be different.

---

### 11. Choosing a Two Sum approach — Multiple choice · Easy · 6 points

Which description of the hash-map Two Sum approach is correct?

A. It stores previously seen values and checks whether each current value's complement has already appeared.  
B. It sorts the input and returns the two values, not their original indices.  
C. It checks only adjacent pairs.  
D. It uses a set of all possible pairs, requiring no extra space.

---

### 12. Complexity — Multiple select · Medium · 8 points

Choose the correct average-case time and extra-space complexity for the two standard Week 001 approaches.

A. Nested-loop brute force: (O(n^2)) time, (O(1)) extra space.  
B. Nested-loop brute force: (O(n)) time, (O(n)) extra space.  
C. Hash map: (O(n)) time, (O(n)) extra space.  
D. Hash map: (O(n^2)) time, (O(1)) extra space.

---

### 13. Time-space trade-off — Short answer · Medium · 7 points

In one or two sentences, explain the time-space trade-off between the brute-force and hash-map Two Sum approaches.

---

### 14. Find the Two Sum bug — Code review · Hard · 10 points

This hash-map implementation returns indices of two numbers that sum to `target`. Identify the problem with the order of operations and give an input where it can return the same index twice.

```python
def two_sum(nums: list[int], target: int) -> list[int] | None:
    seen: dict[int, int] = {}

    for index, value in enumerate(nums):
        seen[value] = index
        complement = target - value
        if complement in seen:
            return [seen[complement], index]

    return None
```

## Answer key and explanations

### 1. B

Lists can be changed in place, while tuples cannot. Dictionaries map keys to values, and sets hold unique values.

### 2. B

The function has no `return` statement. Python returns `None` when a function finishes without an explicit return. The type hint describes the intended return type; it does not add a return automatically.

### 3. `[1, 2, 3]`

The function receives a reference to the same list object as `numbers`. Calling `append` mutates that object, so the caller sees the added item.

### 4. `[3, 8, 6]`

Add corresponding entries: ([2+1, 3+5, 4+2]). The vectors must have the same dimension (the same number of entries).

### 5. Dot product: `25`; norm: (sqrt{29})

(2\times1 + 3\times5 + 4\times2 = 25).  
(|a|_2 = \sqrt{2^2+3^2+4^2}=\sqrt{29}).

### 6. A and C

A linear combination scales vectors and adds the results; (a+b) is the combination 1a+1b. The dot product is a scalar. Its geometric interpretation includes how aligned the vectors are.

### 7. Expected points

Award credit for both parts:

- **3 points:** Explains that stopping at the shorter length drops unmatched trailing entries, so the method can return a plausible but incorrect shorter vector.
- **4 points:** Says to check that the dimensions match and raise a meaningful exception (such as `ValueError`) before adding.

### 8. Example answer

```python
def dot(left: list[float], right: list[float]) -> float:
    if len(left) != len(right):
        raise ValueError("vectors must have the same dimension")
    total = 0.0
    for index in range(len(left)):
        total += left[index] * right[index]
    return total
```

Award points for a correct type-hinted function, dimension validation with `ValueError`, and the sum of pairwise products. A loop instead of `sum` is also correct.

### 9. A

A pytest test can use a normal Python assertion. The equality operator is `==`; `=` is assignment and cannot be used in an assertion expression like this.

### 10. Indices `[0, 1]` (or `[1, 0]`)

The two equal values are at separate positions. A valid pair must use two distinct indices, even though the values are equal.

### 11. A

For each value, compute its complement (`target - value`) and look for that complement among values already seen. A dictionary can also retain the earlier index needed in the result.

### 12. A and C

Nested loops check pairs and take quadratic time with constant extra storage. A hash map supports an average-case linear scan by using additional storage proportional to the input size.

### 13. Expected answer

Brute force uses little extra memory but checks many pairs, taking (O(n^2)) time. The hash-map method uses (O(n)) extra space to look up complements and runs in (O(n)) average-case time.

### 14. It inserts the current value before checking its complement

When `value == complement`, the just-inserted entry can match itself. For example, `nums=[3]` and `target=6` may return `[0, 0]`, reusing one index. Check for the complement first, then store the current value and index. The duplicate-value input `nums=[3, 3]`, `target=6` should still work because the second 3 finds the first one.

## Scoring rubric

Add the points earned for a score out of 100.

| Score | Result | Suggested next step |
|---:|---|---|
| 85–100 | Strong | Continue to Week 002; review any missed questions. |
| 70–84 | Good | Continue, while revisiting the missed topics. |
| 60–69 | Needs improvement | Review the relevant Week 001 sections and retry missed questions. |
| Below 60 | Review recommended | Revisit the Python, vector, and Two Sum fundamentals before moving on. |

For short-answer and coding questions, award partial credit according to the criteria in the answer key. Use the score as a study guide: a high total does not replace the Week 001 implementation, tests, and explanations required by the programme.
