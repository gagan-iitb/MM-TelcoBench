# MM-TelcoBench

## Introduction

The telecommunications industry is undergoing significant transformation, driven by advancements in Large Language Models (LLMs) and Generative AI. Despite these technological breakthroughs, the sector lacks specialized benchmarks to evaluate the proficiency of these models in telecom-specific tasks. In contrast to fields like medicine and finance, which have well-established domain-specific benchmarks, telecommunications still requires tailored datasets that can effectively assess Large Language Models performance on industry-relevant tasks.

## Benchmark Overview

Our benchmark suite covers the following key tasks:

| Task | Evaluation Metrics |
|------|---------------------|
| Multiple-Choice Telecom Question Answering | Accuracy |
| Long Telecom Question Answering | BLEU, ROUGE, BERTScore |
| Telecom Information Retrieval | Top-K Accuracy (K=1, 3, 5) |
| Named Entity Recognition | Accuracy |
| Image Classification | Accuracy |
| Image Retrieval | Top-K Accuracy |

### 1. Multiple-Choice Telecom Question Answering

- **Description**: A dataset comprising complex multiple-choice questions extracted from 3GPP specification documents. The questions are designed to challenge domain-specific understanding with closely related options.
- **Evaluation Metric**: Accuracy

### 2. Long Telecom Question Answering

- **Description**: Long-form question answering task where models provide responses to telecom questions, evaluated on their coherence and contextual accuracy. Each question comes with three candidate answers.
- **Evaluation Metrics**: BLEU, ROUGE, BERTScore

### 3. Telecom Information Retrieval

- **Description**: Focuses on retrieving relevant sections from 3GPP documents based on queries.
- **Evaluation Metric**: Top-K Accuracy (K=1, 3, 5)

### 4. Named Entity Recognition (NER)

- **Description**: Enhances entity type coverage from 3GPP documents. The goal is to evaluate the model's ability to accurately identify and categorize telecom-specific entities.
- **Evaluation Metric**: Accuracy

### 5. Image Classification

- **Description**: Classification of telecom-related images (e.g., packet structure, network architecture, and call ladder/flow diagrams) into predefined categories.
- **Evaluation Metric**: Accuracy

### 6. Image Retrieval

- **Description**: Retrieval of the most relevant image from a database based on user queries. The dataset consists of <image, query> pairs from 3GPP specification documents.
- **Evaluation Metric**: Top-K Accuracy

## Why This Benchmark?

Current benchmarks are not designed to evaluate LLMs within the context of real-world telecom tasks. Our benchmark addresses this by offering:

- **Telecom-Specific Tasks**: Tailored to 3GPP specifications, providing a more realistic evaluation of LLMs' domain proficiency.
- **Multi-Modal Evaluation**: Covers both textual and visual data, ensuring comprehensive assessment across different data modalities.
- **Open Source**: The dataset is freely available, encouraging community collaboration and model evaluation on a large, diverse dataset.

## License

This benchmark is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
