# Evaluation Rubric

This document defines the evaluation framework for the AI Research Engineer Academy.

Its purpose is to ensure that progress reflects demonstrated technical competence rather than the number of completed lessons, watched lectures, or written lines of code.

The evaluation system measures five dimensions:

1. Theoretical understanding.
2. Mathematical reasoning.
3. Implementation quality.
4. Experimental methodology.
5. Technical communication.

The framework applies to weekly assignments, projects, paper reproductions, and phase completion.

---

# 1. Evaluation Philosophy

The Academy uses evidence-based assessment.

A task is not complete simply because:

- A lecture was watched.
- A book chapter was read.
- Code was copied from a tutorial.
- A model successfully ran once.
- An AI assistant generated an implementation.

Completion requires evidence that the learner understands and can apply the underlying concepts.

## Core principles

- Evaluate understanding, not activity.
- Evaluate independent implementation, not copy-paste ability.
- Evaluate mathematical reasoning, not formula memorization.
- Evaluate experiments, not just successful outputs.
- Evaluate reproducibility, not just reported metrics.
- Reward clear explanations and honest limitations.

The evaluation should identify knowledge gaps early, before they become obstacles in later phases.

---

# 2. Assessment Dimensions

Every reviewed week receives a score across five dimensions.

| Dimension       |         Weight | Main focus                          |
| --------------- | -------------: | ----------------------------------- |
| Theory          |            20% | Conceptual understanding            |
| Mathematics     |            20% | Mathematical reasoning              |
| Implementation  |            25% | Correctness and engineering quality |
| Experiments     |            20% | Experimental design and analysis    |
| Communication   |            15% | Documentation and explanations      |
| **Total** | **100%** |                                     |

Each dimension is scored from 1 to 5.

## 2.1 Theory — 20%

Evaluate whether the learner understands the concepts rather than merely recognizing terminology.

| Score | Criteria                                                                                 |
| ----: | ---------------------------------------------------------------------------------------- |
|     1 | Cannot explain the main concepts.                                                        |
|     2 | Understands definitions but struggles to explain relationships.                          |
|     3 | Explains core concepts and gives basic examples.                                         |
|     4 | Explains mechanisms, assumptions, and trade-offs.                                        |
|     5 | Connects concepts, identifies limitations, and applies knowledge to unfamiliar problems. |

Evidence examples:

- Explanation written without copying source material.
- Oral or written knowledge check.
- Comparison of alternative approaches.
- Correct interpretation of a technical paper.

## 2.2 Mathematics — 20%

Evaluate the ability to understand and use mathematical formulations.

| Score | Criteria                                                                                             |
| ----: | ---------------------------------------------------------------------------------------------------- |
|     1 | Cannot interpret relevant mathematical notation.                                                     |
|     2 | Recognizes formulas but cannot explain their components.                                             |
|     3 | Solves basic problems and explains the main equations.                                               |
|     4 | Derives important equations and applies them correctly.                                              |
|     5 | Independently derives results, understands assumptions, and reasons about mathematical consequences. |

Evidence examples:

- Handwritten or typed derivations.
- Numerical examples.
- Mathematical proofs where appropriate.
- Correct translation of equations into code.

Not every weekly topic requires a formal proof. The expected mathematical depth must match the curriculum.

## 2.3 Implementation — 25%

Evaluate correctness, software engineering quality, and independence.

| Score | Criteria                                                                                                                         |
| ----: | -------------------------------------------------------------------------------------------------------------------------------- |
|     1 | Implementation is incomplete or fundamentally incorrect.                                                                         |
|     2 | Implementation works only for limited examples or depends heavily on copied code.                                                |
|     3 | Correct implementation with basic tests and understandable structure.                                                            |
|     4 | Robust implementation, meaningful edge-case tests, and clear design decisions.                                                   |
|     5 | Independent implementation, strong validation, appropriate abstractions, and thoughtful handling of performance and limitations. |

Evidence examples:

- Source code.
- Automated tests.
- Test output.
- Complexity analysis.
- Comparison with a trusted reference implementation.

## 2.4 Experiments — 20%

Evaluate the ability to formulate questions and investigate behavior scientifically.

| Score | Criteria                                                                                                                        |
| ----: | ------------------------------------------------------------------------------------------------------------------------------- |
|     1 | No meaningful experiment or interpretation.                                                                                     |
|     2 | Runs experiments but does not control variables or explain results.                                                             |
|     3 | Defines a baseline, records results, and provides basic interpretation.                                                         |
|     4 | Uses controlled comparisons, appropriate metrics, and reproducible configurations.                                              |
|     5 | Demonstrates rigorous experimental reasoning, analyzes uncertainty and limitations, and draws appropriately scoped conclusions. |

Evidence examples:

- Experiment configuration.
- Baseline results.
- Metrics and plots.
- Reproducible execution instructions.
- Interpretation and limitations.

A failed experiment can receive a high score if the methodology is sound and the results are analyzed correctly.

## 2.5 Communication — 15%

Evaluate whether the learner can communicate technical ideas clearly.

| Score | Criteria                                                             |
| ----: | -------------------------------------------------------------------- |
|     1 | Missing or unclear explanation.                                      |
|     2 | Basic notes with substantial gaps.                                   |
|     3 | Clear explanation of implementation and results.                     |
|     4 | Structured technical documentation with justified decisions.         |
|     5 | Precise, reproducible, professional-quality technical communication. |

Evidence examples:

- Weekly notes.
- Mathematical explanations.
- Experiment reports.
- Architecture diagrams.
- Research paper summaries.

---

# 3. Score Calculation

Each dimension receives a score from 1 to 5.

The weighted score is:

$$
S = \sum_{i=1}^{5} w_i \cdot \frac{s_i}{5}
$$

Where:

- $S$ is the final percentage.
- $w_i$ is the dimension weight expressed as a percentage.
- $s_i$ is the score from 1 to 5.

Example:

| Dimension       |         Weight | Score | Weighted result |
| --------------- | -------------: | ----: | --------------: |
| Theory          |            20% |     4 |              16 |
| Mathematics     |            20% |     3 |              12 |
| Implementation  |            25% |     5 |              25 |
| Experiments     |            20% |     4 |              16 |
| Communication   |            15% |     4 |              12 |
| **Total** | **100%** |       |   **81%** |

## Score interpretation

|    Score | Assessment        | Action                       |
| -------: | ----------------- | ---------------------------- |
|  85–100 | Strong            | Proceed                      |
|   70–84 | Good              | Proceed with documented gaps |
|   60–69 | Needs improvement | Review weak areas            |
| Below 60 | Insufficient      | Repeat essential material    |

The score is an indicator, not an automatic substitute for acceptance criteria.

---

# 4. Critical Competency Gates

A high overall score must not hide a critical weakness.

The following minimum conditions apply:

| Dimension      |       Minimum score to proceed normally |
| -------------- | --------------------------------------: |
| Theory         |                                       3 |
| Mathematics    | 3, when mathematics is a core objective |
| Implementation |                                       3 |
| Experiments    |       2, when an experiment is required |
| Communication  |                                       2 |

If a critical dimension falls below its minimum:

- The week cannot be marked as fully completed.
- The gap must be documented.
- A targeted revision task must be assigned.
- The affected competency must be reassessed.

For weeks where a dimension is genuinely not applicable, mark it as `N/A` and redistribute its weight proportionally across the applicable dimensions. Do not award automatic points for work that was not required.

---

# 5. Weekly Acceptance Criteria

Every week must have explicit acceptance criteria in `CURRICULUM.md` or its weekly README.

A typical week should demonstrate:

## Theory

- [ ] Main concepts explained independently.
- [ ] Important assumptions identified.
- [ ] At least one practical application understood.

## Mathematics

- [ ] Required mathematical notation understood.
- [ ] Relevant derivations or calculations completed.
- [ ] At least one numerical example solved.

## Implementation

- [ ] Required implementation completed.
- [ ] Tests cover normal and relevant edge cases.
- [ ] Correctness verified.
- [ ] Complexity discussed where relevant.

## Experiments

- [ ] Experiment completed when required.
- [ ] Baseline established.
- [ ] Results recorded.
- [ ] Conclusions supported by evidence.

## Communication

- [ ] Weekly notes written.
- [ ] Deliverables are discoverable.
- [ ] Remaining questions documented.

Not every category requires an equal amount of work every week. The curriculum determines which evidence is required.

---

# 6. Phase Completion Gates

Each phase has a separate completion review.

A phase is complete only when:

1. All required weeks have been reviewed.
2. Required deliverables exist.
3. Critical competencies meet the minimum level.
4. The phase project or final assignment is complete.
5. Major unresolved knowledge gaps have a remediation plan.

## Phase 1 — Mathematics & Python Foundations

Weeks 1–12.

Required competencies:

- Python fundamentals.
- Vector and matrix operations.
- Linear algebra fundamentals.
- Derivatives and gradients.
- Basic probability and statistics.
- Testing and numerical reasoning.

Completion evidence:

- Implement core vector and matrix operations.
- Solve selected linear algebra problems manually.
- Implement numerical calculations in Python.
- Explain derivatives and gradients.
- Demonstrate basic probability reasoning.
- Maintain a tested and documented codebase.

Gate:

- Theory: at least 3.
- Mathematics: at least 3.
- Implementation: at least 3.

## Phase 2 — Classical Machine Learning

Weeks 13–24.

Required competencies:

- Supervised and unsupervised learning.
- Regression and classification.
- Loss functions and optimization.
- Model evaluation.
- Regularization.
- Feature engineering.
- Validation and data leakage prevention.

Completion evidence:

- Implement selected ML algorithms from scratch.
- Train and evaluate models using scikit-learn.
- Compare baselines.
- Explain metrics and model behavior.
- Complete an end-to-end ML project.

Gate:

- Theory: at least 3.
- Mathematics: at least 3.
- Implementation: at least 3.
- Experiments: at least 3.

## Phase 3 — Deep Learning & PyTorch

Weeks 25–40.

Required competencies:

- Neural network fundamentals.
- Backpropagation.
- Optimization.
- Regularization.
- PyTorch tensors and autograd.
- Training pipelines.
- CNNs and sequence models.

Completion evidence:

- Implement a simple neural network from scratch.
- Train a model using PyTorch.
- Explain backpropagation.
- Investigate training behavior.
- Track and evaluate model performance.

Gate:

- Theory: at least 3.
- Mathematics: at least 3.
- Implementation: at least 3.
- Experiments: at least 3.

## Phase 4 — NLP & Transformers

Weeks 41–56.

Required competencies:

- Tokenization.
- Word embeddings.
- Sequence models.
- Attention.
- Transformer architecture.
- Encoder and decoder models.
- Language model evaluation.

Completion evidence:

- Implement attention.
- Build a simplified Transformer.
- Explain tensor shapes and attention complexity.
- Train or evaluate a small language model.
- Compare model behavior under controlled conditions.

Gate:

- Theory: at least 3.
- Mathematics: at least 3.
- Implementation: at least 3.
- Communication: at least 3.

## Phase 5 — LLM Training & Fine-tuning

Weeks 57–68.

Required competencies:

- LLM architecture.
- Dataset preparation.
- Pretraining.
- Fine-tuning.
- LoRA and QLoRA.
- Instruction tuning.
- Alignment methods.
- Evaluation and limitations.

Completion evidence:

- Prepare a small training dataset.
- Fine-tune a suitable model.
- Compare baseline and fine-tuned behavior.
- Evaluate with appropriate metrics.
- Document compute constraints and limitations.

Gate:

- Theory: at least 3.
- Implementation: at least 3.
- Experiments: at least 3.
- Communication: at least 3.

## Phase 6 — Research Paper Reproduction

Weeks 69–84.

Required competencies:

- Critical paper reading.
- Mathematical reconstruction.
- Experimental methodology.
- Implementation of published methods.
- Comparison with reported results.
- Research communication.

Completion evidence:

- Analyze selected research papers.
- Reconstruct their main technical ideas.
- Implement selected methods.
- Establish baselines.
- Compare experimental results.
- Publish reproduction reports.

At least two substantial reproduction projects should be completed.

Gate:

- Theory: at least 4.
- Mathematics: at least 3.
- Implementation: at least 3.
- Experiments: at least 4.
- Communication: at least 3.

## Phase 7 — ML Systems, GPU & Performance

Weeks 85–96.

Required competencies:

- CPU/GPU architecture.
- GPU memory.
- CUDA fundamentals.
- Profiling.
- Numerical precision.
- Memory optimization.
- Distributed training.
- Inference systems.

Completion evidence:

- Profile a model.
- Identify performance bottlenecks.
- Compare relevant optimization techniques.
- Measure throughput and memory.
- Document trade-offs and hardware constraints.

Gate:

- Theory: at least 3.
- Implementation: at least 4.
- Experiments: at least 4.
- Communication: at least 3.

## Phase 8 — Independent Research & Portfolio

Weeks 97–104.

Required competencies:

- Research question formulation.
- Literature review.
- Hypothesis development.
- Experimental design.
- Baseline selection.
- Ablation studies.
- Technical reporting.

Completion evidence:

- Define a research question.
- Review relevant literature.
- Implement a baseline.
- Test a proposed improvement.
- Perform controlled experiments.
- Analyze results.
- Publish a reproducible research report.

Gate:

- Theory: at least 4.
- Mathematics: at least 3.
- Implementation: at least 4.
- Experiments: at least 4.
- Communication: at least 4.

---

# 7. Remediation Process

When a competency does not meet the required level, use a targeted remediation process.

## Step 1 — Identify the gap

Describe the missing knowledge precisely.

Bad example:

> I don't understand linear algebra.

Better example:

> I can multiply matrices but cannot explain how matrix rank relates to the dimension of the column space.

## Step 2 — Identify the cause

Possible causes:

- Missing prerequisite knowledge.
- Weak mathematical understanding.
- Insufficient implementation practice.
- Incorrect assumptions.
- Lack of experimental reasoning.
- Poor time allocation.

## Step 3 — Assign a focused task

Examples:

- Solve three matrix rank exercises.
- Implement Gaussian elimination.
- Derive the gradient of a loss function.
- Write tests for edge cases.
- Reproduce a baseline experiment.

## Step 4 — Reassess

Use a new problem or example.

Do not simply repeat the original task from memory.

## Step 5 — Update progress

Record:

- Original gap.
- Remediation activity.
- New evidence.
- Updated score.
- Remaining limitations.

A remediation does not require repeating an entire week if the gap is narrow and can be independently verified.

---

# 8. Project Evaluation

Larger projects require additional evaluation beyond weekly scores.

| Category                          |         Weight |
| --------------------------------- | -------------: |
| Problem definition                |            10% |
| Technical correctness             |            25% |
| Mathematical understanding        |            15% |
| Experimental methodology          |            20% |
| Code quality and tests            |            15% |
| Documentation and reproducibility |            15% |
| **Total**                   | **100%** |

## Project quality levels

**Level 1 — Tutorial implementation**

- Follows an existing tutorial.
- Limited independent reasoning.
- Basic functionality.

**Level 2 — Independent implementation**

- Reimplements the core method.
- Includes tests.
- Explains important design decisions.

**Level 3 — Experimental project**

- Includes baselines.
- Investigates parameters.
- Reports measurable results.
- Documents limitations.

**Level 4 — Portfolio-ready project**

- Clear problem statement.
- Reproducible implementation.
- Strong testing.
- Meaningful experiments.
- Professional documentation.
- Independent technical decisions.

**Level 5 — Research-quality contribution**

- Well-defined research question.
- Relevant literature review.
- Reproducible methodology.
- Meaningful investigation.
- Evidence-supported conclusions.
- Clearly communicated contribution and limitations.

Not every project needs to reach Level 5.

---

# 9. Research Reproduction Evaluation

Paper reproduction requires special care.

A reproduction report must distinguish:

- Conceptual understanding.
- Architectural implementation.
- Training procedure reproduction.
- Evaluation reproduction.
- Numerical result reproduction.

These are different achievements.

## Reproduction levels

| Level | Description                                                 |
| ----- | ----------------------------------------------------------- |
| R0    | Paper read and summarized                                   |
| R1    | Main ideas and mathematics understood                       |
| R2    | Core architecture implemented                               |
| R3    | Method trained or executed successfully                     |
| R4    | Evaluation protocol reproduced                              |
| R5    | Main reported results reproduced within justified tolerance |

A reproduction can be valuable even if the exact original results cannot be matched due to hardware, dataset access, or compute limitations.

In that case, document the deviation and explain what was actually verified.

Never label an R2 or R3 implementation as a full reproduction.

---

# 10. Evidence Requirements

Scores must be supported by artifacts or direct assessment.

Acceptable evidence includes:

- Source code.
- Automated test results.
- Mathematical derivations.
- Experiment configurations.
- Experiment reports.
- Model evaluation results.
- Technical notes.
- Independent explanations.
- Reproducible execution instructions.

Weak evidence includes:

- Statements such as "I understand it."
- Screenshots without context.
- Code without tests or explanation.
- Copied benchmark numbers.
- Unverified AI-generated answers.

A reviewer should be able to inspect the evidence and understand why a score was assigned.

---

# 11. Assessment Record Template

Use this template for every weekly or project review.

```markdown
# Assessment Record

## Identification

- Week / Project:
- Date:
- Reviewer:
- Status:

## Evidence

- Source code:
- Tests:
- Mathematical notes:
- Experiment report:
- Documentation:

## Scores

| Dimension | Weight | Score (1–5) | Comments |
|---|---:|---:|---|
| Theory | 20% | | |
| Mathematics | 20% | | |
| Implementation | 25% | | |
| Experiments | 20% | | |
| Communication | 15% | | |

## Overall Result

- Weighted score:
- Critical gates passed:
- Decision:

## Strengths

-

## Knowledge Gaps

-

## Required Remediation

-

## Next Assessment

- Target:
- Acceptance criteria:
```

---

# 12. Review Integrity

Assessment should be honest and constructive.

Follow these rules:

1. Do not inflate scores to maintain momentum.
2. Do not penalize justified failed experiments.
3. Distinguish missing evidence from incorrect understanding.
4. Distinguish implementation bugs from conceptual mistakes.
5. Reassess weak areas using new problems.
6. Record external assistance when it materially affects the work.
7. Do not claim independent mastery based solely on AI-generated explanations.
8. Allow targeted remediation instead of unnecessary repetition.

The evaluation system exists to improve learning, not to create artificial pressure.

---

# 13. Final Evaluation Principle

The Academy's purpose is to develop an engineer who can independently:

- Understand research papers.
- Reconstruct mathematical formulations.
- Implement machine learning methods.
- Design meaningful experiments.
- Evaluate results critically.
- Optimize ML systems.
- Communicate technical findings.

**Progress is demonstrated through evidence. Completion is earned through understanding and independent application.**
