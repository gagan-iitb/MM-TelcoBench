## 5G Faults Multi-Correct MCQs (New Addition)

### Motivation
This benchmark introduces **multi-correct MCQs** for 5G fault diagnosis, addressing a key limitation of traditional single-correct-option MCQs. Since LLMs are probabilistic, they may guess the correct option without true understanding. By introducing **multiple correct answers out of 6 options**, we significantly increase evaluation rigor and reduce the chance of accidental correctness.

### Task Creation Process
A different MCQ generation approach was used for this dataset:

1. The 5G faults dataset contained multiple valid solutions per scenario, so questions were designed with **6 options** instead of 4, and **multiple correct answers**.
2. Instead of using generic or weak distractors produced during MCQ generation, incorrect options were created using a separate distractor-generation pipeline:
   - An LLM was prompted to generate **three types of distractor errors**:
     - *Concept-based errors*
     - *Reason-based errors*
     - *Telecom-bias-based errors*
   - Each type produced multiple distractors separately using the question and correct answers as context.
   - A second LLM was then used to **select the best distractors** from all generated candidates to maximize difficulty.
3. Questions and options were generated using **Qwen3 32B**, ensuring high-quality telecom-specific reasoning.

This pipeline creates highly challenging multi-correct MCQs optimized for robust telecom competence evaluation.

### Skills Tested
Evaluates the model’s ability to perform **deep reasoning**, validate multiple correct interpretations, and avoid subtle conceptual, causal, and telecom-domain-specific errors.


### Model Performance Summary

| Model | Accuracy |
|-------|----------|
| Llama 3.2 3B | 12.04 |
| Llama 3.1 8B | 31.65 |
| Phi-4 14B | 41.45 |
| Phi-4 14B (Reasoning) | 37.53 |
| Qwen3 8B (Reasoning) | 47.60 |
| Qwen3 32B (Reasoning) | 54.62 |
| Qwen2.5 7B | 41.45 |

### Key Observation
Despite using Qwen3 32B to generate the dataset, results show **no generation-model bias**—other models do not perform disproportionately better or worse, confirming the fairness and robustness of the benchmark design.
