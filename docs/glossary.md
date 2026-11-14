# AI Research Engineer Academy — Technical Glossary

This glossary defines important terminology used throughout the AI Research Engineer Academy.

It is designed as a growing technical reference for mathematics, machine learning, deep learning, natural language processing, large language models, and research engineering.

The glossary prioritizes conceptual understanding over memorizing translations.

Each entry may include:

- **Definition** — what the term means.
- **Intuition** — an informal explanation.
- **Mathematics** — a relevant mathematical formulation.
- **Context** — where the concept is used.

The glossary will evolve throughout the Academy.

---

# 1. Mathematics and Linear Algebra

## 1.1 Basic Mathematics

| Term                | Definition                                                                                        |
| ------------------- | ------------------------------------------------------------------------------------------------- |
| Scalar              | A single numerical value.                                                                         |
| Variable            | A symbol representing a value that may change.                                                    |
| Constant            | A value that remains fixed within a given expression or problem.                                  |
| Function            | A mapping from inputs to outputs.                                                                 |
| Domain              | The set of valid inputs to a function.                                                            |
| Range               | The set of values a function can produce.                                                         |
| Equation            | A statement that two expressions are equal.                                                       |
| Inequality          | A mathematical statement comparing two expressions.                                               |
| Summation           | The addition of a sequence of values, commonly represented by \(\sum\).                           |
| Product             | The multiplication of values.                                                                     |
| Absolute Value      | The non-negative magnitude of a real number.                                                      |
| Norm                | A mathematical measure of the magnitude of a vector.                                              |
| Distance Metric     | A function measuring distance between elements of a space.                                        |
| Approximation       | A value or method that is close to the exact result.                                              |
| Numerical Stability | The ability of a numerical computation to limit the effects of rounding and approximation errors. |

## 1.2 Linear Algebra

| Term                               | Definition                                                                                       |
| ---------------------------------- | ------------------------------------------------------------------------------------------------ |
| Vector                             | An ordered collection of numerical components.                                                   |
| Matrix                             | A rectangular array of numbers.                                                                  |
| Tensor                             | A multidimensional array; in ML, often used as a general representation of numerical data.       |
| Vector Space                       | A set of vectors with defined addition and scalar multiplication operations.                     |
| Linear Combination                 | A weighted sum of vectors.                                                                       |
| Linear Independence                | A set of vectors where no vector can be represented as a linear combination of the others.       |
| Basis                              | A linearly independent set of vectors that spans a vector space.                                 |
| Dimension                          | The number of vectors in a basis of a finite-dimensional vector space.                           |
| Span                               | The set of all possible linear combinations of a collection of vectors.                          |
| Dot Product                        | A scalar product of two vectors, commonly written as \(a^\top b\).                               |
| Inner Product                      | A generalized operation that measures relationships between vectors.                             |
| Orthogonality                      | A relationship where the inner product of two vectors is zero.                                   |
| Projection                         | The component of one vector along another vector or subspace.                                    |
| Transpose                          | An operation that exchanges the rows and columns of a matrix.                                    |
| Identity Matrix                    | A square matrix that leaves vectors unchanged under multiplication.                              |
| Inverse Matrix                     | A matrix that reverses the transformation of an invertible square matrix.                        |
| Determinant                        | A scalar describing important properties of a square matrix, including whether it is invertible. |
| Rank                               | The dimension of the column space or row space of a matrix.                                      |
| Null Space                         | The set of vectors mapped to zero by a matrix.                                                   |
| Column Space                       | The set of all linear combinations of a matrix's columns.                                        |
| Eigenvalue                         | A scalar describing how an eigenvector is scaled by a linear transformation.                     |
| Eigenvector                        | A non-zero vector whose direction is preserved by a linear transformation.                       |
| Diagonalization                    | Representing a matrix in a diagonal form through a suitable change of basis, when possible.      |
| Singular Value Decomposition (SVD) | A factorization of a matrix into orthogonal factors and a diagonal matrix of singular values.    |
| Positive Definite Matrix           | A symmetric matrix whose quadratic form is strictly positive for every non-zero vector.          |
| Least Squares                      | An optimization method that minimizes the sum of squared residuals.                              |

### Important equations

Dot product:

\[
a^\top b = \sum_{i=1}^{n} a_i b_i
\]

Euclidean norm:

\[
\|x\|_2 = \sqrt{\sum_{i=1}^{n}x_i^2}
\]

Matrix multiplication:

\[
C_{ij} = \sum_k A_{ik}B_{kj}
\]

Eigenvalue equation:

\[
Av = \lambda v
\]

Least squares:

\[
\min_x \|Ax-b\|_2^2
\]

SVD:

\[
A = U\Sigma V^\top
\]

---

# 2. Calculus and Optimization

| Term                | Definition                                                                                                             |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Limit               | The value a function approaches as its input approaches a particular point.                                            |
| Continuity          | A property describing whether a function changes without a discontinuity.                                              |
| Derivative          | The instantaneous rate of change of a function.                                                                        |
| Partial Derivative  | A derivative with respect to one variable while other variables are held constant.                                     |
| Gradient            | A vector containing the partial derivatives of a scalar-valued function.                                               |
| Jacobian            | A matrix of first-order partial derivatives of a vector-valued function.                                               |
| Hessian             | A matrix of second-order partial derivatives.                                                                          |
| Chain Rule          | A rule for differentiating composite functions.                                                                        |
| Integral            | A mathematical operation representing accumulation or area under a curve in appropriate settings.                      |
| Optimization        | Finding the best solution according to a specified objective.                                                          |
| Objective Function  | A function that defines what an optimization process tries to minimize or maximize.                                    |
| Loss Function       | A function measuring the discrepancy between model predictions and target values.                                      |
| Gradient Descent    | An optimization algorithm that updates parameters in the direction opposite to the gradient.                           |
| Learning Rate       | A parameter controlling the size of an optimization update.                                                            |
| Local Minimum       | A point that has a lower objective value than nearby points.                                                           |
| Global Minimum      | A point with the lowest objective value over the entire feasible domain.                                               |
| Convex Function     | A function whose value along a line segment does not exceed the corresponding linear interpolation of endpoint values. |
| Non-convex Function | A function that is not convex.                                                                                         |
| Convergence         | The process of approaching a limiting value or solution.                                                               |
| Numerical Gradient  | An approximation of a derivative calculated using finite differences.                                                  |

### Important equations

Derivative:

\[
f'(x) = \lim_{h\to 0}\frac{f(x+h)-f(x)}{h}
\]

Gradient descent:

\[
\theta_{t+1} = \theta_t - \eta \nabla_\theta L(\theta_t)
\]

Chain rule:

\[
\frac{d}{dx}f(g(x)) = f'(g(x))g'(x)
\]

---

# 3. Probability and Statistics

| Term                                   | Definition                                                                                                      |
| -------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Probability                            | A numerical measure of the likelihood of an event.                                                              |
| Random Variable                        | A variable whose value is determined by a random process.                                                       |
| Sample Space                           | The set of all possible outcomes of an experiment.                                                              |
| Event                                  | A subset of a sample space.                                                                                     |
| Probability Distribution               | A mathematical description of possible values and their probabilities.                                          |
| Probability Mass Function (PMF)        | A function assigning probabilities to discrete outcomes.                                                        |
| Probability Density Function (PDF)     | A density function describing a continuous random variable.                                                     |
| Cumulative Distribution Function (CDF) | The probability that a random variable is less than or equal to a given value.                                  |
| Expected Value                         | The probability-weighted average of a random variable.                                                          |
| Variance                               | A measure of dispersion around the mean.                                                                        |
| Standard Deviation                     | The square root of variance.                                                                                    |
| Covariance                             | A measure of how two variables vary together.                                                                   |
| Correlation                            | A normalized measure of association between two variables.                                                      |
| Conditional Probability                | The probability of an event given that another event occurred.                                                  |
| Bayes' Theorem                         | A rule for updating probabilities using observed evidence.                                                      |
| Independence                           | A relationship where knowing one event provides no information about another event's occurrence.                |
| Likelihood                             | The probability of observed data considered as a function of model parameters.                                  |
| Prior                                  | A probability distribution representing beliefs before observing current data.                                  |
| Posterior                              | A probability distribution updated using observed evidence.                                                     |
| Sampling                               | Selecting observations from a population or distribution.                                                       |
| Estimator                              | A procedure for estimating an unknown quantity from data.                                                       |
| Bias                                   | Systematic error in an estimator or model prediction.                                                           |
| Confidence Interval                    | An interval procedure designed to cover a population parameter at a specified long-run frequency.               |
| Hypothesis Testing                     | A statistical procedure for evaluating a claim using observed data.                                             |
| P-value                                | The probability, under a specified null hypothesis, of obtaining results at least as extreme as those observed. |
| Central Limit Theorem                  | A result describing conditions under which normalized sums or averages approach a normal distribution.          |

### Important equations

Expected value:

\[
\mathbb{E}[X] = \sum_x xP(X=x)
\]

Variance:

\[
\operatorname{Var}(X)=\mathbb{E}[(X-\mathbb{E}[X])^2]
\]

Bayes' theorem:

\[
P(A|B)=\frac{P(B|A)P(A)}{P(B)}
\]

Covariance:

\[
\operatorname{Cov}(X,Y)=
\mathbb{E}[(X-\mathbb{E}[X])(Y-\mathbb{E}[Y])]
\]

---

# 4. Classical Machine Learning

| Term                     | Definition                                                                                     |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| Machine Learning (ML)    | A field focused on algorithms that learn patterns from data.                                   |
| Dataset                  | A collection of data used for analysis or model development.                                   |
| Feature                  | An input variable used by a model.                                                             |
| Label                    | The target value a supervised model attempts to predict.                                       |
| Training Set             | Data used to fit model parameters.                                                             |
| Validation Set           | Data used for model selection and hyperparameter tuning.                                       |
| Test Set                 | Data reserved for final evaluation.                                                            |
| Supervised Learning      | Learning from labeled examples.                                                                |
| Unsupervised Learning    | Discovering patterns in data without target labels.                                            |
| Semi-supervised Learning | Learning from a combination of labeled and unlabeled data.                                     |
| Self-supervised Learning | Creating supervisory signals from the data itself.                                             |
| Classification           | Predicting a discrete category.                                                                |
| Regression               | Predicting a continuous numerical value.                                                       |
| Clustering               | Grouping similar observations.                                                                 |
| Feature Engineering      | Creating or transforming input features to improve model performance.                          |
| Feature Scaling          | Transforming numerical features to comparable scales.                                          |
| Normalization            | A transformation that maps data to a specified scale or distribution, depending on context.    |
| Standardization          | Transforming data to have zero mean and unit variance, typically per feature.                  |
| Overfitting              | Learning training-specific patterns that do not generalize well.                               |
| Underfitting             | Failing to capture important patterns in the data.                                             |
| Generalization           | Performance on previously unseen data drawn from the relevant target distribution.             |
| Regularization           | Techniques that discourage undesirable model complexity or behavior.                           |
| Hyperparameter           | A configuration parameter chosen outside the model's ordinary parameter-learning process.      |
| Cross-validation         | Repeatedly splitting data to estimate model performance more robustly.                         |
| Data Leakage             | Using information during training that would not legitimately be available at prediction time. |
| Baseline Model           | A reference model used for comparison.                                                         |
| Class Imbalance          | A dataset condition where classes have substantially different frequencies.                    |
| Decision Boundary        | A boundary separating predicted classes in feature space.                                      |

## Common algorithms

| Algorithm                          | Description                                                                           |
| ---------------------------------- | ------------------------------------------------------------------------------------- |
| Linear Regression                  | Predicts a continuous output using a linear function of features.                     |
| Logistic Regression                | Models class probabilities using a logistic function or related link function.        |
| Decision Tree                      | Predicts using a sequence of feature-based decisions.                                 |
| Random Forest                      | An ensemble of decision trees trained with randomized sampling and feature selection. |
| Gradient Boosting                  | Builds an ensemble sequentially to improve a prediction objective.                    |
| K-Nearest Neighbors (KNN)          | Predicts using nearby training observations.                                          |
| Naive Bayes                        | Uses Bayes' theorem with conditional independence assumptions.                        |
| K-Means                            | Partitions observations into clusters based on distances to cluster centers.          |
| Principal Component Analysis (PCA) | A dimensionality-reduction method based on directions of maximum variance.            |

## Evaluation metrics

| Term                      | Definition                                                                        |
| ------------------------- | --------------------------------------------------------------------------------- |
| Accuracy                  | Fraction of predictions that are correct.                                         |
| Precision                 | Fraction of predicted positives that are true positives.                          |
| Recall                    | Fraction of actual positives that are identified.                                 |
| F1 Score                  | Harmonic mean of precision and recall.                                            |
| Confusion Matrix          | A table comparing predicted and actual class labels.                              |
| Mean Squared Error (MSE)  | Average squared prediction error.                                                 |
| Mean Absolute Error (MAE) | Average absolute prediction error.                                                |
| ROC Curve                 | A curve showing true positive rate against false positive rate across thresholds. |
| AUC                       | Area under a curve, often referring to ROC-AUC in classification.                 |

---

# 5. Deep Learning

| Term                  | Definition                                                                                     |
| --------------------- | ---------------------------------------------------------------------------------------------- |
| Deep Learning         | Machine learning using neural networks with multiple layers.                                   |
| Neural Network        | A parameterized computational model composed of interconnected operations.                     |
| Neuron                | A computational unit that applies a transformation and activation to its inputs.               |
| Layer                 | A group of operations in a neural network.                                                     |
| Weight                | A trainable parameter controlling the contribution of an input.                                |
| Bias                  | A trainable additive parameter.                                                                |
| Activation Function   | A function introducing non-linearity into a neural network.                                    |
| Forward Pass          | Computation of model outputs from inputs and current parameters.                               |
| Backpropagation       | An algorithm for calculating gradients through a computational graph using the chain rule.     |
| Computational Graph   | A representation of operations and dependencies in a computation.                              |
| Epoch                 | One complete pass through the training dataset.                                                |
| Batch                 | A subset of training examples processed together.                                              |
| Batch Size            | The number of examples in a batch.                                                             |
| Iteration             | One optimization update, typically based on one batch.                                         |
| Optimizer             | An algorithm that updates model parameters.                                                    |
| SGD                   | Stochastic Gradient Descent, an optimizer using gradients from individual examples or batches. |
| Momentum              | An optimization technique that accumulates information from previous gradients.                |
| Adam                  | An adaptive optimizer using estimates of first and second moments of gradients.                |
| Weight Initialization | The method used to set initial model parameters.                                               |
| Dropout               | A regularization technique that randomly disables units during training.                       |
| Batch Normalization   | A normalization technique applied to intermediate activations.                                 |
| Layer Normalization   | A normalization technique applied across features within individual examples.                  |
| Vanishing Gradient    | A situation where gradients become very small during backpropagation.                          |
| Exploding Gradient    | A situation where gradients become excessively large.                                          |
| Residual Connection   | A connection that adds an earlier representation to a later transformation.                    |
| Convolution           | An operation that applies shared filters across structured input dimensions.                   |
| Pooling               | An operation that reduces spatial or sequence dimensions by aggregating values.                |
| Embedding             | A learned or fixed vector representation of a discrete item.                                   |
| Transfer Learning     | Reusing knowledge from a previously trained model.                                             |
| Fine-tuning           | Further training a pretrained model on a target task or dataset.                               |

## Activation functions

| Term    | Definition                                                                  |
| ------- | --------------------------------------------------------------------------- |
| ReLU    | Returns the input when positive and zero otherwise.                         |
| Sigmoid | Maps real-valued inputs to values between zero and one.                     |
| Tanh    | Maps real-valued inputs to values between minus one and one.                |
| GELU    | A smooth activation function commonly used in Transformer architectures.    |
| Softmax | Converts a vector of scores into normalized positive values summing to one. |

---

# 6. Natural Language Processing

| Term                              | Definition                                                                                   |
| --------------------------------- | -------------------------------------------------------------------------------------------- |
| Natural Language Processing (NLP) | A field focused on computational processing of human language.                               |
| Corpus                            | A collection of text documents used for linguistic analysis or model training.               |
| Token                             | A unit of text processed by a model.                                                         |
| Tokenization                      | Splitting text into tokens.                                                                  |
| Vocabulary                        | The set of tokens known to a tokenizer or model.                                             |
| Subword Tokenization              | Splitting text into units smaller than words but often larger than characters.               |
| Byte Pair Encoding (BPE)          | A tokenization algorithm that iteratively merges frequent symbol pairs.                      |
| Word Embedding                    | A dense vector representation of a word or token.                                            |
| Positional Encoding               | Information added to representations to communicate token positions.                         |
| Sequence Modeling                 | Learning patterns across ordered data.                                                       |
| Language Modeling                 | Modeling the probability distribution of token sequences.                                    |
| N-gram                            | A contiguous sequence of N tokens.                                                           |
| Perplexity                        | An exponentiated average negative log-likelihood, commonly used to evaluate language models. |
| Named Entity Recognition (NER)    | Identifying entities such as people, locations, and organizations in text.                   |
| Machine Translation               | Automatically translating text between languages.                                            |
| Text Classification               | Assigning categories to text.                                                                |

---

# 7. Attention and Transformers

| Term                         | Definition                                                                                                                    |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Attention                    | A mechanism that computes weighted combinations of information from different positions or elements.                          |
| Query (Q)                    | A representation used to determine what information a position is looking for.                                                |
| Key (K)                      | A representation used to determine how relevant an element is to a query.                                                     |
| Value (V)                    | The information aggregated using attention weights.                                                                           |
| Scaled Dot-Product Attention | An attention mechanism that computes similarity scores, scales them, applies softmax, and aggregates values.                  |
| Self-Attention               | Attention where queries, keys, and values are derived from the same sequence representation.                                  |
| Cross-Attention              | Attention where queries come from one sequence and keys and values come from another.                                         |
| Multi-Head Attention         | Multiple attention operations performed in parallel using different learned projections.                                      |
| Causal Mask                  | A mask preventing a position from attending to future positions.                                                              |
| Attention Mask               | A mask controlling which positions may participate in attention.                                                              |
| Transformer                  | A neural network architecture built primarily around attention and feed-forward transformations.                              |
| Encoder                      | A component that produces contextual representations from input sequences.                                                    |
| Decoder                      | A component that generates or transforms sequences, often using causal attention.                                             |
| Feed-Forward Network (FFN)   | A neural network transformation applied independently to each sequence position.                                              |
| Residual Stream              | The representation pathway that carries information through Transformer layers.                                               |
| LayerNorm                    | Layer normalization applied to hidden representations.                                                                        |
| Context Window               | The maximum number of tokens a model can process together in a particular configuration.                                      |
| KV Cache                     | Stored key and value tensors reused during autoregressive generation.                                                         |
| RoPE                         | Rotary Positional Embedding, a method that encodes positional information through rotations of query and key representations. |
| ALiBi                        | Attention with Linear Biases, a method that adds position-dependent biases to attention scores.                               |
| Encoder-only Model           | A model architecture commonly used for contextual representation and understanding tasks.                                     |
| Decoder-only Model           | An autoregressive architecture commonly used for text generation.                                                             |
| Encoder-decoder Model        | An architecture with separate input encoding and output generation components.                                                |

### Scaled dot-product attention

\[
\operatorname(Q,K,V)
====================

\operatorname{softmax}
\left(
\frac{QK^\top}{\sqrt{d_k}}
\right)V
\]

Where:

- \(Q\) represents queries.
- \(K\) represents keys.
- \(V\) represents values.
- \(d_k\) is the key dimension.

---

# 8. Large Language Models

| Term                                              | Definition                                                                                                                                   |
| ------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Large Language Model (LLM)                        | A large neural language model trained to model and generate text or other token sequences.                                                   |
| Pretraining                                       | Initial large-scale training on a broad dataset.                                                                                             |
| Next-Token Prediction                             | Predicting the next token based on preceding context.                                                                                        |
| Autoregressive Model                              | A model that generates a sequence one element at a time conditioned on previous elements.                                                    |
| Instruction Tuning                                | Fine-tuning a model on instruction-following examples.                                                                                       |
| Supervised Fine-Tuning (SFT)                      | Training on input-output examples with target outputs.                                                                                       |
| Alignment                                         | Techniques intended to make model behavior better match desired objectives or preferences.                                                   |
| Reinforcement Learning from Human Feedback (RLHF) | A family of methods using human preference feedback to guide model behavior.                                                                 |
| Direct Preference Optimization (DPO)              | A method for optimizing model behavior using preference pairs without a separate reward-model optimization loop in its standard formulation. |
| Reward Model                                      | A model trained to assign scores representing preferences or desired outcomes.                                                               |
| Hallucination                                     | Generated content that is unsupported, incorrect, or fabricated.                                                                             |
| Prompt                                            | An input instruction or context supplied to a model.                                                                                         |
| Prompt Engineering                                | Designing prompts to influence model outputs.                                                                                                |
| Sampling                                          | Selecting tokens from a model's output probability distribution.                                                                             |
| Temperature                                       | A parameter controlling the sharpness of a probability distribution during sampling.                                                         |
| Top-k Sampling                                    | Restricting sampling to the k highest-probability tokens.                                                                                    |
| Top-p Sampling                                    | Restricting sampling to the smallest set of tokens whose cumulative probability reaches a threshold.                                         |
| Quantization                                      | Representing model parameters or computations using lower numerical precision.                                                               |
| Distillation                                      | Training a smaller or different model using information from a larger teacher model.                                                         |
| LoRA                                              | Low-Rank Adaptation, a parameter-efficient fine-tuning method using trainable low-rank updates.                                              |
| QLoRA                                             | A fine-tuning approach combining quantization with LoRA.                                                                                     |
| Parameter-Efficient Fine-Tuning (PEFT)            | Methods that adapt models by training a relatively small number of parameters.                                                               |
| Retrieval-Augmented Generation (RAG)              | A method that retrieves external information and uses it as context for generation.                                                          |
| Embedding Model                                   | A model that maps inputs into vector representations.                                                                                        |
| Vector Database                                   | A system designed to store and search vector representations.                                                                                |
| Grounding                                         | Connecting model outputs to external evidence or supplied context.                                                                           |
| Evaluation Benchmark                              | A standardized collection of tasks or measurements used to compare systems.                                                                  |
| Contamination                                     | The presence of evaluation data or closely related material in model training data.                                                          |

---

# 9. ML Systems and Performance Engineering

| Term                   | Definition                                                                                     |
| ---------------------- | ---------------------------------------------------------------------------------------------- |
| CPU                    | Central Processing Unit, a general-purpose processor.                                          |
| GPU                    | Graphics Processing Unit, a processor designed for highly parallel computation.                |
| CUDA                   | NVIDIA's parallel computing platform and programming model.                                    |
| Kernel                 | A function executed on a GPU or other parallel computing device.                               |
| FLOPs                  | Floating-point operations, a measure of numerical computation.                                 |
| FLOP/s                 | Floating-point operations per second, a measure of computational throughput.                   |
| Throughput             | The amount of work completed per unit of time.                                                 |
| Latency                | The time required to complete an operation or request.                                         |
| Memory Bandwidth       | The rate at which data can be transferred between memory and processors.                       |
| VRAM                   | Memory available on a GPU.                                                                     |
| Mixed Precision        | Using multiple numerical precisions within one computation.                                    |
| FP32                   | 32-bit floating-point representation.                                                          |
| FP16                   | 16-bit floating-point representation.                                                          |
| BF16                   | 16-bit floating-point representation with a wider exponent range than FP16.                    |
| Gradient Accumulation  | Combining gradients from multiple smaller batches before updating parameters.                  |
| Gradient Checkpointing | Reducing activation memory by recomputing selected intermediate values during backpropagation. |
| Distributed Training   | Training a model across multiple devices or machines.                                          |
| Data Parallelism       | Distributing batches across devices while maintaining model replicas.                          |
| Model Parallelism      | Splitting model computations or parameters across devices.                                     |
| Tensor Parallelism     | Distributing tensor operations across multiple devices.                                        |
| Pipeline Parallelism   | Dividing model layers into stages executed across devices.                                     |
| Bottleneck             | A resource or operation limiting overall system performance.                                   |
| Profiling              | Measuring runtime behavior to identify performance characteristics and bottlenecks.            |
| Batching               | Processing multiple requests or examples together.                                             |
| Continuous Batching    | Dynamically managing batches as requests arrive and finish.                                    |
| Inference              | Running a trained model to produce predictions or outputs.                                     |
| Model Serving          | Making a model available through an application or service interface.                          |
| Quantization Error     | Numerical error introduced by representing values with reduced precision.                      |

---

# 10. Research Methodology

| Term                     | Definition                                                                                     |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| Research Question        | A specific question that an investigation aims to answer.                                      |
| Hypothesis               | A testable prediction about an expected relationship or outcome.                               |
| Literature Review        | A structured analysis of existing research.                                                    |
| Research Gap             | An unresolved or insufficiently investigated aspect of a research area.                        |
| Baseline                 | A reference method or result used for comparison.                                              |
| Ablation Study           | An experiment investigating the contribution of individual system components.                  |
| Independent Variable     | A variable deliberately changed during an experiment.                                          |
| Dependent Variable       | A variable measured as an experimental outcome.                                                |
| Control Variable         | A variable kept constant to support a fair comparison.                                         |
| Confounding Variable     | A variable that may influence both the independent and dependent variables.                    |
| Reproducibility          | The ability to repeat an experiment using documented methods and resources.                    |
| Replication              | Repeating a study or experiment to examine whether its findings hold.                          |
| Statistical Significance | A conclusion based on a statistical procedure and its assumptions.                             |
| Effect Size              | A measure of the magnitude of an observed effect.                                              |
| Ablation                 | Removal or modification of a component to investigate its contribution.                        |
| Benchmark                | A standardized task, dataset, or procedure used for evaluation.                                |
| Negative Result          | A result that does not support the expected hypothesis or does not show an anticipated effect. |
| Threat to Validity       | A factor that may weaken the correctness or generalizability of a conclusion.                  |
| Peer Review              | Evaluation of research by other experts in the field.                                          |
| Preprint                 | A publicly shared research manuscript that may not yet have completed peer review.             |
| Artifact                 | Code, data, configurations, models, or other materials supporting a research result.           |

---

# 11. Common Mathematical and Programming Notation

| Symbol                 | Meaning                                                         |
| ---------------------- | --------------------------------------------------------------- |
| \(x\)                  | Scalar or input variable                                        |
| \(\mathbf{x}\)         | Vector                                                          |
| \(A\)                  | Matrix                                                          |
| \(A^\top\)             | Matrix transpose                                                |
| \(A^{-1}\)             | Matrix inverse, when it exists                                  |
| \(\mathbf{I}\)         | Identity matrix                                                 |
| \(\lambda\)            | Often an eigenvalue or regularization parameter                 |
| \(\sum\)               | Summation                                                       |
| \(\prod\)              | Product                                                         |
| \(\nabla\)             | Gradient operator                                               |
| \(\partial\)           | Partial derivative notation                                     |
| \(\mathbb{E}\)         | Expected value                                                  |
| \(\operatorname{Var}\) | Variance                                                        |
| \(\mathcal{L}\)        | Often a loss function                                           |
| \(\theta\)             | Model parameters                                                |
| \(\eta\)               | Often a learning rate                                           |
| \(\epsilon\)           | A small positive value or error tolerance, depending on context |
| \(O(n)\)               | Asymptotic complexity notation                                  |
| \(\in\)                | Element of a set                                                |
| \(\subseteq\)          | Subset relation                                                 |
| \(\forall\)            | For all                                                         |
| \(\exists\)            | There exists                                                    |
| \(\approx\)            | Approximately equal                                             |
| \(\propto\)            | Proportional to                                                 |

The meaning of a symbol depends on context. Always inspect how it is defined in the source.

---

# 12. Common Abbreviations

| Abbreviation | Full Form                                  |
| ------------ | ------------------------------------------ |
| AI           | Artificial Intelligence                    |
| ML           | Machine Learning                           |
| DL           | Deep Learning                              |
| NLP          | Natural Language Processing                |
| LLM          | Large Language Model                       |
| SLM          | Small Language Model                       |
| ANN          | Artificial Neural Network                  |
| CNN          | Convolutional Neural Network               |
| RNN          | Recurrent Neural Network                   |
| LSTM         | Long Short-Term Memory                     |
| GRU          | Gated Recurrent Unit                       |
| MLP          | Multilayer Perceptron                      |
| SGD          | Stochastic Gradient Descent                |
| Adam         | Adaptive Moment Estimation                 |
| MSE          | Mean Squared Error                         |
| MAE          | Mean Absolute Error                        |
| BCE          | Binary Cross-Entropy                       |
| CE           | Cross-Entropy                              |
| PCA          | Principal Component Analysis               |
| SVD          | Singular Value Decomposition               |
| BPE          | Byte Pair Encoding                         |
| RoPE         | Rotary Positional Embedding                |
| FFN          | Feed-Forward Network                       |
| KV           | Key-Value                                  |
| KV Cache     | Key-Value Cache                            |
| GPU          | Graphics Processing Unit                   |
| CPU          | Central Processing Unit                    |
| VRAM         | Video Random Access Memory                 |
| CUDA         | Compute Unified Device Architecture        |
| AMP          | Automatic Mixed Precision                  |
| DDP          | Distributed Data Parallel                  |
| PEFT         | Parameter-Efficient Fine-Tuning            |
| LoRA         | Low-Rank Adaptation                        |
| QLoRA        | Quantized Low-Rank Adaptation              |
| SFT          | Supervised Fine-Tuning                     |
| RLHF         | Reinforcement Learning from Human Feedback |
| DPO          | Direct Preference Optimization             |
| RAG          | Retrieval-Augmented Generation             |
| API          | Application Programming Interface          |
| CI           | Continuous Integration                     |

---

# 13. How to Use This Glossary

Do not attempt to memorize the entire glossary before starting the curriculum.

Use it as a reference while studying.

For each new important term:

1. Read its definition.
2. Find it in a textbook, lecture, or research paper.
3. Explain it in your own words.
4. Identify its mathematical or practical context.
5. Implement an example when appropriate.
6. Add a note if the term has multiple meanings.

## Mastery levels

| Level                          | Description                                                 |
| ------------------------------ | ----------------------------------------------------------- |
| 0 — Unfamiliar                | The term is new.                                            |
| 1 — Recognition               | Recognizes the term and its general meaning.                |
| 2 — Explanation               | Can explain the concept in own words.                       |
| 3 — Application               | Can use the concept in an exercise or implementation.       |
| 4 — Independent understanding | Can derive, analyze, and apply it in unfamiliar situations. |

A term should only be considered mastered when it can be explained and applied, not merely recognized.

---

# 14. Glossary Maintenance Rules

1. Add terms when they first become relevant in the curriculum.
2. Prefer precise definitions over long descriptions.
3. Include equations for mathematically important concepts.
4. Add examples when a definition is difficult to understand.
5. Distinguish similar concepts explicitly.
6. Preserve standard English terminology.
7. Include references for specialized or disputed definitions.
8. Avoid adding obscure terminology without a learning purpose.
9. Revisit definitions when deeper study reveals a more precise interpretation.

**The goal is to build a working technical vocabulary that makes research papers, documentation, and engineering discussions easier to understand.**
