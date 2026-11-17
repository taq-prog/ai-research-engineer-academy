# Learning Strategy

This document defines how to make progress toward **AI Engineering first, then AI Research Engineering**, within a sustainable 5–7 hour weekly budget.

The near-term objective is to build useful AI systems and credible applied-AI portfolio evidence early. Mathematical depth and research skills grow continuously; they are not postponed, but they also do not block all practical work.

---

## 1. Two-stage learning strategy

### Stage 1 — Applied AI Engineering

Prioritize Python for AI backends, LLM application patterns, structured outputs, tool calling, RAG, evaluation, service integration, reliability, security, observability, latency, and cost.

The key question is: **Can I design, build, test, evaluate, and operate an AI-enabled feature?**

Use existing senior software engineering strengths—API design, distributed systems, testing, production operations, and .NET experience—as leverage. Build Python fluency through real project work rather than isolated syntax drills alone.

### Stage 2 — Research Engineering

Deepen classical ML, mathematics, PyTorch, neural networks, Transformers, fine-tuning, research reading, reproduction, GPU systems, and independent experimentation.

The key question becomes: **Can I understand a method, reconstruct it, test its claims, explain discrepancies, and develop a defensible improvement?**

The 6–12 and 12–24+ month horizons are planning estimates, not promises of role transition. Assess real job descriptions and portfolio evidence continuously.

---

## 2. Weekly schedule: 5–7 hours

Use 6 hours as the default weekly plan.

| Activity | Default time | Purpose |
|---|---:|---|
| Mathematics and theory | 1.25 h | Build conceptual depth alongside applied work |
| Implementation | 2.75 h | Produce working code and project evidence |
| Experiments and evaluation | 0.5 h | Measure quality, behavior, and trade-offs |
| Notes and portfolio | 0.5 h | Record decisions, results, and limitations |
| MAANG preparation | 1 h | Maintain senior SWE interview readiness |
| **Total** | **6 h** | |

The schedule is flexible. In a project-heavy week, shift some theory time to implementation. In a mathematically difficult week, shift the balance back. Keep a sustainable rhythm rather than trying to compensate with unrealistic study sessions.

### Suggested 60-minute session

1. 5 min — recall the previous topic.
2. 10–15 min — learn one focused concept.
3. 30–35 min — implement, solve, or test.
4. 5–10 min — write down what worked and what remains unclear.

---

## 3. The learning loop

For each meaningful topic:

1. **Frame the problem:** what are we trying to solve, and under what assumptions?
2. **Learn enough theory:** understand the core concepts and notation.
3. **Build a baseline:** implement the simplest useful version.
4. **Test it:** include normal cases, edge cases, and failure behavior.
5. **Evaluate:** use explicit metrics or a clear verification method.
6. **Investigate:** compare alternatives and explain surprising results.
7. **Document:** write a concise note, decision, and next step.

Prefer implementation and feedback over long stretches of passive reading. Do not implement everything from scratch: use libraries appropriately, but understand the important abstractions and trade-offs.

---

## 4. Mathematics runs in parallel

Mathematics is essential for research engineering, but it should not become a gate that delays applied AI practice.

Use a just-in-time approach:
- Weeks 1–4: vectors, matrices, linear combinations, dot products, norms, and basic algebra.
- During LLM/RAG work: cosine similarity, embeddings, probability intuition, and evaluation metrics as they arise.
- Classical ML: derivatives, gradients, probability, statistics, optimization, and generalization.
- Deep learning: chain rule, matrix calculus intuition, loss functions, and numerical stability.
- Research: derive the equations that are central to the selected paper.

For each concept: understand the intuition, read the formal definition, solve a small numerical example manually, implement or verify it, and explain it without notes.

---

## 5. Applied AI project standards

A project should demonstrate engineering, not just a successful demo.

For an LLM or RAG project, consider:
- Clear problem statement and intended users.
- Reproducible setup and configuration.
- Input validation and structured output contracts.
- Unit and integration tests.
- A small, versioned evaluation dataset.
- Baseline and explicit quality metrics.
- Failure analysis, including unsupported answers.
- Security and privacy considerations.
- Logging/observability without leaking sensitive content.
- Latency, throughput, and cost measurements.
- Deployment and operational documentation.

Use hosted or local models based on availability, privacy, and cost. Record model/version/configuration so results can be interpreted later.

---

## 6. Experiment-driven practice

Every experiment should have a question, hypothesis, baseline, controlled variables, measurements, results, interpretation, and limitations.

Change one major variable at a time when practical. Repeat measurements when noise matters. A negative result is useful if the setup is sound and the conclusion is appropriately limited.

For research reproductions, distinguish clearly between:
- Reading and understanding a paper.
- Implementing its central method.
- Reproducing a selected experiment.
- Reproducing the full original training/evaluation setup.

These are different levels of evidence.

---

## 7. Research paper reading

Develop paper-reading habits before the dedicated reproduction phase.

**First pass:** title, abstract, introduction, figures, tables, and conclusion. Identify the problem, claimed contribution, and evidence.

**Second pass:** method, equations, architecture, datasets, baselines, and metrics.

**Implementation pass:** map the method to inputs/outputs, tensor shapes, training objectives, and evaluation steps.

**Reproduction pass:** establish a baseline, implement, validate, run controlled experiments, compare results, and document deviations.

Use arXiv and Google Scholar to discover papers, then verify details against the paper, official code, and reliable supplementary material.

---

## 8. Using AI assistants

Use an assistant as a tutor, reviewer, debugging partner, and experiment-design challenger—not as a substitute for independent reasoning.

Before asking for help, make an attempt and state where you are stuck. Prefer hints, critique, edge-case reviews, and explanations. Verify equations, APIs, paper claims, and benchmark interpretations against authoritative sources or experiments. Reimplement important solutions independently after receiving help.

---

## 9. MAANG preparation

Reserve about one hour each week. Rotate among:
- Algorithms and data structures.
- C# standard library, async/await, multithreading, and practical coding.
- System design.
- Senior-level project and leadership stories.

This track complements the AI transition and keeps existing software engineering options open. Prioritize weak areas and interview requirements rather than broad, unfocused study.

---

## 10. Monthly review and job-market feedback

Every four weeks, ask:
1. What can I now build or explain independently?
2. What evidence did I add to the portfolio?
3. Which skill gap most limits the next project or target role?
4. Did the weekly time budget remain realistic?
5. What do current job descriptions repeatedly ask for?
6. What should change next month?

For the near-term job search, compare actual vacancies with demonstrated skills. Separate immediate matches from stretch roles and long-term research roles. Adjust the next project toward recurring market requirements without chasing every new tool.

---

## 11. Final rule

A topic is not mastered because it was watched, read, or copied. It is mastered when you can explain it, apply it, test it, evaluate its behavior, and describe its limitations.

**Build useful AI systems early. Strengthen the mathematics continuously. Reproduce research carefully. Move toward independent contributions through evidence.**
