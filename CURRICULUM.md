# AI Research Engineer Academy — Weekly Curriculum

A practical 104-week syllabus with weekly assignments, implementation tasks, experiments, deliverables, and acceptance criteria.

**Duration:** 104 weeks
**Target pace:** 5–7 hours/week
**Primary language:** Python
**Framework:** PyTorch
**Primary objective:** Develop the ability to understand, implement, evaluate, and research machine learning systems.

---

# 1. How to Use This Curriculum

Every week follows the same learning cycle:

1. **Read** — study the assigned theory and documentation.
2. **Understand** — write down the key concepts in your own words.
3. **Derive** — work through the relevant mathematical equations.
4. **Implement** — solve the coding assignments.
5. **Experiment** — change parameters, measure behavior, and compare results.
6. **Document** — record conclusions, limitations, and open questions.

## Weekly time budget

| Activity                    |                 Time |
| --------------------------- | -------------------: |
| Theory and reading          |            1–1.25 h |
| Mathematics                 |            0.75–1 h |
| Implementation              |         1.75–2.25 h |
| Experiments                 |               0.75 h |
| Notes and report            |               0.25 h |
| MAANG interview preparation |                  1 h |
| **Total**             | **5.5–6.5 h** |

If a week becomes too difficult, prioritize understanding and core deliverables over completing every optional exercise.

## Weekly folder convention

```text
weeks/
└── week-001/
    ├── README.md
    ├── notes.md
    ├── exercises/
    ├── src/
    ├── tests/
    └── results/
```

Each weekly `README.md` should contain:

- Learning objectives
- Reading assignments
- Mathematics exercises
- Coding assignments
- Experiment description
- Deliverables
- Acceptance criteria
- Time spent
- Self-assessment

---

# 2. Phase 1 — Mathematics & Python Foundations

**Weeks 1–12**

Primary resources:

- MIT OCW 18.06 Linear Algebra
- Python documentation
- NumPy documentation
- Selected algorithm exercises

## Week 001 — Python and Vector Foundations

**Objectives**

- Set up the Python development environment.
- Understand Python functions, classes, collections, and testing.
- Understand vectors and basic vector operations.

**Reading**

- Python tutorial: functions, classes, data structures.
- MIT Linear Algebra: introductory material on vectors.

**Mathematics**

- Vector addition.
- Scalar multiplication.
- Dot product.
- Vector magnitude.
- Basic algebraic functions.

**Coding**

- Create a Python virtual environment.
- Configure `pyproject.toml`.
- Install pytest and Ruff.
- Implement a `Vector` class without NumPy.
- Implement addition, subtraction, scalar multiplication, dot product, and magnitude.
- Write unit tests.
- Solve Two Sum using brute force and a hash map.

**Experiment**

- Compare the results of your implementation with NumPy.
- Measure the difference between O(n²) and O(n) Two Sum implementations.

**Deliverables**

- `vector.py`
- `test_vector.py`
- `two_sum.py`
- `notes.md`

**Acceptance criteria**

- All tests pass.
- Explain the dot product geometrically.
- Explain why the hash map solution is asymptotically faster.

## Week 002 — Vector Spaces and Linear Independence

**Objectives**

- Understand vector spaces, span, and linear independence.

**Reading**

- MIT Linear Algebra: vector spaces and linear combinations.

**Mathematics**

- Linear combinations.
- Span.
- Linear independence.
- Subspaces.

**Coding**

- Implement vector linear combinations.
- Write a function to construct a matrix from vectors.
- Use NumPy to investigate linear independence.

**Experiment**

- Generate dependent and independent vector sets.
- Compare their matrix ranks.

**Deliverables**

- Vector space exercises.
- Linear independence experiments.
- Written explanation of span and basis.

**Acceptance criteria**

- Explain the difference between span and linear independence.
- Identify dependent vectors in small examples.

## Week 003 — Matrices and Matrix Operations

**Objectives**

- Understand matrices as linear transformations.
- Understand matrix multiplication.

**Reading**

- MIT Linear Algebra: matrices and matrix multiplication.

**Mathematics**

- Matrix addition.
- Matrix multiplication.
- Transpose.
- Identity matrix.
- Matrix-vector multiplication.

**Coding**

- Implement matrix multiplication using Python lists.
- Implement transpose and identity matrix.
- Compare the implementation with NumPy.

**Experiment**

- Measure execution time for different matrix sizes.
- Observe the effect of matrix dimensions.

**Deliverables**

- `matrix.py`
- Matrix unit tests.
- Performance comparison.

**Acceptance criteria**

- Explain matrix multiplication geometrically.
- Correctly implement matrix multiplication for compatible dimensions.

## Week 004 — Systems of Linear Equations

**Objectives**

- Understand systems of equations.
- Learn Gaussian elimination.

**Reading**

- MIT Linear Algebra: elimination and matrix equations.

**Mathematics**

- Row operations.
- Echelon form.
- Reduced row echelon form.
- Pivot variables.

**Coding**

- Implement Gaussian elimination.
- Detect inconsistent systems.
- Solve small systems of linear equations.

**Experiment**

- Compare your results with `numpy.linalg.solve`.
- Test singular and nearly singular matrices.

**Deliverables**

- `gaussian_elimination.py`
- Test cases.
- Mathematical notes.

**Acceptance criteria**

- Explain pivot positions.
- Solve small systems manually and programmatically.

## Week 005 — Rank, Basis, and Dimension

**Objectives**

- Understand the structural properties of matrices.

**Reading**

- MIT Linear Algebra: vector spaces and rank.

**Mathematics**

- Column space.
- Null space.
- Rank.
- Basis.
- Dimension.
- Rank-nullity theorem.

**Coding**

- Compute matrix rank using NumPy.
- Explore null spaces using SVD.
- Implement a basic row-reduction utility.

**Experiment**

- Generate matrices with different ranks.
- Investigate how rank relates to the number of independent columns.

**Deliverables**

- Matrix rank exercises.
- Null space experiments.

**Acceptance criteria**

- Explain rank-nullity.
- Understand the relationship between rank and independent columns.

## Week 006 — Orthogonality and Least Squares

**Objectives**

- Understand projections and approximation.
- Learn least squares regression.

**Reading**

- MIT Linear Algebra: orthogonality and least squares.

**Mathematics**

- Orthogonal vectors.
- Orthogonal projections.
- Projection matrices.
- Least squares.

**Coding**

- Implement vector projection.
- Implement least squares using the normal equation.
- Compare with NumPy and scikit-learn.

**Experiment**

- Fit a line to noisy data.
- Compare exact and noisy solutions.

**Deliverables**

- `least_squares.py`
- Regression experiment.
- Results visualization.

**Acceptance criteria**

- Explain why least squares minimizes squared residuals.
- Understand the geometric interpretation of projection.

## Week 007 — Eigenvalues and Eigenvectors

**Objectives**

- Understand eigenvalues and eigenvectors.
- Explore matrix transformations.

**Reading**

- MIT Linear Algebra: eigenvalues and eigenvectors.

**Mathematics**

- Characteristic polynomial.
- Eigenvalues.
- Eigenvectors.
- Diagonalization.

**Coding**

- Compute eigenvalues and eigenvectors using NumPy.
- Implement a basic power iteration algorithm.

**Experiment**

- Visualize transformations of vectors.
- Investigate eigenvectors of symmetric matrices.

**Deliverables**

- `power_iteration.py`
- Eigenvalue experiments.

**Acceptance criteria**

- Explain the meaning of an eigenvector.
- Understand why eigenvalues are useful in dimensionality reduction.

## Week 008 — Singular Value Decomposition

**Objectives**

- Understand SVD and low-rank approximations.

**Reading**

- MIT Linear Algebra: SVD.

**Mathematics**

- Singular values.
- Singular vectors.
- Matrix factorization.
- Low-rank approximation.

**Coding**

- Apply SVD using NumPy.
- Reconstruct a matrix using selected singular values.

**Experiment**

- Perform image compression using low-rank approximation.
- Compare reconstruction quality at different ranks.

**Deliverables**

- SVD implementation experiments.
- Image compression notebook.

**Acceptance criteria**

- Explain the purpose of SVD.
- Understand the trade-off between compression and reconstruction quality.

## Week 009 — Derivatives and Chain Rule

**Objectives**

- Understand derivatives as rates of change.
- Prepare for gradient-based optimization.

**Reading**

- Introductory calculus material.
- PyTorch autograd introduction.

**Mathematics**

- Limits and derivatives.
- Partial derivatives.
- Chain rule.
- Numerical differentiation.

**Coding**

- Implement numerical derivatives.
- Compare numerical and analytical derivatives.

**Experiment**

- Investigate numerical error using different step sizes.

**Deliverables**

- `derivatives.py`
- Derivative comparison notebook.

**Acceptance criteria**

- Calculate derivatives of elementary functions.
- Explain the chain rule.

## Week 010 — Gradients and Gradient Descent

**Objectives**

- Understand multivariable optimization.

**Reading**

- Introductory optimization material.
- Gradient descent documentation or tutorials.

**Mathematics**

- Gradients.
- Directional derivatives.
- Learning rate.
- Local minima.
- Convexity.

**Coding**

- Implement gradient descent.
- Optimize a simple quadratic function.
- Implement gradient descent for a simple linear regression problem.

**Experiment**

- Compare different learning rates.
- Visualize convergence.

**Deliverables**

- `gradient_descent.py`
- Optimization experiments.

**Acceptance criteria**

- Explain why the negative gradient is a descent direction.
- Identify divergence caused by an excessive learning rate.

## Week 011 — Probability Foundations

**Objectives**

- Build probability intuition for machine learning.

**Reading**

- Introductory probability material.
- Selected probability and statistics reference chapters.

**Mathematics**

- Events and probability.
- Conditional probability.
- Bayes' theorem.
- Independence.
- Discrete and continuous distributions.

**Coding**

- Simulate coin flips and dice rolls.
- Implement simple probability calculations.
- Visualize normal and uniform distributions.

**Experiment**

- Compare empirical probabilities with theoretical values.

**Deliverables**

- Probability simulation notebook.
- Notes on Bayes' theorem.

**Acceptance criteria**

- Explain conditional probability.
- Apply Bayes' theorem to a simple problem.

## Week 012 — Statistics and Foundations Review

**Objectives**

- Consolidate mathematical foundations.

**Reading**

- Review the material from Weeks 1–11.

**Mathematics**

- Expectation.
- Variance.
- Standard deviation.
- Covariance.
- Correlation.
- Sampling.

**Coding**

- Implement statistical calculations.
- Compare with NumPy.
- Complete a small data analysis exercise.

**Experiment**

- Investigate correlation using synthetic datasets.
- Demonstrate why correlation does not imply causation.

**Deliverables**

- Mathematics foundations mini-project.
- Phase review report.

**Acceptance criteria**

- Explain the key concepts from Phase 1.
- Complete the core implementations.
- Identify mathematical topics that need revision.

---

# 3. Phase 2 — Classical Machine Learning

**Weeks 13–24**

Primary resource:

- *Grokking Machine Learning, 2nd Edition*
- scikit-learn documentation

## Week 013 — Machine Learning Workflow

**Reading**

- Introduction to machine learning.
- Dataset and feature concepts.

**Mathematics**

- Training and test distributions.
- Basic statistics review.

**Coding**

- Load a public dataset.
- Implement train/validation/test splitting.
- Build a simple preprocessing pipeline.
- Establish a baseline model.

**Experiment**

- Compare training and validation performance.

**Deliverables**

- Reproducible ML pipeline.

**Acceptance criteria**

- Explain features, labels, and data splits.
- Understand why evaluation data must remain separate from training data.

## Week 014 — Linear Regression

**Reading**

- Linear regression chapter from the core book.

**Mathematics**

- Linear model.
- Mean squared error.
- Normal equation.

**Coding**

- Implement linear regression from scratch.
- Add prediction and evaluation functions.

**Experiment**

- Compare normal equation and gradient descent.

**Deliverables**

- Tested linear regression implementation.

**Acceptance criteria**

- Explain the objective function.
- Understand how model parameters affect predictions.

## Week 015 — Logistic Regression

**Reading**

- Logistic regression and classification material.

**Mathematics**

- Sigmoid.
- Logits.
- Binary cross-entropy.

**Coding**

- Implement logistic regression.
- Implement prediction probabilities.
- Implement binary classification.

**Experiment**

- Change decision thresholds.
- Investigate class imbalance.

**Deliverables**

- Logistic regression implementation.

**Acceptance criteria**

- Explain why logistic regression is a classification model.
- Understand probabilities and decision boundaries.

## Week 016 — Gradient-Based ML Optimization

**Reading**

- Optimization and model training material.

**Mathematics**

- Gradients of MSE and cross-entropy.
- Learning rate.
- Convergence.

**Coding**

- Implement gradient descent for linear and logistic regression.
- Add training history.

**Experiment**

- Compare learning rates and convergence behavior.

**Deliverables**

- Reusable optimization implementation.

**Acceptance criteria**

- Explain how gradients update model parameters.
- Diagnose basic optimization problems.

## Week 017 — Model Evaluation

**Reading**

- Classification and regression metrics.

**Mathematics**

- Confusion matrix.
- Precision and recall.
- F1 score.
- ROC and AUC.

**Coding**

- Implement basic metrics.
- Compare with scikit-learn.

**Experiment**

- Evaluate models under different class distributions.

**Deliverables**

- Reusable model evaluation module.

**Acceptance criteria**

- Choose suitable metrics for a given task.
- Explain the precision-recall trade-off.

## Week 018 — Generalization and Regularization

**Reading**

- Overfitting and regularization.

**Mathematics**

- Bias-variance trade-off.
- L1 and L2 penalties.

**Coding**

- Add L1 and L2 regularization to regression.

**Experiment**

- Compare training and validation performance.
- Investigate model complexity.

**Deliverables**

- Regularization experiment report.

**Acceptance criteria**

- Explain overfitting and underfitting.
- Understand why regularization can improve generalization.

## Week 019 — Decision Trees

**Reading**

- Decision tree algorithms.

**Mathematics**

- Entropy.
- Information gain.
- Gini impurity.

**Coding**

- Implement a basic decision tree for classification.

**Experiment**

- Change tree depth and compare performance.

**Deliverables**

- Basic decision tree implementation.

**Acceptance criteria**

- Explain how a decision tree selects splits.
- Identify overfitting in deep trees.

## Week 020 — Ensemble Learning

**Reading**

- Random forests and boosting.

**Mathematics**

- Bootstrap sampling.
- Variance reduction.
- Ensemble intuition.

**Coding**

- Train random forest and gradient boosting models.
- Compare with a single decision tree.

**Experiment**

- Investigate model performance across configurations.

**Deliverables**

- Ensemble comparison report.

**Acceptance criteria**

- Explain bagging and boosting.
- Understand why ensembles can outperform individual models.

## Week 021 — KNN and Naive Bayes

**Reading**

- K-nearest neighbors.
- Naive Bayes.

**Mathematics**

- Distance metrics.
- Conditional independence.
- Bayes' theorem.

**Coding**

- Implement KNN.
- Implement a basic Naive Bayes classifier.

**Experiment**

- Compare distance metrics and feature scaling.

**Deliverables**

- KNN and Naive Bayes implementations.

**Acceptance criteria**

- Explain the assumptions behind Naive Bayes.
- Understand the impact of scaling on distance-based models.

## Week 022 — Clustering

**Reading**

- Unsupervised learning and clustering.

**Mathematics**

- Euclidean distance.
- Cluster centroids.
- Within-cluster variance.

**Coding**

- Implement K-means from scratch.

**Experiment**

- Change the number of clusters and initialization.
- Compare clustering quality.

**Deliverables**

- K-means implementation and report.

**Acceptance criteria**

- Explain the K-means algorithm.
- Understand its limitations.

## Week 023 — PCA and Validation

**Reading**

- PCA and model selection.

**Mathematics**

- Covariance matrix.
- Eigenvectors.
- Variance explained.

**Coding**

- Implement PCA using SVD.
- Add cross-validation and hyperparameter search.

**Experiment**

- Investigate dimensionality reduction and performance.

**Deliverables**

- PCA implementation and validation pipeline.

**Acceptance criteria**

- Explain PCA conceptually.
- Understand cross-validation and data leakage.

## Week 024 — Classical ML Project

**Project**
Build an end-to-end classical ML application.

**Tasks**

- Select a public dataset.
- Define a prediction problem.
- Establish a baseline.
- Train at least three different model types.
- Evaluate with appropriate metrics.
- Perform error analysis.
- Document limitations.

**Deliverables**

- Reproducible project.
- Tests.
- Experiment configurations.
- Technical report.

**Acceptance criteria**

- Another engineer can reproduce the main results.
- Model choices and evaluation metrics are justified.

---

# 4. Phase 3 — Deep Learning & PyTorch

**Weeks 25–40**

Primary resource:

- *Deep Learning with PyTorch, 2nd Edition*
- Official PyTorch tutorials

## Week 025 — Perceptron and Neural Networks

**Reading**

- Perceptron and neural network fundamentals.

**Mathematics**

- Weighted sums.
- Linear decision boundaries.

**Coding**

- Implement a perceptron.
- Test it on linearly separable data.

**Experiment**

- Visualize decision boundaries.

**Deliverable**

- Perceptron implementation.

**Acceptance criteria**

- Explain weights, bias, and activation.

## Week 026 — Activations and Forward Propagation

**Reading**

- Activation functions and multilayer networks.

**Mathematics**

- Sigmoid.
- Tanh.
- ReLU.
- Softmax.

**Coding**

- Implement a two-layer neural network.
- Implement forward propagation.

**Experiment**

- Compare activation functions.

**Deliverable**

- Neural network forward pass.

**Acceptance criteria**

- Explain how layers transform input representations.

## Week 027 — Backpropagation

**Reading**

- Backpropagation and computational graphs.

**Mathematics**

- Chain rule.
- Partial derivatives.
- Gradients of network parameters.

**Coding**

- Implement backpropagation manually for a small network.
- Verify gradients numerically.

**Experiment**

- Compare analytical and numerical gradients.

**Deliverable**

- Backpropagation implementation.

**Acceptance criteria**

- Explain how gradients propagate through layers.

## Week 028 — Loss Functions and SGD

**Reading**

- Loss functions and optimization.

**Mathematics**

- MSE.
- Cross-entropy.
- Mini-batch gradients.

**Coding**

- Implement a training loop.
- Add mini-batch SGD.

**Experiment**

- Compare batch sizes.

**Deliverable**

- Neural network training pipeline.

**Acceptance criteria**

- Explain the training loop and parameter updates.

## Week 029 — Adam and Initialization

**Reading**

- Momentum and adaptive optimization.

**Mathematics**

- First and second moment estimates.
- Variance and initialization.

**Coding**

- Implement momentum SGD.
- Implement a simplified Adam optimizer.

**Experiment**

- Compare optimizers and initialization methods.

**Deliverable**

- Optimizer benchmark.

**Acceptance criteria**

- Explain the intuition behind Adam and momentum.

## Week 030 — Regularization and Stability

**Reading**

- Dropout, batch normalization, and regularization.

**Mathematics**

- Weight decay.
- Training and inference behavior.

**Coding**

- Add dropout.
- Add weight decay.
- Experiment with normalization.

**Experiment**

- Compare training stability and validation metrics.

**Deliverable**

- Regularization comparison.

**Acceptance criteria**

- Explain the purpose of common regularization techniques.

## Week 031 — PyTorch Tensors and Autograd

**Reading**

- PyTorch tensor and autograd tutorials.

**Coding**

- Reimplement the previous network using tensors.
- Use automatic differentiation.
- Compare gradients with manual backpropagation.

**Experiment**

- Investigate computation graphs.

**Deliverable**

- PyTorch neural network.

**Acceptance criteria**

- Understand tensor shapes and gradient tracking.

## Week 032 — PyTorch Model Architecture

**Reading**

- `nn.Module`, optimizers, and loss functions.

**Coding**

- Build reusable model classes.
- Implement a configurable training loop.
- Add validation and checkpoint saving.

**Experiment**

- Compare model configurations.

**Deliverable**

- Reusable training framework.

**Acceptance criteria**

- Train and evaluate a model using standard PyTorch abstractions.

## Week 033 — Data Loading

**Reading**

- Dataset and DataLoader documentation.

**Coding**

- Implement custom Dataset classes.
- Implement DataLoader pipelines.
- Add transformations and batching.

**Experiment**

- Compare data loading configurations.

**Deliverable**

- Reusable data pipeline.

**Acceptance criteria**

- Understand batching, shuffling, and data loading.

## Week 034 — Convolutional Neural Networks

**Reading**

- CNN fundamentals.

**Mathematics**

- Convolution.
- Padding.
- Stride.
- Receptive fields.

**Coding**

- Implement a small CNN in PyTorch.

**Experiment**

- Change kernel size and architecture.

**Deliverable**

- CNN image classifier.

**Acceptance criteria**

- Explain convolution and pooling.

## Week 035 — CNN Optimization

**Reading**

- Data augmentation and transfer learning.

**Coding**

- Add augmentation.
- Apply transfer learning.
- Compare training from scratch with pretrained weights.

**Experiment**

- Compare accuracy, training time, and data requirements.

**Deliverable**

- CNN optimization report.

**Acceptance criteria**

- Explain when transfer learning is useful.

## Week 036 — RNN Fundamentals

**Reading**

- Recurrent neural networks.

**Mathematics**

- Recurrent state updates.
- Sequence dependencies.

**Coding**

- Implement a simple RNN.
- Train it on a sequence prediction task.

**Experiment**

- Compare sequence lengths.

**Deliverable**

- RNN implementation.

**Acceptance criteria**

- Explain hidden states and recurrent computation.

## Week 037 — LSTM and GRU

**Reading**

- LSTM and GRU architecture.

**Mathematics**

- Gates.
- State updates.
- Gradient propagation through time.

**Coding**

- Build an LSTM model.
- Train it on a sequence dataset.

**Experiment**

- Compare RNN and LSTM.

**Deliverable**

- Sequence modeling report.

**Acceptance criteria**

- Explain why gated recurrent networks were introduced.

## Week 038 — GPU Training

**Reading**

- PyTorch CUDA documentation.

**Coding**

- Move model and tensors to GPU.
- Implement device-aware training.
- Record GPU memory usage.

**Experiment**

- Compare CPU and GPU execution.
- Measure training time.

**Deliverable**

- GPU benchmark.

**Acceptance criteria**

- Understand device placement and GPU memory constraints.

## Week 039 — Experiment Tracking

**Reading**

- Reproducibility and experiment management.

**Coding**

- Save configurations.
- Record metrics.
- Save checkpoints.
- Set random seeds.

**Experiment**

- Run multiple configurations and compare results.

**Deliverable**

- Experiment tracking workflow.

**Acceptance criteria**

- Reproduce a previous experiment from its configuration.

## Week 040 — Deep Learning Project

**Project**
Build a complete deep learning application.

**Tasks**

- Select a dataset.
- Define a baseline.
- Build a PyTorch model.
- Train and evaluate.
- Perform error analysis.
- Save checkpoints and configuration.
- Document results.

**Deliverable**

- Public-quality deep learning project.

**Acceptance criteria**

- Complete reproducible training and evaluation workflow.

---

# 5. Phase 4 — NLP & Transformers

**Weeks 41–56**

Primary resource:

- *Build a Large Language Model (From Scratch)*

Core paper:

- Attention Is All You Need.

## Week 041 — NLP Foundations

**Reading**

- Text preprocessing and NLP fundamentals.

**Coding**

- Build a text cleaning pipeline.
- Explore normalization and sentence splitting.

**Experiment**

- Compare raw and normalized text.

**Deliverable**

- Text preprocessing module.

**Acceptance criteria**

- Explain common NLP preprocessing steps.

## Week 042 — Tokenization and TF-IDF

**Reading**

- Tokenization, vocabulary, and TF-IDF.

**Coding**

- Implement a simple tokenizer.
- Implement TF-IDF.

**Experiment**

- Compare vocabulary sizes and tokenization behavior.

**Deliverable**

- Tokenization and TF-IDF implementation.

**Acceptance criteria**

- Explain how text becomes numerical features.

## Week 043 — Word Embeddings

**Reading**

- Word2Vec and embedding concepts.

**Mathematics**

- Vector similarity.
- Cosine similarity.

**Coding**

- Implement embedding lookup.
- Experiment with pretrained embeddings or a small Word2Vec model.

**Experiment**

- Explore nearest-neighbor relationships.

**Deliverable**

- Embedding experiment.

**Acceptance criteria**

- Explain how embeddings represent semantic relationships.

## Week 044 — Language Modeling

**Reading**

- N-gram language models.

**Mathematics**

- Conditional probabilities.
- Maximum likelihood.

**Coding**

- Implement a bigram language model.

**Experiment**

- Compare generated text at different context settings.

**Deliverable**

- Bigram language model.

**Acceptance criteria**

- Explain next-token probability.

## Week 045 — Sequence Models and Perplexity

**Reading**

- RNN language models and evaluation.

**Coding**

- Train a simple RNN language model.
- Implement perplexity.

**Experiment**

- Compare training and validation perplexity.

**Deliverable**

- RNN language modeling report.

**Acceptance criteria**

- Explain perplexity and its limitations.

## Week 046 — Attention

**Reading**

- Attention Is All You Need: attention mechanism.

**Mathematics**

- Query, key, value.
- Scaled dot-product attention.
- Softmax.

**Coding**

- Implement scaled dot-product attention from scratch.

**Experiment**

- Visualize attention weights.

**Deliverable**

- Attention implementation.

**Acceptance criteria**

- Derive the attention formula and explain each term.

## Week 047 — Multi-Head Attention

**Reading**

- Multi-head attention.

**Coding**

- Implement query, key, and value projections.
- Implement multi-head attention.

**Experiment**

- Change the number of heads and embedding dimensions.

**Deliverable**

- Multi-head attention module.

**Acceptance criteria**

- Explain why attention is split into multiple heads.

## Week 048 — Positional Information

**Reading**

- Positional encoding in Transformers.

**Mathematics**

- Sinusoidal functions.
- Positional representations.

**Coding**

- Implement sinusoidal positional encoding.
- Experiment with learned positional embeddings.

**Experiment**

- Compare positional encoding strategies on a small task.

**Deliverable**

- Positional encoding module.

**Acceptance criteria**

- Explain why attention requires positional information.

## Week 049 — Transformer Encoder

**Reading**

- Transformer Encoder architecture.

**Coding**

- Implement encoder blocks.
- Add residual connections and normalization.

**Experiment**

- Inspect tensor shapes through the network.

**Deliverable**

- Minimal Transformer Encoder.

**Acceptance criteria**

- Explain the structure of an encoder block.

## Week 050 — Transformer Decoder

**Reading**

- Decoder architecture and causal masking.

**Coding**

- Implement causal masks.
- Implement decoder blocks.

**Experiment**

- Verify that future tokens cannot influence earlier predictions.

**Deliverable**

- Minimal Transformer Decoder.

**Acceptance criteria**

- Explain autoregressive masking.

## Week 051 — Encoder-Decoder Models

**Reading**

- Sequence-to-sequence architecture.

**Coding**

- Implement a small encoder-decoder model.

**Experiment**

- Train on a small synthetic sequence transformation task.

**Deliverable**

- Sequence-to-sequence project.

**Acceptance criteria**

- Explain encoder-decoder information flow.

## Week 052 — BERT and Masked Language Modeling

**Reading**

- BERT paper and architecture.

**Coding**

- Build a simplified masked language modeling task.

**Experiment**

- Compare masked token prediction behavior.

**Deliverable**

- BERT-style training experiment.

**Acceptance criteria**

- Explain masked language modeling and bidirectional context.

## Week 053 — GPT and Autoregressive Modeling

**Reading**

- GPT architecture and autoregressive training.

**Coding**

- Build a small GPT-style model.
- Train it on a small text corpus.

**Experiment**

- Compare generated text at different training checkpoints.

**Deliverable**

- Small GPT-style model.

**Acceptance criteria**

- Explain decoder-only language modeling.

## Week 054 — BPE and Subword Tokenization

**Reading**

- Byte Pair Encoding and subword tokenization.

**Coding**

- Implement a simple BPE tokenizer or reproduce a simplified version.

**Experiment**

- Compare vocabulary size, sequence length, and token coverage.

**Deliverable**

- BPE experiment.

**Acceptance criteria**

- Explain the trade-offs in vocabulary design.

## Week 055 — Transformer Complexity

**Reading**

- Attention complexity and memory usage.
- FlashAttention introduction.

**Mathematics**

- Time complexity.
- Space complexity.
- Matrix multiplication cost.

**Coding**

- Benchmark attention on different sequence lengths.

**Experiment**

- Measure memory and latency.

**Deliverable**

- Attention benchmark report.

**Acceptance criteria**

- Explain why long context increases computational cost.

## Week 056 — Transformer Project

**Project**
Implement a small Transformer language model.

**Tasks**

- Implement token embeddings.
- Implement positional encoding.
- Implement attention.
- Implement Transformer blocks.
- Implement causal language modeling.
- Train and evaluate.
- Document limitations.

**Deliverable**

- Transformer from scratch project.

**Acceptance criteria**

- Explain every major component and reproduce a training run.

---

# 6. Phase 5 — LLM Training & Fine-tuning

**Weeks 57–68**

Primary resource:

- *Build a Large Language Model (From Scratch)*

## Week 057 — LLM Architecture

**Reading**

- Decoder-only architecture.
- Model configuration and parameter counts.

**Coding**

- Inspect a small pretrained language model.
- Calculate parameter counts.

**Experiment**

- Compare model dimensions and parameter counts.

**Deliverable**

- LLM architecture analysis.

**Acceptance criteria**

- Explain the relationship between layers, hidden dimensions, and parameter count.

## Week 058 — Tokenization and Context Windows

**Reading**

- Tokenization and context length.

**Coding**

- Compare tokenizers.
- Measure token counts for representative texts.

**Experiment**

- Analyze context length and memory requirements.

**Deliverable**

- Tokenizer comparison report.

**Acceptance criteria**

- Explain how tokenization affects model input and context capacity.

## Week 059 — Dataset Engineering

**Reading**

- Dataset preparation and data quality.

**Coding**

- Build a text dataset pipeline.
- Add cleaning, filtering, and deduplication.
- Record dataset statistics.

**Experiment**

- Compare dataset versions.

**Deliverable**

- Dataset preparation pipeline.

**Acceptance criteria**

- Explain common dataset quality problems.

## Week 060 — Pretraining

**Reading**

- Next-token prediction and pretraining objectives.

**Coding**

- Prepare training batches.
- Implement next-token prediction.
- Train a small language model.

**Experiment**

- Track training loss and validation loss.

**Deliverable**

- Small pretraining experiment.

**Acceptance criteria**

- Explain the pretraining objective and training loop.

## Week 061 — Scaling Laws

**Reading**

- Scaling Laws for Neural Language Models.
- Chinchilla paper introduction.

**Mathematics**

- Parameter scaling.
- Dataset size.
- Compute budget.

**Coding**

- Build a small scaling experiment with available compute.

**Experiment**

- Compare model size and training data size under a fixed budget.

**Deliverable**

- Scaling analysis.

**Acceptance criteria**

- Explain why parameter count alone does not determine model quality.

## Week 062 — Supervised Fine-tuning

**Reading**

- Fine-tuning and supervised instruction tuning.

**Coding**

- Prepare instruction-response data.
- Fine-tune a small pretrained model.

**Experiment**

- Compare the base model and fine-tuned model.

**Deliverable**

- SFT experiment.

**Acceptance criteria**

- Explain the difference between pretraining and fine-tuning.

## Week 063 — LoRA

**Reading**

- LoRA paper.

**Mathematics**

- Low-rank matrices.
- Matrix factorization.

**Coding**

- Implement a simplified LoRA layer.
- Fine-tune a small model using LoRA.

**Experiment**

- Compare trainable parameters and memory consumption.

**Deliverable**

- LoRA experiment.

**Acceptance criteria**

- Explain low-rank adaptation.

## Week 064 — QLoRA and Quantization

**Reading**

- QLoRA concepts and quantization.

**Coding**

- Fine-tune a small quantized model where hardware permits.

**Experiment**

- Compare memory usage and model quality.

**Deliverable**

- Quantization report.

**Acceptance criteria**

- Explain the memory-quality trade-off.

## Week 065 — Instruction Tuning

**Reading**

- Instruction datasets and chat templates.

**Coding**

- Prepare an instruction dataset.
- Implement formatting and training pipelines.

**Experiment**

- Compare outputs before and after instruction tuning.

**Deliverable**

- Instruction-tuning pipeline.

**Acceptance criteria**

- Understand the structure of instruction examples.

## Week 066 — Preference Optimization and DPO

**Reading**

- DPO paper.
- RLHF conceptual introduction.

**Mathematics**

- Preference pairs.
- Log probabilities.
- Objective function intuition.

**Coding**

- Build a small preference dataset.
- Implement or use a simplified DPO training setup.

**Experiment**

- Compare preference optimization with supervised fine-tuning.

**Deliverable**

- DPO experiment.

**Acceptance criteria**

- Explain the purpose of preference optimization.

## Week 067 — LLM Evaluation

**Reading**

- Language model evaluation and hallucination analysis.

**Coding**

- Implement perplexity evaluation.
- Create task-specific test cases.
- Record model outputs.

**Experiment**

- Compare model versions on the same evaluation set.

**Deliverable**

- Small LLM evaluation suite.

**Acceptance criteria**

- Explain why a single metric is insufficient for evaluating an LLM.

## Week 068 — End-to-End LLM Project

**Project**
Fine-tune a small language model for a defined task.

**Tasks**

- Prepare data.
- Establish a baseline.
- Select a fine-tuning method.
- Train the model.
- Evaluate outputs.
- Analyze failure cases.
- Document hardware and compute requirements.

**Deliverable**

- Reproducible fine-tuning project.

**Acceptance criteria**

- Demonstrate measurable and documented model behavior changes.

---

# 7. Phase 6 — Research Paper Reproduction

**Weeks 69–84**

Primary objective: move from using ML techniques to understanding and testing research contributions.

## Week 069 — Research Paper Reading

**Reading**

- Select one foundational ML paper.
- Study its abstract, introduction, methodology, and conclusion.

**Tasks**

- Identify the problem.
- Identify the main contribution.
- Separate claims from evidence.
- List unanswered questions.

**Deliverable**

- Structured paper review.

**Acceptance criteria**

- Explain the paper's contribution without simply paraphrasing its abstract.

## Week 070 — Reproduction Methodology

**Reading**

- Reproducibility and experimental design.

**Tasks**

- Define a reproduction target.
- Identify the baseline.
- Identify the dataset and metrics.
- Estimate compute requirements.
- Document implementation assumptions.

**Deliverable**

- Paper reproduction plan.

**Acceptance criteria**

- Another engineer can understand what will be reproduced and how.

## Week 071 — Attention Is All You Need: Architecture

**Reading**

- Original Transformer paper.

**Tasks**

- Study the architecture.
- Derive scaled dot-product attention.
- Analyze multi-head attention.
- Analyze positional encoding.

**Coding**

- Implement the central architecture components.

**Deliverable**

- Architecture implementation.

**Acceptance criteria**

- Explain the major design decisions.

## Week 072 — Attention Is All You Need: Experiments

**Tasks**

- Reproduce a selected small-scale Transformer experiment.
- Document dataset and training setup.
- Record metrics.

**Experiment**

- Compare a baseline and Transformer implementation.

**Deliverable**

- Transformer reproduction report.

**Acceptance criteria**

- Report results and deviations honestly.

## Week 073 — BERT: Architecture and Objective

**Reading**

- Original BERT paper.

**Tasks**

- Study encoder architecture.
- Study masked language modeling.
- Study next sentence prediction as presented in the original work.

**Coding**

- Implement a simplified masked language modeling pipeline.

**Deliverable**

- BERT architecture notes and implementation.

**Acceptance criteria**

- Explain the original BERT pretraining objectives.

## Week 074 — BERT: Evaluation

**Tasks**

- Study evaluation tasks and methodology.
- Compare model outputs on a small task.
- Investigate the effect of masking strategy.

**Deliverable**

- BERT experiment report.

**Acceptance criteria**

- Distinguish between architecture reproduction and full reproduction of the original training setup.

## Week 075 — GPT-2: Architecture and Training

**Reading**

- GPT-2 paper.

**Tasks**

- Study autoregressive language modeling.
- Analyze the decoder-only architecture.
- Study zero-shot task behavior.

**Coding**

- Reproduce a small GPT-style configuration.

**Deliverable**

- GPT-2 architecture report and experiment.

**Acceptance criteria**

- Explain the key architectural and training choices.

## Week 076 — GPT-2: Generation and Analysis

**Tasks**

- Implement text generation.
- Compare greedy decoding and sampling.
- Analyze temperature and top-k behavior.

**Experiment**

- Evaluate output diversity and quality.

**Deliverable**

- Generation experiment report.

**Acceptance criteria**

- Explain how decoding parameters influence output.

## Week 077 — GPT-3 and In-Context Learning

**Reading**

- GPT-3 paper.

**Tasks**

- Study few-shot, one-shot, and zero-shot learning.
- Analyze scaling claims.
- Examine evaluation methodology.

**Experiment**

- Compare prompt configurations on a small model where practical.

**Deliverable**

- GPT-3 research analysis.

**Acceptance criteria**

- Explain in-context learning and its limitations.

## Week 078 — Chinchilla and Compute-Optimal Training

**Reading**

- Chinchilla paper.

**Tasks**

- Study the relationship between model size, training tokens, and compute.
- Analyze the compute-optimal training argument.

**Coding**

- Reproduce a simplified scaling analysis.

**Deliverable**

- Scaling analysis notebook and report.

**Acceptance criteria**

- Explain why data quantity matters alongside model size.

## Week 079 — LoRA: Theory and Implementation

**Reading**

- Original LoRA paper.

**Tasks**

- Study low-rank updates.
- Understand target modules.
- Analyze parameter efficiency.

**Coding**

- Implement a LoRA layer.
- Compare with full fine-tuning on a small model.

**Deliverable**

- LoRA implementation and benchmark.

**Acceptance criteria**

- Explain the mathematical idea behind LoRA.

## Week 080 — LoRA: Ablation Study

**Tasks**

- Compare multiple ranks.
- Compare target modules.
- Measure memory and training time.

**Experiment**

- Run controlled ablations.

**Deliverable**

- LoRA ablation report.

**Acceptance criteria**

- Explain the observed trade-offs with experimental evidence.

## Week 081 — FlashAttention

**Reading**

- Original FlashAttention paper.

**Tasks**

- Study IO-aware attention.
- Understand memory hierarchy.
- Analyze the relationship between computation and memory traffic.

**Coding**

- Benchmark available attention implementations.

**Deliverable**

- Attention performance report.

**Acceptance criteria**

- Explain the central IO-awareness insight.

## Week 082 — Experimental Design and Ablations

**Tasks**

- Design a controlled experiment.
- Select independent variables.
- Define metrics.
- Establish a baseline.
- Run multiple configurations.

**Deliverable**

- Experimental design document.

**Acceptance criteria**

- Explain why the experiment can distinguish between competing hypotheses.

## Week 083 — Research Report

**Tasks**

- Organize experimental results.
- Compare with published findings.
- Explain discrepancies.
- Document limitations.

**Deliverable**

- Research-style reproduction report.

**Acceptance criteria**

- Report methodology, results, limitations, and conclusions clearly.

## Week 084 — Research Review

**Tasks**

- Review all reproduction projects.
- Identify weak mathematical areas.
- Identify implementation gaps.
- Present one reproduction project.

**Deliverable**

- Phase portfolio review.

**Acceptance criteria**

- Explain the reproduced method and defend experimental choices.

---

# 8. Phase 7 — ML Systems, GPU & Performance

**Weeks 85–96**

Primary resources:

- CUDA documentation.
- PyTorch performance documentation.
- *Grokking Parallel Programming*.

## Week 085 — CPU and GPU Architecture

**Reading**

- Basic computer architecture.
- CPU/GPU execution models.

**Tasks**

- Study parallelism.
- Understand memory hierarchy.
- Compare sequential and parallel workloads.

**Deliverable**

- CPU/GPU architecture notes.

**Acceptance criteria**

- Explain why GPUs are effective for tensor workloads.

## Week 086 — GPU Execution Model

**Reading**

- CUDA programming model.

**Tasks**

- Study threads, blocks, and warps.
- Understand global and shared memory.
- Study memory coalescing.

**Deliverable**

- GPU execution model diagram and notes.

**Acceptance criteria**

- Explain how GPU threads are organized.

## Week 087 — CUDA Kernels

**Reading**

- CUDA kernel programming basics.

**Tasks**

- Write a simple vector addition kernel where supported.
- Explore thread indexing.
- Compare with a CPU implementation.

**Deliverable**

- CUDA kernel experiment.

**Acceptance criteria**

- Explain the basic structure of a CUDA kernel.

## Week 088 — Profiling and Performance

**Reading**

- GPU profiling documentation.

**Tasks**

- Profile a tensor operation.
- Measure execution time.
- Identify memory and compute bottlenecks.

**Deliverable**

- Profiling report.

**Acceptance criteria**

- Use measurements rather than assumptions to identify bottlenecks.

## Week 089 — Numerical Precision

**Reading**

- FP32, FP16, BF16, and mixed precision.

**Tasks**

- Understand numerical range and precision.
- Experiment with mixed precision.

**Deliverable**

- Precision benchmark.

**Acceptance criteria**

- Explain the trade-offs between precision, stability, and performance.

## Week 090 — Training Memory Optimization

**Reading**

- Gradient accumulation.
- Activation checkpointing.

**Tasks**

- Measure memory usage.
- Implement gradient accumulation.
- Test activation checkpointing.

**Deliverable**

- Training memory optimization report.

**Acceptance criteria**

- Explain how these techniques affect memory and computation.

## Week 091 — Quantization

**Reading**

- Quantization concepts.

**Tasks**

- Study integer and floating-point quantization.
- Quantize a small model where supported.

**Experiment**

- Compare model size, latency, and quality.

**Deliverable**

- Quantization benchmark.

**Acceptance criteria**

- Explain the quality-performance trade-off.

## Week 092 — Inference and KV Cache

**Reading**

- Autoregressive inference.
- KV caching.

**Tasks**

- Study prefill and decode.
- Understand KV cache memory requirements.
- Compare cached and uncached generation where practical.

**Deliverable**

- KV cache analysis and benchmark.

**Acceptance criteria**

- Explain why KV caching improves autoregressive inference efficiency.

## Week 093 — Distributed Training

**Reading**

- PyTorch Distributed Data Parallel documentation.

**Tasks**

- Study data parallelism.
- Understand gradient synchronization.
- Explore DDP.

**Experiment**

- Run a small distributed experiment where resources permit.

**Deliverable**

- Distributed training notes and experiment.

**Acceptance criteria**

- Explain the basic DDP workflow and communication overhead.

## Week 094 — Model Serving

**Reading**

- Model inference and serving fundamentals.

**Tasks**

- Build a basic inference API.
- Load a trained model.
- Implement input validation and error handling.

**Deliverable**

- Model inference service.

**Acceptance criteria**

- Serve model predictions through a documented interface.

## Week 095 — Monitoring and Benchmarking

**Tasks**

- Measure latency.
- Measure throughput.
- Track memory.
- Record failures.
- Define benchmark methodology.

**Deliverable**

- Inference benchmark report.

**Acceptance criteria**

- Explain the difference between latency and throughput.

## Week 096 — ML Systems Project

**Project**
Optimize and serve a small model.

**Tasks**

- Establish baseline performance.
- Identify bottlenecks.
- Apply at least one optimization.
- Measure the result.
- Build an inference interface.
- Document limitations.

**Deliverable**

- ML systems project.

**Acceptance criteria**

- Demonstrate a measured performance improvement or a well-supported finding that an optimization did not help.

---

# 9. Phase 8 — Independent Research & Portfolio

**Weeks 97–104**

The final phase combines research, engineering, and communication.

## Week 097 — Research Topic Selection

**Tasks**

- Select a narrow research area.
- Search arXiv and Google Scholar.
- Identify relevant papers.
- Define a problem worth investigating.

**Deliverable**

- Topic proposal and initial bibliography.

**Acceptance criteria**

- Explain why the topic matters and why it is feasible.

## Week 098 — Research Hypothesis

**Tasks**

- Formulate a research question.
- Define a hypothesis.
- Identify measurable outcomes.
- Define potential confounding variables.

**Deliverable**

- Research proposal.

**Acceptance criteria**

- The hypothesis is testable and can be disproved.

## Week 099 — Baseline Implementation

**Tasks**

- Select a baseline method.
- Prepare datasets.
- Define metrics.
- Implement the baseline.
- Run initial evaluation.

**Deliverable**

- Baseline implementation and results.

**Acceptance criteria**

- Baseline results are reproducible.

## Week 100 — Proposed Method

**Tasks**

- Implement the proposed modification.
- Keep the baseline unchanged.
- Document implementation decisions.

**Deliverable**

- Proposed method implementation.

**Acceptance criteria**

- The implementation directly tests the research hypothesis.

## Week 101 — Experiments and Ablations

**Tasks**

- Run controlled experiments.
- Change one major variable at a time.
- Record metrics.
- Compare baseline and proposed method.

**Deliverable**

- Experiment results and ablation table.

**Acceptance criteria**

- Results can be traced to specific configurations.

## Week 102 — Evaluation and Error Analysis

**Tasks**

- Analyze positive and negative results.
- Investigate failure cases.
- Evaluate robustness.
- Discuss statistical uncertainty where appropriate.

**Deliverable**

- Evaluation report.

**Acceptance criteria**

- Conclusions are supported by the evidence.

## Week 103 — Research Writing

**Tasks**

- Write abstract and introduction.
- Explain methodology.
- Present experiments.
- Discuss limitations.
- Document reproduction instructions.

**Deliverable**

- Complete research report.

**Acceptance criteria**

- Another engineer can understand and reproduce the work.

## Week 104 — Final Portfolio Review

**Tasks**

- Clean up repositories.
- Verify installation and execution instructions.
- Review tests.
- Prepare project descriptions.
- Summarize lessons learned.
- Define the next research direction.

**Deliverable**

- Public research portfolio.
- Final Academy retrospective.
- Next-stage learning plan.

**Acceptance criteria**

- The portfolio demonstrates engineering quality, mathematical understanding, experimental discipline, and technical communication.

---

# 10. MAANG Interview Preparation Track

This track runs in parallel with the Academy.

**Target time:** approximately 1 hour per week.

The objective is to preserve algorithmic and software engineering interview readiness while developing ML expertise.

## Recommended rotation

| Week Type | Focus                                                      |
| --------- | ---------------------------------------------------------- |
| A         | Data structures and algorithm patterns                     |
| B         | C# standard library, collections, async and multithreading |
| C         | System design                                              |
| D         | Review previous problems and communicate solutions         |

Repeat the cycle.

### Algorithm practice

Prioritize:

- Arrays and strings.
- Hash maps and sets.
- Two pointers.
- Sliding window.
- Binary search.
- Stacks and queues.
- Linked lists.
- Trees and graphs.
- BFS and DFS.
- Heaps.
- Dynamic programming.
- Backtracking.

For every problem:

1. Explain the brute-force solution.
2. Identify the bottleneck.
3. Derive an optimized solution.
4. Analyze time and space complexity.
5. Implement clean code.
6. Test edge cases.

### C# engineering practice

Focus on:

- Collections and LINQ.
- Generics.
- `Span<T>` and memory concepts.
- `Task` and `ValueTask`.
- `async` / `await`.
- Cancellation tokens.
- Thread safety.
- Locks and synchronization primitives.
- Concurrent collections.
- ThreadPool behavior.
- Exception propagation.
- Performance and allocation analysis.

### System design

Practice:

- Requirements gathering.
- API design.
- Data modeling.
- Scalability.
- Caching.
- Messaging and event-driven systems.
- Database trade-offs.
- Reliability.
- Observability.
- Distributed systems fundamentals.

The goal is to preserve the ability to interview for senior-level software engineering roles while expanding toward AI engineering.

---

# 11. Weekly Evaluation Template

Use this template in each weekly `README.md`.

```markdown
# Week NNN — Topic

## Objectives
- [ ] Objective 1
- [ ] Objective 2

## Reading
- [ ] Resource 1
- [ ] Resource 2

## Mathematics
- [ ] Exercise 1
- [ ] Exercise 2

## Implementation
- [ ] Task 1
- [ ] Task 2
- [ ] Unit tests

## Experiments
- [ ] Baseline
- [ ] Experiment configurations
- [ ] Results recorded

## Deliverables
- [ ] Source code
- [ ] Tests
- [ ] Notes
- [ ] Results

## MAANG Preparation
- [ ] Weekly practice

## Self-assessment

| Dimension | Score (1–5) |
|---|---:|
| Theory | |
| Mathematics | |
| Implementation | |
| Experiments | |
| Communication | |

## Time Spent
- Theory:
- Mathematics:
- Implementation:
- Experiments:
- Documentation:
- MAANG preparation:
- Total:

## What I Learned
...

## What I Could Not Explain Yet
...

## Next Week
...
```

---

# 12. Final Principles

- The curriculum is a guide, not a race.
- Understanding takes priority over speed.
- Do not skip mathematical foundations just to reach LLMs sooner.
- Do not train large models merely to claim that you have trained an LLM.
- Small, controlled experiments are valuable.
- Reproducibility is part of engineering quality.
- Negative results are valid research outcomes.
- Every substantial project should include tests, documentation, and measurable results.

**The desired outcome is not simply familiarity with AI tools. It is the ability to understand the underlying methods, implement them, evaluate them rigorously, and contribute new engineering or research ideas.**
