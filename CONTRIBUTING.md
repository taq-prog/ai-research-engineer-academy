# Contributing to AI Research Engineer Academy

Thank you for contributing to the AI Research Engineer Academy.

This repository is primarily a structured, long-term learning project. Its goal is to develop practical skills in mathematics, machine learning, deep learning, LLM engineering, and independent research.

The contribution process is designed to keep the repository:

- Reproducible.
- Well-documented.
- Easy to navigate.
- Technically correct.
- Useful as a professional portfolio.

Even when working alone, follow these guidelines to maintain consistent engineering standards.

---

# 1. Repository Structure

The repository separates learning activities, reusable implementations, research artifacts, and portfolio projects.

```text
ai-research-engineer-academy/
├── README.md
├── ROADMAP.md
├── CURRICULUM.md
├── PROGRESS.md
├── CONTRIBUTING.md
├── docs/
├── resources/
├── foundations/
├── weeks/
├── projects/
├── papers/
├── experiments/
├── src/
└── tests/
```

## Directory responsibilities

| Directory        | Purpose                                                      |
| ---------------- | ------------------------------------------------------------ |
| `docs/`        | Learning strategy, engineering standards, research workflows |
| `resources/`   | Books, courses, papers, and documentation                    |
| `foundations/` | Reusable mathematics and Python implementations              |
| `weeks/`       | Weekly exercises, notes, and learning evidence               |
| `projects/`    | Larger, portfolio-oriented projects                          |
| `papers/`      | Paper analysis and reproduction work                         |
| `experiments/` | Experiment configurations, results, and reports              |
| `src/`         | Reusable Python package code                                 |
| `tests/`       | Tests for shared package functionality                       |

Do not create all 104 weekly directories in advance. Create a weekly directory when work on that week begins.

---

# 2. Weekly Learning Workflow

Each week follows a consistent workflow.

1. Read the weekly assignment in `CURRICULUM.md`.
2. Identify the expected learning outcomes.
3. Review the required theory and mathematical concepts.
4. Implement the assigned exercises.
5. Write and run tests.
6. Perform experiments where applicable.
7. Document findings and unresolved questions.
8. Review the acceptance criteria.
9. Update `PROGRESS.md`.

The weekly folder is the source of truth for that week's learning artifacts.

## Weekly directory template

```text
weeks/week-NNN/
├── README.md
├── notes.md
├── exercises/
├── src/
├── tests/
└── results/
```

### README.md

Describe:

- Weekly objectives.
- Prerequisites.
- Assigned tasks.
- Expected deliverables.
- Acceptance criteria.
- References.

### notes.md

Record:

- Key concepts.
- Mathematical derivations.
- Important observations.
- Common mistakes.
- Questions that remain unanswered.
- Links to relevant implementations.

### exercises/

Store independent exercises and problem-solving attempts.

### src/

Store implementations created during the week.

### tests/

Store automated tests for weekly implementations.

### results/

Store benchmarks, experiment outputs, plots, and short reports.

---

# 3. Coding Standards

Python is the primary language for mathematical implementations, ML experiments, and research reproductions.

Use C#/.NET where it provides a meaningful comparison or demonstrates production engineering concepts. Do not introduce additional languages without a clear learning objective.

## Python version

- Python 3.11 or newer.
- Use a virtual environment.
- Declare project dependencies.
- Avoid unnecessary dependencies in foundational exercises.

## Code quality

Use:

- Ruff for linting and formatting.
- pytest for automated testing.
- Type hints for public functions and classes.
- Clear and descriptive names.
- Small, focused functions.
- Explicit error handling where appropriate.

Example:

```python
def dot_product(left: list[float], right: list[float]) -> float:
    """Calculate the dot product of two vectors."""
    if len(left) != len(right):
        raise ValueError("Vectors must have the same dimension.")

    return sum(a * b for a, b in zip(left, right))
```

## Mathematical implementations

For foundational exercises, implement algorithms from scratch before using high-level libraries.

For example:

| Topic             | First implementation | Later comparison          |
| ----------------- | -------------------- | ------------------------- |
| Vector operations | Pure Python          | NumPy                     |
| Matrix operations | Pure Python          | NumPy                     |
| Linear regression | From scratch         | scikit-learn              |
| Gradient descent  | From scratch         | PyTorch                   |
| Neural networks   | NumPy                | PyTorch                   |
| Attention         | PyTorch operations   | Optimized implementations |

The purpose is to understand the underlying mechanics, not to avoid mature libraries permanently.

Always distinguish between:

- Educational implementations.
- Production-ready implementations.
- Optimized research implementations.

---

# 4. Testing Requirements

Every reusable implementation should have automated tests.

Tests should cover:

- Normal inputs.
- Boundary conditions.
- Invalid inputs.
- Expected mathematical properties.
- Numerical precision where applicable.

For mathematical code, prefer property-based reasoning in addition to individual examples.

Example:

```python
def test_dot_product_is_commutative():
    left = [1.0, 2.0, 3.0]
    right = [4.0, 5.0, 6.0]

    assert dot_product(left, right) == dot_product(right, left)
```

For floating-point calculations, use `pytest.approx` where appropriate.

Do not accept an implementation merely because it produces the expected output for one example.

---

# 5. Experiment Standards

Experiments must be reproducible and clearly documented.

Each non-trivial experiment should record:

| Field          | Description                       |
| -------------- | --------------------------------- |
| Objective      | What are we trying to understand? |
| Hypothesis     | What do we expect to happen?      |
| Baseline       | What are we comparing against?    |
| Configuration  | Parameters and environment        |
| Dataset        | Data source and preprocessing     |
| Metrics        | How will success be measured?     |
| Results        | Actual observations               |
| Interpretation | What do the results mean?         |
| Limitations    | What cannot be concluded?         |

## Experiment directory

```text
experiments/
└── experiment-name/
    ├── README.md
    ├── config.yaml
    ├── run.py
    ├── results/
    └── report.md
```

## Reproducibility rules

- Record random seeds when applicable.
- Record dependency versions.
- Record hardware details for performance experiments.
- Store configuration files.
- Separate training, validation, and test data correctly.
- Never report expected results as measured results.
- Document failed experiments when they provide useful information.

Do not commit large datasets, model checkpoints, or generated artifacts without a clear reason. Prefer documented download instructions or appropriate artifact storage.

---

# 6. Research Paper Guidelines

Every paper analysis should distinguish between understanding, implementation, and reproduction.

A paper is not considered reproduced just because its architecture has been implemented.

## Paper analysis template

Each paper directory should contain:

```text
papers/paper-name/
├── README.md
├── paper-notes.md
├── mathematical-derivations.md
├── implementation/
├── experiments/
└── reproduction-report.md
```

### README.md

Include:

- Paper title.
- Authors.
- Publication venue and year.
- Official paper URL.
- Repository URL, if available.
- Main research contribution.
- Current reproduction status.

### paper-notes.md

Explain:

- Problem statement.
- Motivation.
- Related work.
- Main ideas.
- Architecture.
- Training methodology.
- Evaluation methodology.
- Limitations.

### mathematical-derivations.md

Record important equations and explain their meaning.

Do not copy equations without understanding their variables, assumptions, and role in the method.

### reproduction-report.md

Compare:

- Original paper results.
- Reproduced results.
- Experimental conditions.
- Differences in implementation.
- Possible explanations for discrepancies.

Clearly label partial reproductions.

---

# 7. Documentation Standards

Documentation should be written in English.

This improves technical writing skills and makes the repository accessible to an international engineering audience.

Use:

- Clear technical language.
- Short paragraphs.
- Descriptive headings.
- Working links.
- Code examples where useful.
- Mathematical notation where necessary.

Prefer explanations that answer:

1. What is it?
2. Why does it matter?
3. How does it work?
4. How can it be implemented?
5. How can it be tested?

When referencing an external resource, include its original URL and relevant bibliographic details.

Do not invent page numbers, chapter references, publication details, or experimental results.

---

# 8. Git Workflow

Use small, focused commits with descriptive messages.

Suggested commit format:

```text
<type>(<scope>): <description>
```

Examples:

```text
docs(week-001): add vector foundations notes
feat(foundations): implement vector operations
test(week-001): add vector unit tests
experiment(week-010): compare gradient descent learning rates
docs(papers): add attention paper analysis
fix(project): correct tensor shape validation
```

Suggested types:

| Type           | Purpose                             |
| -------------- | ----------------------------------- |
| `feat`       | New implementation or capability    |
| `fix`        | Bug fix                             |
| `test`       | Tests                               |
| `docs`       | Documentation                       |
| `refactor`   | Code restructuring                  |
| `experiment` | Experiment configuration or results |
| `chore`      | Maintenance                         |

Keep commits focused on one logical change.

Use branches for larger or experimental changes when useful. A pull request can be used even for solo work as a lightweight review checkpoint.

---

# 9. Definition of Done

A task is complete only when its expected deliverables are available and verified.

## Code task

- [ ] Implementation exists.
- [ ] Correctness has been checked.
- [ ] Relevant tests exist.
- [ ] Tests pass.
- [ ] Code is formatted and linted.
- [ ] Complexity is documented when relevant.

## Mathematics task

- [ ] Concepts are explained in my own words.
- [ ] Important equations are understood.
- [ ] Derivations are documented where required.
- [ ] At least one practical example is available.
- [ ] Remaining gaps are recorded.

## Experiment task

- [ ] Hypothesis is documented.
- [ ] Baseline is defined.
- [ ] Configuration is saved.
- [ ] Results are reproducible.
- [ ] Conclusions are supported by evidence.
- [ ] Limitations are documented.

## Documentation task

- [ ] Content is technically accurate.
- [ ] Links work.
- [ ] Code examples are valid.
- [ ] Claims are supported by sources or experiments.
- [ ] English is clear and consistent.

---

# 10. Pull Request Review Checklist

Before merging a significant change, review it as if another engineer were evaluating the repository.

- [ ] Does this change support the Academy learning objectives?
- [ ] Is the implementation understandable?
- [ ] Are mathematical assumptions explicit?
- [ ] Are tests meaningful?
- [ ] Are experiment results supported by evidence?
- [ ] Is documentation sufficient to reproduce the work?
- [ ] Does the change avoid unnecessary dependencies?
- [ ] Are existing files and progress records consistent?

For research-related changes, also ask:

- [ ] Is the original method represented accurately?
- [ ] Are deviations from the paper documented?
- [ ] Are comparisons fair?
- [ ] Are conclusions appropriately limited?

---

# 11. Learning Integrity

The Academy prioritizes genuine understanding over superficial completion.

Follow these principles:

1. Attempt important exercises independently before looking at solutions.
2. Use AI assistants as tutors and reviewers, not as substitutes for understanding.
3. Be able to explain code you submit.
4. Reimplement important algorithms without copying a tutorial.
5. Verify AI-generated mathematical explanations and code.
6. Preserve failed experiments and useful debugging notes.
7. Never claim to have reproduced a result without evidence.
8. Record assistance from external sources when it materially affects an implementation.

Using tools is encouraged. Blindly relying on them is not.

---

# 12. Final Principle

Treat this repository as both a learning environment and a professional engineering portfolio.

Every substantial contribution should demonstrate at least one of the following:

- Deeper theoretical understanding.
- Stronger mathematical reasoning.
- Better implementation skills.
- More reliable experiments.
- Improved research methodology.
- Clearer technical communication.

**The objective is not to accumulate code. The objective is to develop the ability to understand, implement, evaluate, and improve machine learning systems independently.**
