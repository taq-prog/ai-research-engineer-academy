# AI Research Engineer Academy — Roadmap

A 104-week learning roadmap designed to develop the mathematical, engineering, and research skills required for AI / ML Research Engineering.

**Target duration:** 18–24 months
**Weekly commitment:** 5–7 hours
**Primary language:** Python
**Primary deep learning framework:** PyTorch
**Learning approach:** Theory → Mathematics → Implementation → Experiments → Evaluation

---

## 1. Roadmap at a Glance

| Phase                               |   Weeks | Duration | Main Outcome                                 |
| ----------------------------------- | ------: | -------: | -------------------------------------------- |
| 1. Mathematics & Python Foundations |   1–12 | 12 weeks | Mathematical and programming foundations     |
| 2. Classical Machine Learning       |  13–24 | 12 weeks | Understanding and implementing ML algorithms |
| 3. Deep Learning & PyTorch          |  25–40 | 16 weeks | Building and training neural networks        |
| 4. NLP & Transformers               |  41–56 | 16 weeks | Understanding Transformer architectures      |
| 5. LLM Training & Fine-tuning       |  57–68 | 12 weeks | Building and adapting small language models  |
| 6. Research Paper Reproduction      |  69–84 | 16 weeks | Reproducing published research               |
| 7. ML Systems, GPU & Performance    |  85–96 | 12 weeks | Understanding and optimizing ML systems      |
| 8. Independent Research & Portfolio | 97–104 |  8 weeks | Conducting an independent research project   |

The curriculum is sequential. Each phase builds on the knowledge and practical skills developed in previous phases.

---

# 2. Phase 1 — Mathematics & Python Foundations

**Weeks 1–12**

### Objective

Build the mathematical and programming foundations required to understand machine learning algorithms rather than treating them as black boxes.

### Prerequisites

- Basic programming experience.
- Basic algebra.
- No previous ML experience required.

### Topics

- Python fundamentals and scientific computing.
- Linear algebra.
- Calculus and derivatives.
- Probability and statistics.
- Basic algorithmic problem solving.

### Weekly curriculum

| Week | Topics                                                                                                    | Practical Deliverable                                                                                          |
| ---: | --------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
|    1 | Python environment, functions, classes, collections; algebra and functions; vectors and vector operations | Implement a `Vector` class without NumPy; write pytest tests; solve Two Sum using brute force and a hash map |
|    2 | Vector spaces, linear combinations, span, linear independence                                             | Implement vector operations and test linear independence on small examples                                     |
|    3 | Matrices, matrix multiplication, transpose, identity matrix                                               | Implement matrix operations using Python lists and NumPy                                                       |
|    4 | Systems of linear equations, Gaussian elimination, row operations                                         | Implement Gaussian elimination                                                                                 |
|    5 | Rank, basis, dimension, column space and null space                                                       | Explore rank and null space using NumPy                                                                        |
|    6 | Orthogonality, projections, least squares                                                                 | Implement least squares linear regression using linear algebra                                                 |
|    7 | Eigenvalues, eigenvectors, diagonalization                                                                | Compute and visualize eigenvectors and eigenvalues                                                             |
|    8 | Singular Value Decomposition (SVD), low-rank approximation                                                | Implement a simple dimensionality reduction experiment                                                         |
|    9 | Derivatives, partial derivatives, chain rule                                                              | Implement numerical derivatives and compare with analytical derivatives                                        |
|   10 | Gradients, Jacobians, gradient descent                                                                    | Implement gradient descent for a simple optimization problem                                                   |
|   11 | Probability, conditional probability, Bayes' theorem, common distributions                                | Implement probability simulations and visualize distributions                                                  |
|   12 | Expectation, variance, covariance, correlation, statistical foundations                                   | Complete a mathematical foundations mini-project and self-assessment                                           |

### Core resources

- MIT OCW — [Linear Algebra 18.06](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/)
- [Python Documentation](https://docs.python.org/3/)
- [NumPy Documentation](https://numpy.org/doc/)
- Selected chapters from *Grokking Algorithms* for algorithmic refreshers.

### Phase deliverables

- Python development environment.
- Tested vector and matrix implementations.
- Gaussian elimination implementation.
- Least squares implementation.
- Gradient descent implementation.
- Mathematical notes and exercises.

### Completion criteria

You should be able to:

- Work comfortably with vectors and matrices.
- Explain matrix multiplication and linear transformations.
- Understand gradients and derivatives.
- Explain the intuition behind gradient descent.
- Work with basic probability and statistical concepts.
- Implement small mathematical algorithms without relying entirely on libraries.

---

# 3. Phase 2 — Classical Machine Learning

**Weeks 13–24**

### Objective

Understand the foundations of machine learning, including model training, optimization, evaluation, and generalization.

### Prerequisites

- Phase 1 mathematics.
- Basic Python and NumPy.
- Basic probability and statistics.

### Topics

- Supervised and unsupervised learning.
- Regression and classification.
- Loss functions and optimization.
- Model evaluation.
- Regularization.
- Feature engineering.
- Dimensionality reduction.

### Weekly curriculum

| Week | Topics                                                                   | Practical Deliverable                        |
| ---: | ------------------------------------------------------------------------ | -------------------------------------------- |
|   13 | ML workflow, datasets, features, labels, train/validation/test splits    | Build a reproducible ML pipeline             |
|   14 | Linear regression, MSE, normal equation                                  | Implement linear regression from scratch     |
|   15 | Logistic regression, sigmoid, binary cross-entropy                       | Implement binary classification from scratch |
|   16 | Gradient descent, learning rates, convergence, optimization              | Compare gradient descent configurations      |
|   17 | Classification metrics, confusion matrix, precision, recall, F1, ROC-AUC | Build an evaluation module                   |
|   18 | Overfitting, underfitting, bias-variance trade-off, regularization       | Compare L1 and L2 regularization             |
|   19 | Decision trees, entropy, information gain, Gini impurity                 | Implement a basic decision tree              |
|   20 | Random forests, bagging, boosting, ensemble methods                      | Compare tree-based models                    |
|   21 | KNN, Naive Bayes, feature scaling                                        | Implement KNN and Naive Bayes                |
|   22 | Clustering, K-means, unsupervised learning                               | Implement K-means and evaluate clusters      |
|   23 | PCA, dimensionality reduction, cross-validation, hyperparameter tuning   | Build a dimensionality reduction experiment  |
|   24 | End-to-end ML project, model comparison, error analysis                  | Deliver a complete classical ML project      |

### Core resource

- *Grokking Machine Learning, 2nd Edition* — primary reading resource for this phase.

### Phase deliverables

- Linear regression from scratch.
- Logistic regression from scratch.
- Decision tree implementation.
- KNN and Naive Bayes implementations.
- K-means implementation.
- End-to-end ML project with evaluation and documentation.

### Completion criteria

You should be able to:

- Explain the difference between supervised and unsupervised learning.
- Implement basic ML algorithms from scratch.
- Select appropriate loss functions and evaluation metrics.
- Detect overfitting and data leakage.
- Compare models using a reproducible experimental setup.
- Explain why one model performs better than another.

---

# 4. Phase 3 — Deep Learning & PyTorch

**Weeks 25–40**

### Objective

Understand neural networks mathematically and implement, train, debug, and evaluate them using PyTorch.

### Prerequisites

- Linear algebra.
- Derivatives and gradients.
- Gradient descent.
- Classical ML foundations.

### Topics

- Neural networks.
- Backpropagation.
- Optimization algorithms.
- PyTorch fundamentals.
- CNNs.
- RNNs and LSTMs.
- GPU training.

### Weekly curriculum

| Week | Topics                                                      | Practical Deliverable                         |
| ---: | ----------------------------------------------------------- | --------------------------------------------- |
|   25 | Perceptron, neural network architecture, neurons and layers | Implement a perceptron                        |
|   26 | Activation functions, forward propagation                   | Build a small neural network from scratch     |
|   27 | Backpropagation, chain rule, computational graphs           | Implement backpropagation manually            |
|   28 | Loss functions, SGD, batch and mini-batch training          | Build a complete training loop                |
|   29 | Adam, momentum, initialization strategies                   | Compare optimizers and initialization methods |
|   30 | Regularization, dropout, batch normalization, weight decay  | Run controlled regularization experiments     |
|   31 | PyTorch tensors, tensor operations, autograd                | Reimplement a neural network using PyTorch    |
|   32 | `nn.Module`, optimizers, loss functions, training loops   | Build a reusable PyTorch training pipeline    |
|   33 | Dataset, DataLoader, batching, transforms                   | Create a reusable data loading pipeline       |
|   34 | CNN architecture, convolution, pooling, receptive fields    | Train a CNN on a small image dataset          |
|   35 | CNN optimization, augmentation, transfer learning           | Compare training strategies                   |
|   36 | Embeddings, sequence modeling, RNN fundamentals             | Implement a simple RNN                        |
|   37 | LSTM, GRU, vanishing and exploding gradients                | Train an LSTM on a sequence task              |
|   38 | GPU execution, CUDA basics, memory management               | Train and benchmark a model on GPU            |
|   39 | Experiment tracking, reproducibility, checkpoints           | Build an experiment tracking workflow         |
|   40 | Deep learning project and model evaluation                  | Deliver a complete PyTorch project            |

### Core resource

- *Deep Learning with PyTorch, 2nd Edition*.

### Phase deliverables

- Neural network from scratch.
- Manual backpropagation implementation.
- PyTorch training framework.
- CNN image classification project.
- RNN/LSTM sequence modeling project.
- Reproducible GPU training experiment.

### Completion criteria

You should be able to:

- Derive and explain backpropagation.
- Understand the relationship between gradients and parameter updates.
- Build neural networks using PyTorch.
- Debug training instability.
- Understand common optimization and regularization techniques.
- Train and evaluate models on GPU.
- Reproduce an experiment using saved configurations and checkpoints.

---

# 5. Phase 4 — NLP & Transformers

**Weeks 41–56**

### Objective

Understand how modern language models process text and how Transformer architectures work internally.

### Prerequisites

- Neural networks and PyTorch.
- Embeddings.
- Basic probability.
- Linear algebra and matrix operations.

### Topics

- Natural Language Processing.
- Tokenization.
- Language modeling.
- Attention.
- Transformer architecture.
- Encoder and decoder models.
- BERT and GPT.

### Weekly curriculum

| Week | Topics                                                          | Practical Deliverable                       |
| ---: | --------------------------------------------------------------- | ------------------------------------------- |
|   41 | NLP foundations, text preprocessing, normalization              | Build a basic text preprocessing pipeline   |
|   42 | Tokenization, vocabulary, one-hot encoding, TF-IDF              | Implement a simple tokenizer and TF-IDF     |
|   43 | Word2Vec, embeddings, semantic similarity                       | Train or implement a simple embedding model |
|   44 | Language modeling, n-grams, bigram models                       | Implement a bigram language model           |
|   45 | Sequence models, RNN language models, perplexity                | Train a small language model                |
|   46 | Attention mechanism and scaled dot-product attention            | Implement attention from scratch            |
|   47 | Multi-head attention, query, key, value                         | Implement multi-head attention              |
|   48 | Positional encoding and positional embeddings                   | Implement positional information            |
|   49 | Transformer Encoder architecture                                | Build a minimal Transformer Encoder         |
|   50 | Transformer Decoder, causal masking                             | Implement a causal Transformer Decoder      |
|   51 | Encoder-decoder architecture, sequence-to-sequence learning     | Build a small sequence-to-sequence model    |
|   52 | BERT architecture, masked language modeling                     | Study and implement a simplified masked LM  |
|   53 | GPT architecture, autoregressive language modeling              | Build a small GPT-style model               |
|   54 | BPE, subword tokenization, vocabulary design                    | Implement or experiment with BPE            |
|   55 | Transformer complexity, attention memory and computational cost | Benchmark attention implementations         |
|   56 | Transformer project and evaluation                              | Deliver a Transformer from scratch          |

### Core resource

- *Build a Large Language Model (From Scratch)*.

### Important research paper

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)

### Phase deliverables

- Tokenizer implementation.
- Bigram language model.
- Attention implementation.
- Multi-head attention implementation.
- Transformer Encoder and Decoder.
- Small GPT-style language model.

### Completion criteria

You should be able to:

- Explain tokenization and embeddings.
- Derive scaled dot-product attention.
- Explain queries, keys, and values.
- Understand causal masking.
- Explain the difference between encoder and decoder architectures.
- Implement a small Transformer using PyTorch.
- Explain the computational complexity of attention.

---

# 6. Phase 5 — LLM Training & Fine-tuning

**Weeks 57–68**

### Objective

Understand how language models are trained, fine-tuned, evaluated, and adapted to downstream tasks.

### Prerequisites

- Transformer architecture.
- PyTorch training.
- NLP foundations.
- Basic optimization and probability.

### Topics

- LLM architecture.
- Dataset preparation.
- Pretraining.
- Scaling laws.
- Fine-tuning.
- LoRA and QLoRA.
- Instruction tuning.
- Alignment and evaluation.

### Weekly curriculum

| Week | Topics                                                           | Practical Deliverable                               |
| ---: | ---------------------------------------------------------------- | --------------------------------------------------- |
|   57 | LLM architecture, decoder-only models, model configurations      | Analyze and document a small LLM architecture       |
|   58 | Tokenization, entropy, vocabulary, context windows               | Experiment with tokenization and sequence length    |
|   59 | Dataset collection, cleaning, deduplication, data quality        | Build a small text dataset pipeline                 |
|   60 | Pretraining objectives, next-token prediction, training dynamics | Pretrain a small language model                     |
|   61 | Scaling laws, compute, parameters, data and training budgets     | Analyze scaling trade-offs using small experiments  |
|   62 | Fine-tuning, supervised fine-tuning (SFT)                        | Fine-tune a small pretrained model                  |
|   63 | LoRA, low-rank adaptation, parameter-efficient fine-tuning       | Implement or use LoRA                               |
|   64 | QLoRA, quantization, memory constraints                          | Fine-tune a quantized model                         |
|   65 | Instruction tuning, instruction datasets, chat templates         | Build an instruction-tuning pipeline                |
|   66 | Preference data, RLHF concepts, DPO                              | Study and implement a simplified DPO experiment     |
|   67 | LLM evaluation, perplexity, benchmarks, hallucinations           | Build a small evaluation suite                      |
|   68 | End-to-end LLM project                                           | Deliver a fine-tuned language model with evaluation |

### Core resources

- *Build a Large Language Model (From Scratch)*.
- PyTorch documentation.
- Selected technical papers on fine-tuning and model alignment.

### Important research papers

- [GPT-2](https://openai.com/research/better-language-models)
- [Scaling Laws for Neural Language Models](https://arxiv.org/abs/2001.08361)
- [Training Compute-Optimal Large Language Models (Chinchilla)](https://arxiv.org/abs/2203.15556)
- [LoRA](https://arxiv.org/abs/2106.09685)
- [Direct Preference Optimization](https://arxiv.org/abs/2305.18290)

### Phase deliverables

- Small language model pretraining experiment.
- Dataset preparation pipeline.
- Fine-tuning project.
- LoRA experiment.
- Quantization experiment.
- LLM evaluation framework.

### Completion criteria

You should be able to:

- Explain the next-token prediction objective.
- Understand the major stages of LLM training.
- Prepare and validate training datasets.
- Fine-tune a small language model.
- Explain LoRA and QLoRA.
- Understand the basic principles of preference optimization.
- Evaluate model behavior using appropriate metrics and test cases.

---

# 7. Phase 6 — Research Paper Reproduction

**Weeks 69–84**

### Objective

Move from learning existing architectures to understanding, implementing, and reproducing published research.

This phase is a transition from ML engineering toward research engineering.

### Prerequisites

- Strong understanding of neural networks.
- Transformer implementation.
- PyTorch.
- Basic statistical reasoning.
- Ability to run reproducible experiments.

### Research workflow

Every paper reproduction should follow this process:

1. Read the abstract and introduction.
2. Identify the problem and research contribution.
3. Study the methodology and mathematical formulation.
4. Identify datasets, baselines, and evaluation metrics.
5. Implement the central method.
6. Run controlled experiments.
7. Compare results with the paper.
8. Analyze discrepancies.
9. Document limitations and conclusions.

### Weekly curriculum

| Week | Topics                                                               | Practical Deliverable                                    |
| ---: | -------------------------------------------------------------------- | -------------------------------------------------------- |
|   69 | How to read research papers, identify claims and contributions       | Write a structured analysis of a research paper          |
|   70 | Research methodology, baselines, datasets, metrics, reproducibility  | Create a paper reproduction plan                         |
|   71 | Attention Is All You Need: architecture and mathematical formulation | Implement the central Transformer components             |
|   72 | Attention Is All You Need: experiments and comparison                | Reproduce a selected small-scale result                  |
|   73 | BERT: masked language modeling and architecture                      | Implement a simplified BERT-style training objective     |
|   74 | BERT: evaluation and experimental analysis                           | Compare masked language modeling configurations          |
|   75 | GPT-2: autoregressive training and model behavior                    | Reproduce a small-scale GPT-style experiment             |
|   76 | GPT-2: generation, evaluation and limitations                        | Analyze language generation behavior                     |
|   77 | GPT-3: in-context learning and scaling                               | Analyze scaling and in-context learning claims           |
|   78 | Chinchilla: compute-optimal training                                 | Reproduce a simplified scaling analysis                  |
|   79 | LoRA: low-rank adaptation theory                                     | Implement and test a LoRA configuration                  |
|   80 | LoRA: rank, target modules and trade-offs                            | Run controlled LoRA ablations                            |
|   81 | FlashAttention: IO awareness and memory efficiency                   | Study and benchmark attention implementations            |
|   82 | Experimental design, ablation studies, statistical variation         | Run a controlled experiment with multiple configurations |
|   83 | Reproduction report, comparison with published findings              | Write a research-style technical report                  |
|   84 | Research review and presentation                                     | Present findings, limitations and lessons learned        |

### Core papers

- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
- [BERT](https://arxiv.org/abs/1810.04805)
- [GPT-3](https://arxiv.org/abs/2005.14165)
- [Chinchilla](https://arxiv.org/abs/2203.15556)
- [LoRA](https://arxiv.org/abs/2106.09685)
- [FlashAttention](https://arxiv.org/abs/2205.14135)

### Phase deliverables

- Structured research paper notes.
- At least two substantial small-scale reproduction projects.
- One additional paper analysis.
- Reproducible experiment configurations.
- Ablation study.
- Research-style report.

### Completion criteria

You should be able to:

- Read a research paper and identify its central contribution.
- Understand the mathematical formulation of a proposed method.
- Implement its core mechanism.
- Design experiments to test its claims.
- Compare results with published findings.
- Explain discrepancies and limitations.
- Write a clear technical reproduction report.

**Important:** Reproduction does not mean obtaining identical numbers at any cost. Differences in compute, datasets, hardware, and implementation must be documented honestly.

---

# 8. Phase 7 — ML Systems, GPU & Performance

**Weeks 85–96**

### Objective

Understand the systems and hardware foundations behind efficient model training and inference.

### Prerequisites

- PyTorch.
- Neural network training.
- Transformer architecture.
- Basic computer architecture and memory concepts.

### Topics

- CPU and GPU architecture.
- GPU memory hierarchy.
- CUDA programming.
- Numerical precision.
- Model optimization.
- Distributed training.
- Inference systems.

### Weekly curriculum

| Week | Topics                                                               | Practical Deliverable                                              |
| ---: | -------------------------------------------------------------------- | ------------------------------------------------------------------ |
|   85 | CPU vs GPU, parallelism, memory hierarchy                            | Analyze CPU/GPU execution differences                              |
|   86 | GPU architecture, threads, blocks, warps, memory access              | Build a GPU execution model overview                               |
|   87 | CUDA fundamentals, kernels, thread indexing                          | Write a simple CUDA kernel where hardware permits                  |
|   88 | GPU profiling, bottlenecks, kernel performance                       | Profile a small tensor operation                                   |
|   89 | FP32, FP16, BF16, mixed precision                                    | Compare numerical precision and performance                        |
|   90 | Gradient accumulation, activation checkpointing, memory optimization | Reduce training memory usage                                       |
|   91 | Quantization, inference optimization, model compression              | Quantize and benchmark a small model                               |
|   92 | Batching, KV cache, autoregressive inference                         | Implement or analyze KV caching                                    |
|   93 | Distributed training, data parallelism, DDP                          | Run a small distributed training experiment where resources permit |
|   94 | Model serving, inference throughput and latency                      | Build a basic model inference service                              |
|   95 | Monitoring, benchmarking, reliability and cost                       | Create an inference benchmarking report                            |
|   96 | ML systems project                                                   | Deliver a measured and documented optimization project             |

### Core resources

- *Grokking Parallel Programming* — selected topics.
- [CUDA Documentation](https://docs.nvidia.com/cuda/)
- [PyTorch Documentation](https://pytorch.org/docs/stable/)
- [FlashAttention](https://arxiv.org/abs/2205.14135)

### Phase deliverables

- GPU profiling experiments.
- CUDA kernel experiments.
- Mixed precision benchmark.
- Memory optimization experiment.
- Quantization benchmark.
- Inference service.
- Performance report.

### Completion criteria

You should be able to:

- Explain basic GPU architecture.
- Understand memory and compute bottlenecks.
- Profile model training and inference.
- Explain mixed precision and quantization.
- Understand gradient checkpointing and accumulation.
- Explain data parallelism.
- Measure latency, throughput, and memory usage.
- Identify performance bottlenecks using evidence.

**Compute constraint:** Large-scale model training is not required. Start with CPU and small local GPU experiments. Use larger compute only when a research question justifies it.

---

# 9. Phase 8 — Independent Research & Portfolio

**Weeks 97–104**

### Objective

Apply the accumulated knowledge to an independent research question and produce a portfolio-quality engineering and research artifact.

### Prerequisites

- Completed or demonstrated mastery of the core phases.
- Experience implementing and evaluating ML models.
- Experience reading research papers.
- Experience conducting controlled experiments.

### Weekly curriculum

| Week | Topics                                                        | Practical Deliverable                              |
| ---: | ------------------------------------------------------------- | -------------------------------------------------- |
|   97 | Research area selection, literature review, identifying gaps  | Select a research topic and review relevant papers |
|   98 | Problem formulation, hypothesis, expected contribution        | Write a research proposal                          |
|   99 | Baseline selection, datasets, metrics, experiment design      | Implement a baseline                               |
|  100 | Proposed method or modification                               | Implement the proposed change                      |
|  101 | Experiments, ablations, hyperparameter analysis               | Run controlled experiments                         |
|  102 | Evaluation, error analysis, statistical reasoning             | Analyze results and limitations                    |
|  103 | Research writing, reproducibility, documentation              | Write a research-style report                      |
|  104 | Final review, portfolio presentation, next research direction | Publish the project and present findings           |

### Suggested research directions

Choose one topic based on interest, available compute, and the literature review.

Potential topics:

- How sequence length affects Transformer memory consumption and inference latency.
- How positional encoding choices affect language model behavior.
- How vocabulary size affects tokenization efficiency and model performance.
- How LoRA rank affects fine-tuning quality and memory consumption.
- How dataset deduplication affects small language model training.
- How different attention implementations affect performance.
- How training data quality affects model generalization.

### Final deliverables

- Independent research question.
- Literature review.
- Research hypothesis.
- Baseline implementation.
- Proposed modification or experiment.
- Reproducible configurations.
- Evaluation and ablation results.
- Research-style report.
- Public GitHub project.

### Completion criteria

You should be able to:

- Identify a tractable research question.
- Explain why the question matters.
- Formulate a testable hypothesis.
- Design an experiment that can disprove the hypothesis.
- Implement a baseline and proposed method.
- Analyze positive, negative, and inconclusive results.
- Communicate findings clearly.

---

# 10. Weekly Study Structure

The program is designed to fit around a full-time engineering job.

Suggested allocation:

| Activity                    |            Time per Week |
| --------------------------- | -----------------------: |
| Theory and reading          |            1–1.25 hours |
| Mathematics                 |             0.75–1 hour |
| Implementation              |         1.75–2.25 hours |
| Experiments and evaluation  |                0.75 hour |
| Notes and documentation     |                0.25 hour |
| MAANG interview preparation |                   1 hour |
| **Total**             | **5.5–6.5 hours** |

The allocation is flexible. Some weeks will require more implementation, while others will focus on mathematics or reading.

Do not add every optional resource to the schedule. The core book or course for the current phase should remain the primary learning resource.

---

# 11. Assessment and Phase Gates

Each week is evaluated across five dimensions.

| Dimension                           | Weight |
| ----------------------------------- | -----: |
| Theory and conceptual understanding |    20% |
| Mathematics                         |    20% |
| Implementation                      |    25% |
| Experiments and evaluation          |    20% |
| Technical communication             |    15% |

Each dimension receives a score from 1 to 5.

### Overall score

|    Score | Interpretation                               |
| -------: | -------------------------------------------- |
|  85–100 | Strong understanding; proceed                |
|   70–84 | Good progress; proceed while addressing gaps |
|   60–69 | Review weak areas before moving forward      |
| Below 60 | Repeat the essential material                |

A high implementation score alone is not enough to pass a phase. The ability to explain the underlying mathematics and reasoning is equally important.

### Phase gate requirements

Before moving to the next phase:

- Complete the core practical deliverables.
- Pass the conceptual review.
- Demonstrate the required mathematical understanding.
- Run and document at least one experiment.
- Explain the main limitations of the implementation.

---

# 12. Research Engineering Principles

Throughout the curriculum, follow these principles:

1. **Understand before using abstractions.** Learn what a library does before depending on it.
2. **Implement core mechanisms.** Rebuild important algorithms to develop first-principles understanding.
3. **Keep experiments reproducible.** Save configurations, seeds, metrics, and environment information.
4. **Use meaningful baselines.** An improvement is meaningful only when compared against a relevant baseline.
5. **Change one major variable at a time.** Avoid experiments where multiple changes make the result impossible to interpret.
6. **Document failures.** Negative results are useful evidence.
7. **Be honest about conclusions.** Do not claim more than the experiments demonstrate.
8. **Build public evidence of skills.** Code, tests, reports, and reproducible experiments matter more than a list of completed courses.

---

# 13. Career Alignment

This roadmap targets the intersection of software engineering, machine learning, and research.

The intended skill profile:

| Area                 | Target Capability                                                                 |
| -------------------- | --------------------------------------------------------------------------------- |
| Software engineering | Strong engineering practices, testing, architecture and maintainability           |
| Python               | Confident scientific and ML programming                                           |
| Mathematics          | Practical understanding of linear algebra, calculus, probability and optimization |
| Machine learning     | Ability to implement, train and evaluate models                                   |
| Deep learning        | Ability to build and debug neural networks                                        |
| LLMs                 | Understanding of Transformer architecture, training and fine-tuning               |
| Research             | Ability to read, reproduce and critically evaluate papers                         |
| ML systems           | Understanding of GPU execution, performance and inference                         |
| Communication        | Ability to explain technical decisions and research findings                      |

The goal is to combine existing senior-level software engineering experience with deep ML knowledge rather than discard previous engineering expertise.

---

# 14. Progress Tracking

Use [PROGRESS.md](PROGRESS.md) to record:

- Current week and phase.
- Completed deliverables.
- Weekly study time.
- Assessment scores.
- Knowledge gaps.
- Next actions.

Each completed week should have its own directory under `weeks/`.

Recommended weekly structure:

```text
week-NNN/
├── README.md
├── notes.md
├── exercises/
├── src/
├── tests/
└── results/
```

The weekly README should include objectives, reading assignments, mathematical exercises, implementation tasks, experiments, and acceptance criteria.

Do not create all 104 directories in advance. Add them progressively as the work is completed.

---

# 15. Important Notes

- This roadmap is a structured learning plan, not a guarantee of employment or research-level mastery within a fixed period.
- The actual pace may change depending on work commitments, mathematical difficulty, and project complexity.
- Advanced research topics should be selected based on current literature rather than following a fixed list forever.
- Large-scale training is not a prerequisite for learning research engineering.
- Optional resources should supplement the core curriculum, not compete with it.
- The roadmap should be reviewed periodically, but its foundations should remain stable.

---

**The long-term objective: become an engineer who can understand the mathematics, implement the model, run rigorous experiments, analyze research, and build reliable AI systems.**
