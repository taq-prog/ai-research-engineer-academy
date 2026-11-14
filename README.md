# AI Research Engineer Academy

A structured, hands-on learning path from Senior Software Engineer to AI / ML Research Engineer.

The goal of this repository is to build a strong foundation in mathematics, machine learning, deep learning, and modern language models — and gradually develop the ability to understand research papers, reproduce published results, and conduct independent experiments.

This is a long-term learning project focused on **understanding how AI systems work, implementing them from scratch, and learning through research and experimentation.**

## 🎯 Goals

By the end of this learning path, the objectives are to:

- Build a solid foundation in linear algebra, calculus, probability, and statistics.
- Become proficient in Python and the scientific Python ecosystem.
- Understand classical machine learning algorithms and implement core methods from scratch.
- Develop practical experience with PyTorch and deep learning architectures.
- Understand Transformers, LLM architectures, pretraining, and fine-tuning.
- Read and critically analyze research papers.
- Reproduce selected research papers and compare results with published findings.
- Understand GPU computing, model optimization, and ML systems.
- Design and conduct independent ML experiments.
- Build a portfolio demonstrating practical AI and research engineering skills.

## 🗺️ Learning Roadmap

The curriculum is organized into eight phases over approximately 104 weeks.

| Phase |   Weeks | Focus                            |
| ----- | ------: | -------------------------------- |
| 1     |   1–12 | Mathematics & Python Foundations |
| 2     |  13–24 | Classical Machine Learning       |
| 3     |  25–40 | Deep Learning & PyTorch          |
| 4     |  41–56 | NLP & Transformers               |
| 5     |  57–68 | LLM Training & Fine-tuning       |
| 6     |  69–84 | Research Paper Reproduction      |
| 7     |  85–96 | ML Systems, GPU & Performance    |
| 8     | 97–104 | Independent Research & Portfolio |

See [ROADMAP.md](ROADMAP.md) for the high-level learning plan and [CURRICULUM.md](CURRICULUM.md) for the detailed weekly syllabus.

## ⏱️ Weekly Commitment

The planned workload is approximately **5–7 hours per week**.

A typical week includes:

- Theory and reading
- Mathematics exercises
- Coding and implementation
- Experiments and evaluation
- Technical notes and documentation
- A small amount of software engineering interview preparation

The schedule is designed for sustainable progress alongside a full-time engineering job.

## 🧠 Learning Philosophy

The curriculum follows a practical, implementation-driven approach:

1. **Understand** — learn the mathematical and conceptual foundations.
2. **Derive** — understand the equations and algorithms behind the methods.
3. **Implement** — build core algorithms from scratch where appropriate.
4. **Experiment** — test hypotheses and investigate model behavior.
5. **Evaluate** — compare results using meaningful metrics and baselines.
6. **Document** — explain findings, limitations, and conclusions.

The emphasis is not on completing courses or collecting certificates. The objective is to develop the ability to reason about ML systems and solve problems independently.

## 📂 Repository Structure

```text
ai-research-engineer-academy/
├── README.md
├── ROADMAP.md
├── CURRICULUM.md
├── PROGRESS.md
├── CONTRIBUTING.md
├── pyproject.toml
│
├── docs/
│   ├── learning-strategy.md
│   ├── evaluation-rubric.md
│   ├── research-workflow.md
│   └── glossary.md
│
├── resources/
│   ├── books.md
│   ├── courses.md
│   ├── papers.md
│   └── documentation.md
│
├── foundations/
│   ├── mathematics/
│   │   ├── linear-algebra/
│   │   ├── calculus/
│   │   └── probability-statistics/
│   └── python/
│
├── weeks/
│   ├── README.md
│   └── week-001/
│       ├── README.md
│       ├── notes.md
│       ├── exercises/
│       ├── src/
│       ├── tests/
│       └── results/
│
├── projects/
│   ├── 01-ml-from-scratch/
│   ├── 02-neural-network-from-scratch/
│   ├── 03-transformer-from-scratch/
│   ├── 04-small-language-model/
│   └── 05-independent-research/
│
├── papers/
│   ├── README.md
│   ├── attention-is-all-you-need/
│   ├── bert/
│   ├── gpt-2/
│   ├── chinchilla/
│   ├── lora/
│   └── flash-attention/
│
├── experiments/
│   ├── README.md
│   └── templates/
│
└── .github/
    └── workflows/
        ├── tests.yml
        └── lint.yml
```

Directories and modules will be introduced progressively as the curriculum evolves.

## 🔬 Research Workflow

Each paper reproduction or independent research project should follow a consistent workflow:

1. Select a research paper or formulate a research question.
2. Study the problem, assumptions, and proposed approach.
3. Understand the relevant mathematical foundations.
4. Implement the baseline or reproduce the original method.
5. Define datasets, metrics, and experimental conditions.
6. Run experiments and record results.
7. Compare findings with the original paper.
8. Document deviations, limitations, and conclusions.

See [docs/research-workflow.md](docs/research-workflow.md) for the planned research workflow.

## 📊 Progress Tracking

Progress is evaluated across five dimensions:

| Area                                | Weight |
| ----------------------------------- | -----: |
| Theory and conceptual understanding |    20% |
| Mathematics                         |    20% |
| Implementation                      |    25% |
| Experiments and evaluation          |    20% |
| Technical communication             |    15% |

The objective is to demonstrate understanding through working implementations, reproducible experiments, and clear technical explanations.

See [PROGRESS.md](PROGRESS.md) for progress tracking and [docs/evaluation-rubric.md](docs/evaluation-rubric.md) for evaluation criteria.

## 🛠️ Technology Stack

The primary tools and technologies planned for this journey:

- **Python** — primary language for ML and research.
- **NumPy** — numerical computing.
- **Pandas** — data manipulation.
- **Matplotlib** — visualization.
- **scikit-learn** — classical machine learning.
- **PyTorch** — deep learning and neural networks.
- **Jupyter** — interactive experimentation.
- **pytest** — testing.
- **Ruff** — Python linting and formatting.
- **Git & GitHub** — version control and portfolio.
- **CUDA** — GPU programming and optimization in later phases.

## 📚 Core Learning Resources

The curriculum will integrate selected books and courses into the corresponding learning phases.

Some planned resources:

- [MIT OpenCourseWare — Linear Algebra](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/)
- [Grokking Machine Learning, 2nd Edition](https://www.manning.com/books/grokking-machine-learning-second-edition)
- [Deep Learning with PyTorch, 2nd Edition](https://www.manning.com/books/deep-learning-with-pytorch-second-edition)
- [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch)
- [Grokking Parallel Programming](https://www.manning.com/books/grokking-parallel-programming)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [arXiv](https://arxiv.org/)
- [Google Scholar](https://scholar.google.com/)

Additional resources and reading assignments will be documented in the `resources/` directory.

## 🚀 Final Outcome

The intended outcome is a public engineering and research portfolio containing:

- Mathematical implementations and exercises.
- Classical ML algorithms implemented from scratch.
- Neural networks and deep learning projects.
- A Transformer implementation.
- A small language model trained or fine-tuned experimentally.
- Selected research paper reproductions.
- GPU and ML performance experiments.
- An independent research project with documented results.

This repository is a work in progress. The roadmap represents the intended learning path; implementation, experiments, and progress will be added incrementally.

---

**Learn the theory. Implement the algorithms. Run the experiments. Understand the research.**
