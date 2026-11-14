# Research Workflow

This document defines the research workflow used throughout the AI Research Engineer Academy.

The goal is to develop the ability to independently investigate machine learning problems, understand published research, reproduce experimental results, and eventually propose and evaluate original ideas.

Research engineering requires more than implementing models. It requires disciplined reasoning, reliable experimentation, careful measurement, and clear communication.

This workflow applies to:

- Research paper analysis.
- Paper reproduction.
- ML experiments.
- Model architecture investigations.
- Performance optimization.
- Independent research projects.

---

# 1. Research Lifecycle

Every research task follows a structured lifecycle.

```text
Problem Identification
        |
        v
Literature Review
        |
        v
Problem Formulation
        |
        v
Hypothesis Development
        |
        v
Experimental Design
        |
        v
Baseline Implementation
        |
        v
Proposed Method
        |
        v
Controlled Experiments
        |
        v
Evaluation and Analysis
        |
        v
Reproducibility Checks
        |
        v
Research Report
        |
        v
Next Research Question
```

Research is iterative. New results may require revisiting earlier assumptions, refining the problem, or changing the experimental design.

Do not treat this workflow as a rigid waterfall process.

---

# 2. Step 1 — Problem Identification

A useful research project begins with a specific problem.

Avoid starting with a vague objective such as:

- Build a better LLM.
- Improve model performance.
- Make inference faster.
- Investigate transformers.

Instead, narrow the problem.

Examples:

- How does context length affect inference memory consumption?
- How does LoRA rank influence model quality and training cost?
- Does a particular positional encoding improve long-context generalization?
- How does batch size affect inference throughput under a fixed GPU memory budget?
- Can a simpler attention implementation achieve comparable results on a constrained workload?

## Problem statement template

```markdown
# Problem Statement

## Context

What is the technical area?

## Problem

What specific issue are we investigating?

## Motivation

Why does this problem matter?

## Scope

What will and will not be investigated?

## Expected Contribution

What new understanding or evidence could this work provide?

## Constraints

- Hardware:
- Compute budget:
- Dataset:
- Time:
- Dependencies:
```

A good research problem is specific enough to investigate and important enough to justify the effort.

---

# 3. Step 2 — Literature Review

Before proposing a solution, understand existing work.

The objective is to identify:

- What is already known?
- Which methods have been proposed?
- What assumptions do they make?
- What results have been reported?
- Which limitations remain?
- Where might further investigation be useful?

## 3.1 Where to search

Use several complementary sources.

| Resource                     | Purpose                                  |
| ---------------------------- | ---------------------------------------- |
| arXiv                        | Recent preprints                         |
| Google Scholar               | Academic literature discovery            |
| Semantic Scholar             | Paper discovery and citation exploration |
| Papers with Code             | Research implementations and benchmarks  |
| Conference proceedings       | Peer-reviewed research                   |
| Official GitHub repositories | Reference implementations                |
| Research lab publications    | Work from research groups                |

Useful links:

- https://arxiv.org/
- https://scholar.google.com/
- https://www.semanticscholar.org/
- https://paperswithcode.com/
- https://openreview.net/
- https://proceedings.neurips.cc/

A preprint is not automatically peer-reviewed. Record the publication status and version of important papers.

## 3.2 Search strategy

Start with broad keywords.

Example:

```text
"long context language model memory efficiency"
```

Then refine:

```text
"KV cache memory optimization transformer inference"
```

Use:

- Key terminology.
- Author names.
- Related paper titles.
- Citation networks.
- Recent survey papers.

Do not rely exclusively on search ranking.

## 3.3 Build a paper collection

Organize papers by topic.

Example:

```text
papers/
├── attention/
├── transformers/
├── language-models/
├── efficient-training/
├── inference/
└── alignment/
```

Keep a research bibliography with:

- Title.
- Authors.
- Year.
- Venue.
- DOI or arXiv identifier.
- URL.
- Publication status.
- Relevance to the research question.

## 3.4 Literature review matrix

Compare relevant papers systematically.

| Paper   | Problem   | Method   | Dataset   | Main Result | Limitation   |
| ------- | --------- | -------- | --------- | ----------- | ------------ |
| Paper A | Problem A | Method A | Dataset A | Result A    | Limitation A |
| Paper B | Problem B | Method B | Dataset B | Result B    | Limitation B |

Do not invent missing details. Mark unavailable information explicitly.

## 3.5 Identify a research gap

A research gap does not have to mean that nobody has ever investigated the topic.

It may be:

- An underexplored configuration.
- A limitation in an existing evaluation.
- A trade-off that has not been sufficiently measured.
- A discrepancy between reported results.
- A method that behaves differently under constrained hardware.
- An opportunity to improve reproducibility or evaluation.

For early projects, a carefully designed empirical investigation is a valid learning outcome even if it does not produce a novel algorithm.

---

# 4. Step 3 — Problem Formulation

Translate the problem into a measurable question.

A good research question should define:

1. The system being investigated.
2. The variable being changed.
3. The outcome being measured.
4. The relevant constraints.
5. The comparison baseline.

Example:

**Broad topic:**

Investigate LoRA efficiency.

**Research question:**

How does LoRA rank affect fine-tuning memory consumption, training time, and validation quality for a fixed model, dataset, and training budget?

This question can be investigated through controlled experiments.

## Research question checklist

- [ ] The problem is specific.
- [ ] The scope is manageable.
- [ ] The variables are identifiable.
- [ ] Outcomes can be measured.
- [ ] A baseline can be established.
- [ ] The experiment fits the available compute budget.

---

# 5. Step 4 — Hypothesis Development

A hypothesis is a testable prediction.

It should connect a proposed explanation with an observable outcome.

Example:

**Research question:**

How does LoRA rank affect model quality and resource consumption?

**Hypothesis:**

Increasing LoRA rank will initially improve adaptation quality, but improvements will eventually diminish while trainable parameter count and memory requirements increase.

This is a prediction, not a guaranteed result.

## Hypothesis template

```markdown
# Hypothesis

## Research Question

What are we investigating?

## Hypothesis

What do we expect to happen?

## Reasoning

Why do we expect this result?

## Independent Variables

What will we change?

## Dependent Variables

What will we measure?

## Controlled Variables

What must remain constant?

## Falsification Criteria

What result would contradict our hypothesis?
```

A good hypothesis should be falsifiable.

If no possible result could contradict it, it is probably too vague.

---

# 6. Step 5 — Experimental Design

A research experiment must be designed before results are collected.

## 6.1 Define variables

| Variable Type | Meaning                | Example                 |
| ------------- | ---------------------- | ----------------------- |
| Independent   | Variable being changed | LoRA rank               |
| Dependent     | Measured outcome       | Validation loss         |
| Controlled    | Kept constant          | Dataset and base model  |
| Confounding   | Uncontrolled influence | Different hardware load |

Control variables wherever possible.

If multiple variables change simultaneously, it becomes difficult to determine what caused an observed difference.

## 6.2 Select evaluation metrics

Choose metrics based on the research question.

Examples:

| Research Area         | Possible Metrics                                   |
| --------------------- | -------------------------------------------------- |
| Language modeling     | Perplexity, cross-entropy loss                     |
| Classification        | Accuracy, precision, recall, F1                    |
| Generation            | Task-specific quality metrics and human evaluation |
| Training performance  | Steps per second, time to convergence              |
| Inference performance | Tokens per second, latency                         |
| Memory efficiency     | Peak allocated and reserved memory                 |
| Model compression     | Model size, quality degradation                    |
| Optimization          | Convergence behavior and stability                 |

Avoid selecting metrics only because they produce favorable results.

## 6.3 Define a baseline

The baseline is the reference against which the proposed method is evaluated.

A baseline should be:

- Relevant.
- Correctly implemented.
- Documented.
- Reproducible.
- Evaluated using the same methodology.

Without a baseline, claims of improvement are difficult to interpret.

## 6.4 Estimate compute requirements

Before running expensive experiments, estimate:

- Model size.
- Dataset size.
- Sequence length.
- Batch size.
- Number of training steps.
- Memory requirements.
- Expected runtime.
- Storage requirements.

Start with a small-scale pilot experiment.

Use the smallest configuration that can test the core hypothesis.

---

# 7. Step 6 — Baseline Implementation

Implement the baseline before the proposed method.

This validates the experimental environment and provides a reference result.

## Baseline checklist

- [ ] Architecture is documented.
- [ ] Dataset preprocessing is documented.
- [ ] Training configuration is saved.
- [ ] Random seed is recorded where applicable.
- [ ] Evaluation procedure is defined.
- [ ] Baseline metrics are recorded.
- [ ] Implementation is tested.
- [ ] Execution instructions are available.

For paper reproduction, distinguish between:

- Official reference implementation.
- Independent implementation.
- Simplified educational implementation.

These are not equivalent.

Document which one is being used.

---

# 8. Step 7 — Implement the Proposed Method

Only after establishing the baseline should the proposed change be implemented.

Keep the change isolated.

For example:

If investigating positional encodings:

- Keep the model architecture fixed.
- Keep the dataset fixed.
- Keep the training budget fixed.
- Change the positional encoding method.
- Evaluate under the same protocol.

Avoid introducing unrelated changes during the same experiment.

## Implementation principles

- Keep experimental code understandable.
- Separate model configuration from implementation.
- Save training and evaluation configurations.
- Use version control.
- Test important tensor shapes.
- Validate numerical behavior.
- Document deviations from the reference method.

For complex systems, isolate individual components to make debugging easier.

---

# 9. Step 8 — Run Controlled Experiments

A single successful run is rarely sufficient to establish a reliable conclusion.

For important comparisons:

- Use consistent evaluation conditions.
- Repeat runs when randomness materially affects results.
- Report the number of runs.
- Record variability.
- Avoid changing several factors without a reason.
- Preserve failed and unexpected results.

## Example experiment matrix

Research question:

How does LoRA rank affect fine-tuning?

| Experiment | LoRA Rank | Dataset | Training Budget |
| ---------- | --------: | ------- | --------------- |
| Baseline   |        — | Fixed   | Fixed           |
| E1         |         4 | Fixed   | Fixed           |
| E2         |         8 | Fixed   | Fixed           |
| E3         |        16 | Fixed   | Fixed           |
| E4         |        32 | Fixed   | Fixed           |

Possible measurements:

- Trainable parameters.
- Peak GPU memory.
- Training time.
- Validation loss.
- Task-specific evaluation score.

The experiment should also record the base model, target modules, optimizer, learning rate, precision, batch size, and sequence length.

---

# 10. Step 9 — Ablation Studies

An ablation study investigates the contribution of individual components.

It helps answer:

- Which component provides the improvement?
- Does every component matter?
- Is the full system necessary?
- Are two components interacting?

Example:

Suppose a model contains:

- Attention modification A.
- Positional encoding B.
- Regularization C.

Possible ablations:

| Experiment | A   | B   | C   |
| ---------- | --- | --- | --- |
| Full model | Yes | Yes | Yes |
| Remove A   | No  | Yes | Yes |
| Remove B   | Yes | No  | Yes |
| Remove C   | Yes | Yes | No  |
| Baseline   | No  | No  | No  |

Ablations are useful when the research question concerns component contributions.

They are not mandatory for every small educational exercise.

---

# 11. Step 10 — Evaluation and Analysis

Do not stop after collecting metrics.

Interpret the results.

Ask:

1. Did the results support the hypothesis?
2. How large was the observed difference?
3. Is the difference practically meaningful?
4. Could randomness explain the difference?
5. Were the experiments sufficiently controlled?
6. Were there unexpected effects?
7. What limitations remain?

## Statistical considerations

For experiments with meaningful variability:

- Report sample size.
- Report mean and standard deviation where appropriate.
- Use confidence intervals when justified.
- Consider statistical tests only when their assumptions are satisfied.
- Distinguish statistical significance from practical significance.

Do not overstate conclusions from a small number of runs.

## Example interpretation

Weak conclusion:

> Rank 16 is better because it achieved a higher score.

Stronger conclusion:

> Under the tested configuration, rank 16 achieved a higher validation score than rank 8, with increased memory consumption. Additional runs are needed to determine whether the difference is stable.

Good research communication makes uncertainty explicit.

---

# 12. Step 11 — Reproducibility

Reproducibility is a core research engineering requirement.

Another engineer should be able to understand and rerun the experiment using the documented configuration and available resources.

## Record the environment

At minimum:

- Python version.
- Library versions.
- Operating system.
- CPU.
- GPU.
- CUDA version, where applicable.
- Model checkpoint and version.
- Dataset version.
- Random seeds.
- Configuration files.

## Save experiment artifacts

```text
experiments/
└── experiment-name/
    ├── README.md
    ├── config.yaml
    ├── environment.txt
    ├── run.py
    ├── evaluate.py
    ├── results/
    │   ├── metrics.json
    │   └── plots/
    └── report.md
```

Do not commit credentials, private datasets, or large model weights to Git.

Use appropriate external artifact storage when needed.

## Reproducibility checklist

- [ ] Setup instructions are documented.
- [ ] Dependencies are specified.
- [ ] Configuration is saved.
- [ ] Dataset source and version are recorded.
- [ ] Model version is recorded.
- [ ] Evaluation procedure is documented.
- [ ] Results are preserved.
- [ ] Known limitations are stated.

Reproducibility does not always mean obtaining exactly identical numbers. Hardware, numerical precision, nondeterministic operations, and software versions may affect results.

The goal is to make differences explainable.

---

# 13. Step 12 — Research Report

Every substantial research project should produce a technical report.

Use the following structure:

```markdown
# Research Report

## Abstract

A concise summary of the problem, method, and results.

## 1. Introduction

- Problem statement
- Motivation
- Research question
- Expected contribution

## 2. Related Work

- Relevant papers
- Existing methods
- Research gap

## 3. Methodology

- Hypothesis
- Proposed method
- Mathematical formulation
- Experimental design

## 4. Implementation

- Architecture
- Dataset
- Training configuration
- Environment

## 5. Experiments

- Baselines
- Experimental conditions
- Evaluation metrics
- Ablation studies

## 6. Results

- Tables
- Plots
- Measurements
- Statistical summaries where appropriate

## 7. Discussion

- Interpretation
- Comparison with prior work
- Unexpected findings

## 8. Limitations

- Compute limitations
- Dataset limitations
- Methodological limitations
- Threats to validity

## 9. Conclusion

- What was learned?
- Was the hypothesis supported?
- What should be investigated next?

## References

Bibliographic references and source links.
```

Write the report so that someone who has not followed the experiment can understand what was done and why.

---

# 14. Threats to Validity

Research results can be misleading even when the implementation is correct.

Always consider possible threats to validity.

## Internal validity

Could something other than the independent variable explain the result?

Examples:

- Different training budgets.
- Different random seeds.
- Different preprocessing.
- Different hardware conditions.

## External validity

Do the results generalize beyond the tested environment?

Examples:

- A small dataset.
- One model architecture.
- One GPU.
- One specific sequence length.

## Construct validity

Do the chosen metrics actually measure the intended concept?

Example:

Higher benchmark accuracy does not necessarily mean better real-world reasoning.

## Reproducibility validity

Can another person reproduce the experiment with the available instructions and artifacts?

A good report identifies these limitations rather than ignoring them.

---

# 15. Research Project Directory

Use a consistent structure for independent research.

```text
projects/
└── independent-research-project/
    ├── README.md
    ├── research-question.md
    ├── literature-review.md
    ├── hypothesis.md
    ├── methodology.md
    ├── configs/
    ├── src/
    ├── tests/
    ├── experiments/
    ├── results/
    ├── reports/
    └── references.bib
```

Keep the project focused.

Do not create unnecessary abstractions before the research question and experimental requirements are understood.

---

# 16. AI-Assisted Research

AI assistants can help with literature discovery, explanations, code review, and experiment design.

However, AI-generated content must be independently verified.

## Appropriate uses

- Explaining difficult mathematical concepts.
- Summarizing a paper as an initial orientation.
- Identifying unfamiliar terminology.
- Reviewing an experimental design.
- Generating test cases.
- Investigating implementation bugs.
- Comparing alternative approaches.

## Verification requirements

- Verify paper metadata against the original source.
- Check equations against the paper.
- Inspect official implementations when available.
- Run generated code.
- Validate tensor shapes.
- Reproduce important calculations.
- Check all benchmark claims against actual evidence.

Do not cite a paper that has not been inspected.

Do not claim that an experiment was run when only a proposed configuration exists.

AI assistance should improve research productivity without weakening independent understanding.

---

# 17. From Reproduction to Original Research

Paper reproduction is a foundation for original research.

A useful progression:

## Level 1 — Understand

Explain the paper's central ideas and assumptions.

## Level 2 — Implement

Reconstruct the important components.

## Level 3 — Reproduce

Run the method under a documented evaluation protocol.

## Level 4 — Investigate

Change one controlled variable and study its effect.

## Level 5 — Extend

Propose a justified modification and evaluate it.

## Level 6 — Research independently

Formulate a new question, review relevant literature, design experiments, and communicate the findings.

Not every extension will produce a novel scientific contribution.

The ability to conduct a rigorous investigation is valuable even when the result is negative.

---

# 18. Final Research Principles

Throughout the Academy:

1. Start with a precise question.
2. Understand existing work.
3. Formulate a falsifiable hypothesis.
4. Design the experiment before running it.
5. Establish a reliable baseline.
6. Change variables deliberately.
7. Measure the right outcomes.
8. Analyze uncertainty and limitations.
9. Preserve reproducibility artifacts.
10. Communicate conclusions honestly.

**Research is not just building something that works. It is developing evidence for why it works, when it works, and where it fails.**
