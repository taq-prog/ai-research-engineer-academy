# AI Research Engineer Academy — Curriculum

A 104-week syllabus organized around **AI Engineering first → AI Research Engineering next**. The first 16 weeks prioritize practical LLM application work while building Python and mathematics foundations in parallel. Later phases progressively deepen ML and research capability.

**Weekly budget:** 5–7 hours (default 6 hours: 5 hours Academy + 1 hour MAANG preparation). Week numbers are planning units, not deadlines.

## Phase map

| Phase | Weeks | Focus | Main evidence |
|---|---:|---|---|
| 1 | 1–4 | Python and Mathematics Foundations | Python exercises and vector/matrix implementations |
| 2 | 5–8 | LLM Application Engineering | Working LLM app |
| 3 | 9–16 | RAG and Production AI Engineering | Evaluated RAG portfolio project |
| 4 | 17–28 | Classical Machine Learning | Reproducible ML pipeline |
| 5 | 29–44 | Deep Learning and PyTorch | Trained neural network |
| 6 | 45–56 | NLP and Transformers | Transformer implementation |
| 7 | 57–68 | LLM Adaptation and Fine-tuning | Fine-tuning comparison |
| 8 | 69–84 | Research Paper Reproduction | Reproduction report |
| 9 | 85–96 | ML Systems, GPU and Performance | Serving / optimization project |
| 10 | 97–104 | Independent Research and Portfolio | Independent research report |

---

## Phase 1 — Python and Mathematics Foundations (Weeks 1–4)

**Goal:** become productive with Python for AI development while building the minimum mathematical foundation needed for vectors, embeddings, and ML.

| Week | Topics | Practical deliverable |
|---:|---|---|
| 1 | Python environment, functions, classes, collections, type hints; algebra, vectors, vector operations | Vector class without NumPy, pytest tests, Two Sum brute force and hash map |
| 2 | Python modules, exceptions, typing, packages; vector spaces, linear combinations, span | Small reusable Python package and vector-space exercises |
| 3 | NumPy arrays, shapes, broadcasting; matrices, matrix multiplication, transpose | Matrix operations and shape-focused tests |
| 4 | Python HTTP/JSON basics, virtual environments, project structure; systems of linear equations | Small API/data exercise and foundations review |

**Resources:** [Python Tutorial](https://docs.python.org/3/tutorial/), [MIT 18.06SC Linear Algebra](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/), [NumPy](https://numpy.org/doc/), [pytest](https://docs.pytest.org/en/stable/).

## Phase 2 — LLM Application Engineering (Weeks 5–8)

**Goal:** build a useful LLM application early, learning the application layer before moving into deeper model internals.

| Week | Topics | Practical deliverable |
|---:|---|---|
| 5 | LLM fundamentals, tokens, context windows, API calls, environment variables and secrets | Minimal LLM client with configuration and error handling |
| 6 | Prompt design, system/user messages, structured outputs, JSON validation | Typed extraction or classification workflow with tests |
| 7 | Tool/function calling, conversation state, retries, timeouts, rate limits | Tool-using assistant with deterministic mock tests |
| 8 | Basic evaluation sets, qualitative review, latency/cost logging, safety boundaries | First end-to-end LLM application and short evaluation report |

**Milestone:** a working LLM app. Understand model/API boundaries, failure modes, and how to test behavior; do not treat prompt examples as reliable evaluation.

## Phase 3 — RAG and Production AI Engineering (Weeks 9–16)

**Goal:** build and evaluate a production-minded retrieval-augmented generation system.

| Week | Topics | Practical deliverable |
|---:|---|---|
| 9 | RAG architecture, document ingestion, parsing, metadata | Ingestion pipeline for a small document collection |
| 10 | Chunking strategies, overlap, metadata filtering | Chunking comparison with inspectable output |
| 11 | Embeddings, vector similarity, cosine similarity, vector stores | Embedding and semantic-search prototype |
| 12 | Retrieval evaluation, recall@k, precision@k, MRR; baseline retrieval | Small labeled query set and retrieval metrics |
| 13 | Hybrid search, reranking, query rewriting | Compare retrieval variants against baseline |
| 14 | Grounded generation, citations, context construction, hallucination analysis | Answer generation with source references and failure cases |
| 15 | Security, prompt injection, access control, privacy, validation | Threat model and security-focused tests |
| 16 | API/service design, observability, latency/cost, Docker, integration | Portfolio-ready RAG service, evaluation report, and .NET integration boundary |

**Milestone:** portfolio-ready RAG system. Include setup instructions, test data, evaluation methodology, limitations, and measured latency/cost. Use local models or hosted APIs according to availability and budget.

---

## Phase 4 — Classical Machine Learning (Weeks 17–28)

**Goal:** understand training, generalization, model selection, and evaluation.

| Week | Topics | Practical deliverable |
|---:|---|---|
| 17 | ML workflow, datasets, labels, splits, leakage | Reproducible dataset pipeline |
| 18 | Linear regression, MSE, normal equation | Regression from scratch |
| 19 | Logistic regression, sigmoid, cross-entropy | Binary classifier from scratch |
| 20 | Gradient descent, learning rates, convergence | Optimization experiment |
| 21 | Confusion matrix, precision, recall, F1, ROC-AUC | Metrics module and threshold analysis |
| 22 | Overfitting, bias/variance, L1/L2 regularization | Regularization comparison |
| 23 | Decision trees, entropy, information gain, Gini | Small decision tree implementation |
| 24 | Random forests, bagging, boosting | Ensemble comparison |
| 25 | KNN, Naive Bayes, scaling | Baseline classifier comparison |
| 26 | Clustering and K-means | Clustering implementation and analysis |
| 27 | PCA, cross-validation, hyperparameter tuning | Dimensionality-reduction experiment |
| 28 | End-to-end ML project, baselines, error analysis | Reproducible classical ML project |

## Phase 5 — Deep Learning and PyTorch (Weeks 29–44)

| Week | Topics | Practical deliverable |
|---:|---|---|
| 29 | Perceptron, neurons, layers | Perceptron implementation |
| 30 | Activations, forward propagation | Small network from scratch |
| 31 | Chain rule, computational graphs, backpropagation | Manual backpropagation |
| 32 | Loss functions, SGD, batches | Training loop |
| 33 | Adam, momentum, initialization | Optimizer comparison |
| 34 | Regularization, dropout, batch normalization | Controlled regularization experiment |
| 35 | PyTorch tensors, autograd | Reimplement network in PyTorch |
| 36 | nn.Module, optimizers, loss functions | Reusable training pipeline |
| 37 | Dataset, DataLoader, transforms | Data loading pipeline |
| 38 | CNNs, convolution, pooling | Small image classifier |
| 39 | CNN architectures and transfer learning | Transfer-learning experiment |
| 40 | RNNs, sequence modeling, limitations | Sequence-model notes and prototype |
| 41 | LSTM/GRU concepts | Sequence classification experiment |
| 42 | GPU training, device placement, reproducibility | CPU/GPU training comparison |
| 43 | Debugging, gradients, overfit-one-batch checks | Training diagnostics |
| 44 | End-to-end deep learning project | Trained model, tests, metrics, and report |

## Phase 6 — NLP and Transformers (Weeks 45–56)

| Week | Topics | Practical deliverable |
|---:|---|---|
| 45 | NLP pipeline, text normalization, tokenization | Tokenization experiments |
| 46 | Subword tokenization, BPE intuition | Simple tokenizer exploration |
| 47 | Language modeling, embeddings | Embedding visualization/analysis |
| 48 | Attention motivation, query/key/value | Attention derivation and tensor exercise |
| 49 | Scaled dot-product attention, masking | Attention implementation |
| 50 | Multi-head attention | Multi-head attention module |
| 51 | Positional encodings/embeddings | Positional information experiment |
| 52 | Feed-forward blocks, residuals, layer normalization | Transformer block |
| 53 | Encoder and decoder architectures | Architecture comparison |
| 54 | Training objectives and language-model loss | Tiny language-model training |
| 55 | Autoregressive generation, sampling, temperature | Text generation experiment |
| 56 | Transformer integration and evaluation | Small Transformer implementation and report |

## Phase 7 — LLM Adaptation and Fine-tuning (Weeks 57–68)

| Week | Topics | Practical deliverable |
|---:|---|---|
| 57 | Pretraining concepts, corpora, data quality | Dataset inspection report |
| 58 | Tokenization pipelines and batching | Reproducible data pipeline |
| 59 | Small language-model training setup | Baseline training run |
| 60 | Training stability, loss curves, checkpoints | Training diagnostics |
| 61 | Scaling laws concepts and compute budgets | Small scaling analysis |
| 62 | Supervised fine-tuning | SFT experiment |
| 63 | LoRA and low-rank adaptation | LoRA implementation/experiment |
| 64 | QLoRA, quantization, memory constraints | Quantization/fine-tuning comparison |
| 65 | Instruction tuning and chat templates | Instruction-tuning pipeline |
| 66 | Preference data, RLHF concepts, DPO | Small preference optimization study |
| 67 | LLM evaluation, task metrics, hallucination analysis | Evaluation suite |
| 68 | End-to-end adaptation project | Baseline vs fine-tuned model report |

## Phase 8 — Research Paper Reproduction (Weeks 69–84)

| Week | Topics | Practical deliverable |
|---:|---|---|
| 69 | Research question, paper search, first-pass reading | Structured paper review |
| 70 | Reproducibility, baselines, datasets, compute planning | Reproduction plan |
| 71 | Transformer paper: architecture | Architecture reconstruction |
| 72 | Transformer paper: bounded experiment | Small-scale reproduction report |
| 73 | BERT architecture and objectives | BERT method notes and prototype |
| 74 | BERT evaluation and reproduction limits | Evaluation comparison |
| 75 | GPT-2 architecture and autoregressive training | GPT-style small configuration |
| 76 | Decoding, sampling, generation evaluation | Generation experiment |
| 77 | GPT-3 and in-context learning | Critical paper analysis |
| 78 | Chinchilla and compute-optimal training | Scaling analysis |
| 79 | LoRA paper: theory and implementation | LoRA implementation |
| 80 | LoRA ablations and evaluation | Ablation report |
| 81 | FlashAttention and IO-aware attention | Attention benchmark/analysis |
| 82 | Experimental design and controlled ablations | Experiment protocol |
| 83 | Research writing and result comparison | Reproduction report draft |
| 84 | Reproduction review and presentation | Reviewed reproduction portfolio item |

Choose reproduction scope based on compute availability. Reproducing a method on a smaller model or dataset is valid when differences from the original setup are clearly stated.

## Phase 9 — ML Systems, GPU and Performance (Weeks 85–96)

| Week | Topics | Practical deliverable |
|---:|---|---|
| 85 | CPU/GPU architecture and memory hierarchy | Architecture notes |
| 86 | CUDA execution model, threads, blocks, warps | GPU execution explanation |
| 87 | CUDA kernels and vector operations | Kernel experiment where hardware permits |
| 88 | Profiling and bottleneck analysis | Profiling report |
| 89 | FP32, FP16, BF16, mixed precision | Precision benchmark |
| 90 | Gradient accumulation and activation checkpointing | Memory optimization experiment |
| 91 | Quantization and quality/performance trade-offs | Quantization benchmark |
| 92 | Inference, prefill/decode, KV cache | KV-cache analysis |
| 93 | Distributed training and DDP concepts | Small distributed experiment or design |
| 94 | Model serving and inference APIs | Model inference service |
| 95 | Latency, throughput, memory, monitoring | Benchmark report |
| 96 | ML systems capstone | Optimized/served model with measured results |

## Phase 10 — Independent Research and Portfolio (Weeks 97–104)

| Week | Topics | Practical deliverable |
|---:|---|---|
| 97 | Topic selection, arXiv/Google Scholar literature search | Topic proposal and bibliography |
| 98 | Research question, hypothesis, measurable outcomes | Research proposal |
| 99 | Baseline method and reproducible evaluation | Baseline implementation |
| 100 | Proposed modification and implementation | Proposed method |
| 101 | Controlled experiments and ablations | Results table |
| 102 | Error analysis, robustness, uncertainty, limitations | Evaluation report |
| 103 | Research writing and reproducibility instructions | Complete research report |
| 104 | Portfolio review and next research direction | Public portfolio and retrospective |

---

## MAANG interview preparation (parallel track)

**Target:** approximately 1 hour per week. Rotate focus rather than attempting every area every week.

- Algorithms and data structures: arrays, hash maps, two pointers, sliding window, binary search, trees, graphs, heaps, dynamic programming, and backtracking.
- C# engineering: collections, LINQ, generics, async/await, Task/ValueTask, cancellation, ThreadPool, synchronization, concurrency, and allocations.
- System design: APIs, data modeling, caching, messaging, scalability, reliability, observability, and distributed systems.
- Senior-level communication: trade-offs, ownership, technical leadership, incidents, and project impact.

## Evaluation and definition of done

A week is complete only when its required evidence exists: code or written work, tests where relevant, experiment results where relevant, and a short explanation in the user's own words. Use [docs/evaluation-rubric.md](docs/evaluation-rubric.md) consistently.

Do not mark a paper as reproduced merely because it has been read. Do not mark a project portfolio-ready without setup instructions, tests, evaluation, and limitations.
