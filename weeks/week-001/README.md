# Week 001 — Python & Vector Foundations

**Phase:** 1 — Mathematics & Python Foundations
**Estimated effort:** 6 hours
**Status:** Not started

## 1. Weekly objectives

By the end of this week, you should be able to:

- Write basic Python code using functions, classes, collections and type hints.
- Explain what a vector represents mathematically.
- Implement fundamental vector operations without NumPy.
- Write automated tests with `pytest`.
- Solve Two Sum using brute-force and hash-map approaches.
- Explain the time and space complexity of both solutions.

The goal is not just to finish the exercises. You should understand the underlying concepts and be able to explain your implementation.

## 2. Time budget

| Activity                    |              Time |
| --------------------------- | ----------------: |
| Python theory and practice  |            1 hour |
| Linear algebra              |            1 hour |
| Implementation              |           2 hours |
| Experiments                 |        30 minutes |
| Notes and review            |        30 minutes |
| MAANG interview preparation |            1 hour |
| **Total**             | **6 hours** |

You can split the work across several days.

## 3. Python foundations

### Topics

Review and practice:

- Variables and basic data types
- Functions and return values
- Lists, tuples, dictionaries and sets
- Classes and objects
- Type hints
- Exceptions
- Modules and imports
- Basic automated testing with `pytest`

### Exercises

1. Implement a function that calculates the arithmetic mean of a list of numbers.
2. Implement a function that returns the minimum and maximum values.
3. Create a class representing a simple bank account with deposit and withdrawal methods.
4. Add type hints to all public functions and methods.
5. Write tests for normal cases and invalid inputs.

**Acceptance criteria:**

- Code follows Python conventions.
- Functions have meaningful names and type hints.
- Invalid inputs are handled explicitly.
- Tests cover normal and edge cases.

## 4. Mathematics — vectors

### Theory

Study the following concepts:

**Scalar:** A single numerical value.

**Vector:** An ordered collection of numerical values.

For example:

$$
\begin{aligned}
a &= [2, 3, 4]\\
b &= [1, 5, 2]
\end{aligned}
$$

### Operations

**Vector addition**

$$
a+b =
\begin{bmatrix}
2+1\\
3+5\\
4+2
\end{bmatrix}
=
\begin{bmatrix}
3\\
8\\
6
\end{bmatrix}
$$

**Scalar multiplication**

$$
3a =
3
\begin{bmatrix}
2\\
3\\
4
\end{bmatrix}
=
\begin{bmatrix}
6\\
9\\
12
\end{bmatrix}
$$

**Dot product**

$$
\begin{aligned}
a \cdot b
&= 2 \cdot 1 + 3 \cdot 5 + 4 \cdot 2\\
&= 2 + 15 + 8\\
&= 25
\end{aligned}
$$

**Euclidean norm (L2 norm)**

$$
\begin{aligned}
\|a\|_2
&= \sqrt{2^2 + 3^2 + 4^2}\\
&= \sqrt{4 + 9 + 16}\\
&= \sqrt{29}
\end{aligned}
$$

### Math exercises

1. Calculate the sum of two vectors manually.
2. Calculate the dot product of two vectors.
3. Calculate the Euclidean norm.
4. Explain why vectors with different dimensions cannot be added.
5. Explain the geometric intuition behind the dot product.

Do the calculations by hand first, then verify them with Python.

## 5. Implementation — Vector class

Create:

`foundations/mathematics/linear-algebra/vector.py`

Implement a `Vector` class without NumPy.

### Required API

```python
class Vector:
    def __init__(self, values: list[float]):
        ...

    def __add__(self, other: "Vector") -> "Vector":
        ...

    def __mul__(self, scalar: float) -> "Vector":
        ...

    def dot(self, other: "Vector") -> float:
        ...

    def magnitude(self) -> float:
        ...
```

You may add:

- `__eq__`
- `__repr__`
- `__len__`

### Required behavior

- Vectors must have a consistent number of dimensions for binary operations.
- Addition must return a new vector.
- Scalar multiplication must return a new vector.
- Dot product must return a scalar.
- Magnitude must return a non-negative value.
- The zero vector must have magnitude zero.
- Invalid dimensions must raise a meaningful exception.

### Tests

Create:

`foundations/mathematics/linear-algebra/test_vector.py`

Cover:

1. Vector addition.
2. Scalar multiplication.
3. Dot product.
4. Magnitude.
5. Zero vector.
6. Empty vector behavior.
7. Dimension mismatch.
8. Equality.
9. Negative scalar multiplication.

**Important:** Do not use NumPy in this assignment. The purpose is to understand the operations rather than delegate them to a library.

## 6. MAANG practice — Two Sum

Problem: Given an array of integers and a target value, return the indices of two numbers whose sum equals the target.

Example:

```python
nums = [2, 7, 11, 15]
target = 9

# Expected result: [0, 1]
```

### Task A — Brute force

Implement the solution using nested loops.

Requirements:

- Explain why it works.
- Calculate time complexity.
- Calculate space complexity.

Expected complexity:

- Time: $O(n^2)$
- Extra space: $O(1)$

### Task B — Hash map

Implement an optimized solution using a dictionary.

Hint: For each number, calculate:

$$
complement = target - current
$$

Check whether the complement already exists in the dictionary.

Expected complexity:

- Time: $O(n)$ average case
- Extra space: $O(n)$

### Edge cases

Test:

- Two elements.
- Negative numbers.
- Duplicate values.
- Zero values.
- No valid pair.
- Multiple possible pairs.

Be prepared to explain the trade-off between time and space complexity.

## 7. Mini experiment

Compare the two Two Sum implementations on synthetic inputs.

Suggested input sizes:

- 100
- 1,000
- 5,000
- 10,000

Record:

| Input size | Brute-force time | Hash-map time |
| ---------: | ---------------: | ------------: |
|        100 |                  |               |
|      1,000 |                  |               |
|      5,000 |                  |               |
|     10,000 |                  |               |

Use Python's `time.perf_counter()`.

Important:

- Run each benchmark multiple times.
- Avoid comparing runs with different machine conditions.
- Do not assume a single measurement proves theoretical complexity.
- Explain whether the observed results match your expectations.

## 8. Suggested project structure

```text
ai-research-engineer-academy/
├── foundations/
│   └── mathematics/
│       └── linear-algebra/
│           ├── vector.py
│           └── test_vector.py
├── weeks/
│   └── week-001/
│       ├── README.md
│       ├── notes.md
│       ├── exercises/
│       │   ├── python_basics.py
│       │   └── two_sum.py
│       ├── tests/
│       └── results/
│           └── benchmark.md
```

You can adapt the structure to the repository's existing layout.

## 9. Definition of Done

Before marking Week 001 as complete, verify every item:

- [ ] Python environment is configured.
- [ ] Python exercises are implemented.
- [ ] Vector class is implemented without NumPy.
- [ ] Vector tests pass.
- [ ] Two Sum brute-force solution is implemented.
- [ ] Two Sum hash-map solution is implemented.
- [ ] Complexity analysis is documented.
- [ ] Benchmark results are recorded.
- [ ] Mathematical exercises are solved manually.
- [ ] Notes explain the concepts in your own words.
- [ ] At least one MAANG problem is ready to discuss verbally.

## 10. Self-assessment

Score each dimension from 1 to 5.

| Dimension                   | Score |
| --------------------------- | ----: |
| Python understanding        |    /5 |
| Mathematical understanding  |    /5 |
| Implementation quality      |    /5 |
| Testing and experimentation |    /5 |
| Technical communication     |    /5 |

A score of 3 means you can complete the task independently and explain the main ideas. A score of 5 means you can also explain design trade-offs, edge cases and limitations.

Do not mark a topic as mastered simply because the code works.

## 11. Weekly retrospective

Complete `notes.md` with answers to these questions:

1. What did I learn this week?
2. Which mathematical concept was most difficult?
3. What Python feature was unfamiliar?
4. What implementation decision would I change?
5. Can I explain the dot product without looking at my notes?
6. Can I explain why the hash-map solution is faster?
7. What should I review before Week 002?

**Final deliverable:** A tested, documented implementation of vectors and Two Sum, plus a short mathematical and experimental report.
