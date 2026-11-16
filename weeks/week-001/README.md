# Week 001 — Python & Linear Algebra Foundations

**Programme:** AI Research Engineer Academy
**Phase:** 1 — Mathematics & Python Foundations
**Duration:** 1 week
**Estimated workload:** 6 hours
**Status:** Not Started

---

## 1. Weekly Objectives

By the end of this week, you should be able to:

1. Write basic Python code using functions, classes, collections and type hints.
2. Understand vectors and fundamental vector operations.
3. Explain the geometric intuition behind the dot product and Euclidean norm.
4. Implement a basic `Vector` class without NumPy.
5. Write automated tests using `pytest`.
6. Solve Two Sum using brute-force and hash-map approaches.
7. Explain the time and space complexity of both solutions.

**Learning principle:** Understand the mathematics first, implement it in Python, test your implementation, and explain the results in your own words.

## 2. Time Allocation

| Activity                        |              Time |
| ------------------------------- | ----------------: |
| Python fundamentals             |            1 hour |
| MIT Linear Algebra              |            1 hour |
| Mathematics exercises           |        30 minutes |
| Vector implementation and tests |         1.5 hours |
| Experiments and notes           |            1 hour |
| MAANG interview preparation     |            1 hour |
| **Total**                 | **6 hours** |

You can distribute these activities across multiple days.

---

## 3. Learning Resources

Use the following resources in the recommended order. Required resources are sufficient to complete this week.

### 3.1 Python Fundamentals

**Primary resource:**

- [The Python Tutorial — Official Documentation](https://docs.python.org/3/tutorial/)

Recommended sections:

| Section | Topic                              | Priority |
| ------- | ---------------------------------- | -------- |
| 3       | An Informal Introduction to Python | Required |
| 4       | More Control Flow Tools            | Required |
| 5       | Data Structures                    | Required |
| 9       | Classes                            | Required |
| 6       | Modules                            | Optional |

Focus on functions, collections, classes, exceptions and modules.

You do not need to read the entire Python documentation.

### 3.2 Linear Algebra

**Primary resource:**

- [MIT 18.06SC — Linear Algebra, Fall 2011](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/)

Lecturer: Gilbert Strang.

Recommended materials:

- [Lecture Videos](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/video_galleries/lecture-videos/)
- [Lecture Notes](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/resources/lecture-notes/)
- [Problem Sets](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/resources/problem-sets/)
- [Problem Set Solutions](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/resources/problem-set-solutions/)

**Assigned material:**

- Lecture 1 — The Geometry of Linear Equations.
- Start Lecture 2 — Elimination with Matrices, if time permits.

Study the lecture notes alongside the videos. Attempt exercises before looking at solutions.

### 3.3 Additional Vector Intuition

**Optional supporting resource:**

- [Khan Academy — Vectors and Spaces](https://www.khanacademy.org/math/vectors-and-spaces)

Recommended topics:

- Vector addition and scalar multiplication.
- Dot product.
- Vector length.
- Angle between vectors.

Use this resource if the geometric interpretation of vectors or dot products is unclear.

### 3.4 Python Testing

**Primary resource:**

- [pytest — Getting Started](https://docs.pytest.org/en/stable/getting-started.html)

Focus on:

- Writing your first test.
- Using assertions.
- Testing exceptions.
- Testing floating-point values with `pytest.approx`.

### 3.5 Algorithm Practice

**Primary problem:**

- [LeetCode — Two Sum](https://leetcode.com/problems/two-sum/)

Recommended learning sequence:

1. Solve using brute force.
2. Analyze time and space complexity.
3. Identify the repeated lookup operation.
4. Optimize using a hash map.
5. Explain the time-space trade-off.

Do not look at the editorial before attempting the problem yourself.

---

## 4. Python Fundamentals

**Estimated time:** 1 hour

### Topics

Review and practice:

- Variables and basic data types.
- Functions and return values.
- Lists, tuples, dictionaries and sets.
- Classes and objects.
- Type hints.
- Exceptions.
- Modules and imports.
- Basic unit testing with `pytest`.

### Exercises

1. Implement a function that calculates the arithmetic mean of a list of numbers.
2. Implement a function that returns the minimum and maximum values.
3. Create a simple `BankAccount` class with deposit and withdrawal methods.
4. Add type hints to all public functions and methods.
5. Write tests for normal cases and invalid inputs.

### Acceptance Criteria

- Functions have meaningful names and type hints.
- Invalid inputs are handled explicitly.
- Code follows basic Python conventions.
- Tests cover normal and edge cases.

---

## 5. Linear Algebra — MIT 18.06SC

**Estimated time:** 1 hour

### Assigned lectures

**Lecture 1 — The Geometry of Linear Equations**

Focus on:

- What is a linear equation?
- Geometric interpretation of equations.
- Systems of linear equations.
- Vectors as mathematical objects.
- Linear combinations.

**Lecture 2 — Elimination with Matrices**

Start this lecture if time permits. Focus on the relationship between systems of equations and matrices.

### Study Instructions

For each lecture:

1. Watch the explanation.
2. Write down the main definitions.
3. Reproduce important mathematical derivations.
4. Solve at least one related exercise.
5. Explain the main idea without looking at your notes.

### Learning Outcome

Understand why vectors and matrices are fundamental representations of data and transformations in machine learning.

---

## 6. Mathematics — Vector Operations

**Estimated time:** 30 minutes

Consider two vectors:

$$
\begin{aligned}
a &= [2, 3, 4]\\
b &= [1, 5, 2]
\end{aligned}
$$

### 6.1 Vector Addition

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

### 6.2 Scalar Multiplication

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

### 6.3 Dot Product

$$
\begin{aligned}
a \cdot b
&= 2 \cdot 1 + 3 \cdot 5 + 4 \cdot 2\\
&= 2 + 15 + 8\\
&= 25
\end{aligned}
$$

### 6.4 Euclidean Norm (L2 Norm)

$$
\begin{aligned}
\|a\|_2
&= \sqrt{2^2 + 3^2 + 4^2}\\
&= \sqrt{4 + 9 + 16}\\
&= \sqrt{29}
\end{aligned}
$$

### Exercises

1. Calculate the sum of two vectors manually.
2. Calculate the dot product of two vectors.
3. Calculate the Euclidean norm.
4. Explain why vectors with different dimensions cannot be added.
5. Explain the geometric meaning of the dot product.

Perform the calculations manually before verifying them with Python.

---

## 7. Implementation — Vector Class

**Estimated time:** 1.5 hours

Create:

`foundations/mathematics/linear-algebra/vector.py`

Implement a `Vector` class without using NumPy.

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

You may additionally implement:

- `__eq__`
- `__repr__`
- `__len__`

### Requirements

- Support vector addition.
- Support scalar multiplication.
- Implement the dot product.
- Implement the Euclidean norm.
- Validate dimensions.
- Return new vectors instead of modifying existing ones.
- Raise meaningful exceptions for invalid operations.

### Example

```python
a = Vector([2, 3, 4])
b = Vector([1, 5, 2])

print(a + b)          # [3, 8, 6]
print(a * 3)          # [6, 9, 12]
print(a.dot(b))       # 25
print(a.magnitude())  # sqrt(29)
```

---

## 8. Unit Testing

Create:

`foundations/mathematics/linear-algebra/test_vector.py`

Use `pytest`.

### Required test cases

- Vector addition.
- Scalar multiplication.
- Dot product.
- Euclidean norm.
- Zero vector.
- Empty vector behavior.
- Dimension mismatch.
- Equality.
- Negative scalar multiplication.

Run:

```bash
pytest -v
```

**Acceptance Criteria:** All tests pass. NumPy is not used anywhere in the implementation.

---

## 9. MAANG Interview Preparation — Two Sum

**Estimated time:** 1 hour

Problem:

Given an array of integers and a target value, return the indices of two numbers whose sum equals the target.

Example:

```python
nums = [2, 7, 11, 15]
target = 9

# Expected output: [0, 1]
```

### Task A — Brute Force

Implement the solution using nested loops.

Expected complexity:

- Time: `O(n²)`
- Extra space: `O(1)`

### Task B — Hash Map

Implement an optimized solution using a Python dictionary.

Hint:

```python
complement = target - current
```

Check whether the complement already exists in the dictionary.

Expected complexity:

- Time: `O(n)` average case
- Extra space: `O(n)`

### Edge Cases

Test:

- Two elements.
- Negative numbers.
- Duplicate values.
- Zero values.
- No valid pair.
- Multiple possible pairs.

### Interview Practice

Be able to explain:

1. Why does the brute-force approach work?
2. Why is the hash-map approach faster?
3. What is the time-space trade-off?
4. What happens if the input contains duplicate values?

---

## 10. Mini Experiment

**Estimated time:** 30 minutes

Compare both Two Sum implementations using synthetic inputs.

Suggested input sizes:

- 100
- 1,000
- 5,000
- 10,000

Use Python's `time.perf_counter()`.

Record the results:

| Input Size | Brute Force | Hash Map |
| ---------: | ----------: | -------: |
|        100 |             |          |
|      1,000 |             |          |
|      5,000 |             |          |
|     10,000 |             |          |

### Experiment Guidelines

- Run each benchmark multiple times.
- Use the same input for both implementations.
- Record the measurement conditions.
- Avoid drawing conclusions from a single run.
- Explain whether the observed behavior matches theoretical complexity.

---

## 11. Deliverables

Expected repository structure:

```text
ai-research-engineer-academy/
├── foundations/
│   └── mathematics/
│       └── linear-algebra/
│           ├── vector.py
│           └── test_vector.py
└── weeks/
    └── week-001/
        ├── README.md
        ├── notes.md
        ├── exercises/
        │   ├── python_basics.py
        │   └── two_sum.py
        ├── tests/
        └── results/
            └── benchmark.md
```

### Required Deliverables

1. Working Python exercises.
2. Vector implementation.
3. Passing unit tests.
4. Two Sum brute-force implementation.
5. Two Sum hash-map implementation.
6. Complexity analysis.
7. Benchmark results.
8. Mathematics notes.
9. Weekly retrospective.

---

## 12. Definition of Done

- [ ] Python environment is configured.
- [ ] Python exercises are implemented.
- [ ] MIT Lecture 1 is completed.
- [ ] Main mathematical concepts are understood.
- [ ] Vector class is implemented without NumPy.
- [ ] All vector tests pass.
- [ ] Both Two Sum solutions are implemented.
- [ ] Time and space complexity are documented.
- [ ] Benchmark results are recorded.
- [ ] Weekly notes are written in your own words.
- [ ] At least one MAANG problem can be explained verbally.

---

## 13. Weekly Self-Assessment

Rate each dimension from 1 to 5.

| Dimension                   | Score |
| --------------------------- | ----: |
| Python understanding        |    /5 |
| Mathematical understanding  |    /5 |
| Implementation quality      |    /5 |
| Testing and experimentation |    /5 |
| Technical communication     |    /5 |

A score of 3 means you can complete the task independently and explain the main ideas.

A score of 5 means you can also explain design trade-offs, edge cases, limitations and alternative approaches.

Do not mark a topic as mastered simply because the code works.

---

## 14. Weekly Retrospective

Complete `notes.md` by answering:

1. What did I learn this week?
2. Which mathematical concept was the most difficult?
3. Which Python feature was unfamiliar?
4. What implementation decision would I change?
5. Can I explain the dot product without looking at my notes?
6. Can I explain why the hash-map solution is faster?
7. What should I review before Week 002?

**Final goal:** Build a solid foundation in Python and vector mathematics. These concepts will be reused throughout the entire AI Research Engineer Academy programme.
