# Learning Strategy

This document defines the learning methodology used throughout the AI Research Engineer Academy.

The objective is not simply to complete courses or read technical books. The objective is to develop the ability to understand, implement, evaluate, and improve machine learning systems independently.

The Academy uses a combination of deliberate practice, active recall, mathematical reasoning, implementation from scratch, experimentation, and technical communication.

---

# 1. Learning Philosophy

The Academy follows five principles.

## 1.1 Understand before optimizing

First understand the mathematical and conceptual foundations.

Then implement a simple version.

Only after validating correctness should you optimize performance.

For example, when learning gradient descent:

1. Understand the optimization problem.
2. Derive the gradient mathematically.
3. Implement gradient descent using basic Python or NumPy.
4. Verify the implementation on a simple function.
5. Experiment with learning rates.
6. Compare the results with a mature library.

Do not start with a highly optimized framework implementation before understanding the underlying algorithm.

## 1.2 Build, don't just consume

Passive learning has a limited role.

Watching lectures and reading books are useful, but they do not demonstrate that you can apply the knowledge.

For every major concept, produce at least one concrete artifact:

- Mathematical derivation.
- Python implementation.
- Unit tests.
- Experiment.
- Technical explanation.

## 1.3 Learn through retrieval

Try to recall information without looking at your notes.

Examples:

- Explain matrix multiplication from memory.
- Derive the gradient of mean squared error.
- Implement logistic regression without following a tutorial.
- Explain why attention uses scaled dot products.
- Describe the difference between training and inference.

If you cannot explain a concept without copying an explanation, revisit it.

## 1.4 Use progressive difficulty

Move through three levels:

| Level          | Activity                     | Expected result          |
| -------------- | ---------------------------- | ------------------------ |
| 1. Understand  | Read, derive, explain        | Conceptual understanding |
| 2. Implement   | Code, test, debug            | Working implementation   |
| 3. Investigate | Experiment, compare, analyze | Independent reasoning    |

Do not skip foundational levels merely because a library makes implementation easy.

## 1.5 Treat mistakes as evidence

A failed implementation or unexpected result is useful information.

Record:

- What you expected.
- What actually happened.
- Why the difference occurred.
- How you diagnosed the issue.
- What you learned.

The ability to investigate unexpected behavior is an important research engineering skill.

---

# 2. Weekly Learning Schedule

The Academy is designed around 5–7 hours per week.

A typical target is approximately 6 hours.

| Activity           |          Weekly time | Purpose                          |
| ------------------ | -------------------: | -------------------------------- |
| Theory and reading |            1–1.25 h | Understand concepts              |
| Mathematics        |            0.75–1 h | Develop mathematical foundations |
| Implementation     |         1.75–2.25 h | Turn theory into code            |
| Experiments        |               0.75 h | Validate and investigate         |
| Notes and review   |               0.25 h | Consolidate knowledge            |
| MAANG preparation  |                  1 h | Maintain interview readiness     |
| **Total**    | **5.5–6.5 h** |                                  |

This is a flexible allocation, not a rigid timetable.

Some weeks require more mathematical work. Others require more implementation or experimentation.

The goal is to maintain consistency without sacrificing understanding.

## Recommended session structure

For a 60-minute learning session:

1. 5 minutes — recall previous knowledge.
2. 15 minutes — study a new concept.
3. 30 minutes — solve a problem or implement something.
4. 10 minutes — summarize what was learned.

For longer sessions, extend implementation and experimentation time.

---

# 3. Active Recall

Active recall means retrieving knowledge from memory instead of repeatedly rereading material.

Use it throughout the Academy.

## Before studying

Write down what you already know about the topic.

Example:

**Topic: Eigenvalues**

Questions:

- What is an eigenvector?
- What does an eigenvalue represent?
- Why are eigenvalues useful?
- Where might they appear in machine learning?

Do not worry if your answers are incomplete.

## After studying

Close the book or lecture and answer:

1. What is the central idea?
2. What problem does it solve?
3. What assumptions does it make?
4. Can I explain the equations?
5. Can I implement a basic example?

## Weekly recall test

At the end of every week:

- Explain the key concepts without notes.
- Solve at least one problem independently.
- Reconstruct an important equation or algorithm.
- Identify remaining knowledge gaps.

Store questions and answers in `weeks/week-NNN/notes.md`.

---

# 4. Spaced Repetition

Important concepts should be revisited over time.

Use the following review intervals as a starting point:

| Review | When            | Purpose                    |
| ------ | --------------- | -------------------------- |
| First  | Same day        | Initial consolidation      |
| Second | 1 day later     | Check short-term retention |
| Third  | 3–4 days later | Reinforce understanding    |
| Fourth | 7 days later    | Check independent recall   |
| Fifth  | 30 days later   | Long-term retention        |

These intervals are guidelines, not mandatory sessions.

If a concept is difficult, revisit it more frequently.

If you can explain and apply it confidently, move on.

## What should be reviewed?

Prioritize:

- Mathematical definitions.
- Important equations.
- Algorithmic complexity.
- Common implementation patterns.
- ML concepts.
- Architecture decisions.
- Experimental conclusions.

Do not create flashcards for every paragraph in a book.

Use flashcards for information that benefits from repeated recall.

---

# 5. Mathematics Learning Method

Mathematics is a core part of becoming an effective research engineer.

The objective is to understand mathematical concepts well enough to derive, implement, and reason about ML algorithms.

## The four-step method

For every important mathematical concept:

### Step 1 — Understand the intuition

Explain the idea in simple language.

Example:

A vector represents a quantity with magnitude and direction.

### Step 2 — Understand the formal definition

Study the notation, assumptions, and mathematical properties.

### Step 3 — Work through examples

Solve numerical examples manually.

Do not immediately use NumPy or SymPy.

### Step 4 — Implement it

Write a small Python implementation and test it.

For example:

- Vector addition.
- Dot product.
- Matrix multiplication.
- Gaussian elimination.
- Gradient calculation.
- Probability distributions.

## Mathematics acceptance criteria

You should be able to:

- Explain the concept.
- Understand the notation.
- Solve a basic problem manually.
- Implement a numerical example.
- Identify common assumptions and limitations.

A mathematical formula is not understood simply because it looks familiar.

---

# 6. Implementation-First Learning

The Academy emphasizes implementing important algorithms from scratch before relying on high-level abstractions.

This is especially important in the first learning phases.

## Implementation workflow

1. Define the problem.
2. Write down the mathematical formulation.
3. Identify inputs and outputs.
4. Design a simple algorithm.
5. Implement the algorithm.
6. Write tests.
7. Validate against known examples.
8. Compare with an established library.
9. Document limitations and complexity.

## Example: Linear Regression

A useful learning sequence:

1. Implement prediction using $y = wx + b$.
2. Implement mean squared error.
3. Derive gradients for $w$ and $b$.
4. Implement gradient descent.
5. Train on synthetic data.
6. Experiment with learning rates.
7. Compare with scikit-learn.
8. Explain why the results differ, if they do.

## When to use libraries

| Library      | Appropriate use                             |
| ------------ | ------------------------------------------- |
| NumPy        | Numerical arrays and vectorized operations  |
| SciPy        | Scientific computing and numerical methods  |
| SymPy        | Symbolic mathematics and derivations        |
| pandas       | Tabular data processing                     |
| scikit-learn | Classical ML algorithms and evaluation      |
| PyTorch      | Deep learning and automatic differentiation |
| Transformers | Modern pretrained model workflows           |

Libraries are tools for productive engineering. Understanding their abstractions is part of the learning process.

---

# 7. Experiment-Driven Learning

An experiment should answer a specific question.

Avoid running experiments without a hypothesis or a clear evaluation method.

## Experimental workflow

### 1. Question

What do you want to understand?

Example:

How does the learning rate affect gradient descent convergence?

### 2. Hypothesis

What do you expect?

Example:

A learning rate that is too high may cause divergence or oscillation.

### 3. Baseline

Define a reference implementation or configuration.

### 4. Variables

Change one major variable at a time whenever possible.

### 5. Measurements

Choose metrics appropriate to the question.

### 6. Results

Record actual observations.

### 7. Interpretation

Explain why the results occurred.

### 8. Limitations

Identify what the experiment cannot establish.

## Example experiment

**Question:** How does batch size affect training behavior?

Possible measurements:

- Training loss.
- Validation loss.
- Training time.
- GPU memory usage.
- Throughput.

Keep the dataset, model, optimizer, and other relevant settings controlled.

A useful experiment is not necessarily one that confirms the hypothesis. Unexpected results can be more informative.

---

# 8. Reading Technical Books and Courses

Use one primary learning resource per phase.

Supplement it with official documentation and selected lectures.

Avoid collecting many overlapping courses.

## Reading workflow

For each assigned section:

1. Preview the section headings.
2. Identify the central question.
3. Read actively.
4. Write down important equations.
5. Close the resource.
6. Explain the material in your own words.
7. Solve a related problem.
8. Record unresolved questions.

## Avoid passive reading

Do not measure progress by pages read or videos watched.

Measure progress by what you can explain and implement afterward.

## Resource selection

Prefer this order:

1. Primary textbook or course.
2. Official documentation.
3. Original research paper.
4. Supplementary explanations.
5. Community discussions when additional context is useful.

Use supplementary resources to resolve specific questions, not to continuously switch between courses.

---

# 9. Research Paper Reading Workflow

Paper reading becomes a central activity during the research reproduction phase.

However, basic research reading skills should be developed earlier.

Do not expect to understand every equation on the first reading.

## First pass — Understand the contribution

Spend approximately 15–30 minutes.

Read:

- Title.
- Abstract.
- Introduction.
- Figures and tables.
- Conclusion.

Answer:

1. What problem does the paper address?
2. Why is the problem important?
3. What is the main contribution?
4. What are the reported results?
5. What should I investigate further?

## Second pass — Understand the method

Study:

- Related work.
- Model architecture.
- Mathematical formulation.
- Training procedure.
- Datasets.
- Evaluation methodology.

Create a diagram or a structured explanation of the method.

## Third pass — Reconstruct the implementation

Identify:

- Inputs and outputs.
- Model components.
- Tensor shapes.
- Important equations.
- Training objectives.
- Optimization settings.
- Evaluation procedure.

Try to explain the algorithm without referring to the original paper.

## Fourth pass — Reproduce

Follow this sequence:

1. Establish a baseline.
2. Implement the method.
3. Validate the implementation.
4. Run experiments.
5. Compare results.
6. Investigate discrepancies.
7. Write a reproduction report.

## Paper reading notes

For every paper, record:

```markdown
# Paper Notes

## Bibliographic Information

- Title:
- Authors:
- Year:
- Venue:
- URL:

## Research Problem

What problem does the paper solve?

## Motivation

Why is the problem important?

## Main Contribution

What is new?

## Method

How does the proposed method work?

## Mathematics

Which equations are essential?

## Experiments

Which datasets, metrics, and baselines are used?

## Results

What did the authors demonstrate?

## Limitations

What assumptions or weaknesses exist?

## My Understanding

Explain the paper in my own words.

## Questions

What do I still not understand?

## Reproduction Plan

What would be required to reproduce the main results?
```

---

# 10. Using AI Assistants Effectively

AI assistants can accelerate learning, but they must not replace independent reasoning.

Use them as:

- Tutors.
- Code reviewers.
- Mathematical explanation assistants.
- Debugging partners.
- Experiment design reviewers.
- Research discussion partners.

## Recommended workflow

### Before asking AI

Attempt the problem independently.

Write down:

- Your understanding.
- Your approach.
- Your implementation.
- The exact point where you are stuck.

### While asking AI

Prefer questions that reveal reasoning.

Good examples:

- Explain why this gradient has this form.
- Give me a hint without revealing the full solution.
- Review my implementation and identify edge cases.
- Challenge my explanation of this paper.
- What experiment would distinguish these two hypotheses?

Avoid immediately requesting a complete implementation.

### After receiving help

1. Verify the explanation.
2. Reimplement the solution independently.
3. Run tests.
4. Explain the result without copying the response.
5. Record important corrections.

## Verification rules

AI-generated content may contain:

- Incorrect mathematical derivations.
- Incorrect tensor shapes.
- Outdated APIs.
- Incorrect benchmark interpretations.
- Unsupported claims about papers.

Verify important claims against textbooks, official documentation, source code, or experimental evidence.

---

# 11. Balancing AI Academy and MAANG Preparation

The Academy should complement existing software engineering experience, not replace it.

Maintain a small but consistent interview preparation track.

Suggested weekly allocation:

| Area              |    Weekly time |
| ----------------- | -------------: |
| AI Academy        | 4.5–5.5 hours |
| MAANG preparation |         1 hour |

The MAANG track should rotate between:

- Algorithms and data structures.
- C# standard library.
- Async/await and multithreading.
- Practical coding exercises.
- System design.
- Behavioral and leadership examples.

Do not attempt to prepare for every interview topic every week.

Use focused practice and revisit weak areas.

---

# 12. Learning Environment

Keep the toolchain simple.

| Tool           | Responsibility                         |
| -------------- | -------------------------------------- |
| Python         | Primary learning and research language |
| VS Code        | Development environment                |
| Git and GitHub | Version control and portfolio          |
| pytest         | Automated testing                      |
| Ruff           | Formatting and linting                 |
| NumPy          | Numerical computing                    |
| PyTorch        | Deep learning                          |
| Jupyter        | Interactive experimentation            |
| Obsidian       | Personal knowledge base                |
| ChatGPT        | Tutor and reviewer                     |

Use local GPU resources when they provide a meaningful benefit.

Do not optimize the environment prematurely.

Start with CPU-compatible exercises. Introduce CUDA and GPU-specific tooling when the curriculum reaches deep learning and performance engineering.

Record hardware and software versions when running performance-sensitive experiments.

---

# 13. Monthly Learning Review

Every four weeks, evaluate the learning process itself.

Answer:

1. Did I understand the material or merely finish it?
2. Can I implement important concepts independently?
3. Which mathematical topics remain difficult?
4. Did I run meaningful experiments?
5. Did I maintain the weekly time budget?
6. Which learning activities produced the most value?
7. What should I change in the next month?

## Monthly review outcomes

Choose one:

- Continue with the current approach.
- Increase practice in a weak area.
- Reduce unnecessary supplementary resources.
- Revisit foundational topics.
- Adjust the weekly workload.

The curriculum should remain challenging but sustainable.

---

# 14. Research Engineer Mindset

Throughout the Academy, develop the following habits:

- Ask precise questions.
- Understand assumptions.
- Derive important equations.
- Build minimal implementations.
- Test edge cases.
- Measure performance.
- Compare against baselines.
- Investigate unexpected results.
- Document limitations.
- Communicate conclusions clearly.

The goal is to move from following instructions to making independent technical decisions.

---

# 15. Final Learning Rule

A topic is not mastered because it has been read, watched, or copied.

A topic is mastered when you can:

1. Explain it clearly.
2. Derive its important mathematics.
3. Implement a working version.
4. Test its correctness.
5. Evaluate its behavior.
6. Explain its limitations.
7. Apply it to a new problem.

**Learn the theory. Derive the mathematics. Build the implementation. Run the experiment. Explain the result.**

That is the learning loop of the AI Research Engineer Academy.
