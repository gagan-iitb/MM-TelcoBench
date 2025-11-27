# MM-TelcoBench
This is the **official GitHub repository** for the paper:
**_MM-Telco: Benchmarks and Multimodal Large Language Models for Telecom Applications_**  
📄 Paper (arXiv): [https://arxiv.org/abs/2511.13131](https://arxiv.org/abs/2511.13131)

## Introduction

MM-Telco is a comprehensive suite of multimodal benchmarks and domain-adapted models designed to evaluate and advance Large Language Models (LLMs) for real-world telecom applications. It includes diverse text and image tasks spanning network operations, troubleshooting, documentation, retrieval, and PCAP-based analysis. Our baseline experiments with leading LLMs and VLMs show significant performance gains when fine-tuned on MM-Telco, while also highlighting key gaps in current multimodal models—offering clear direction for future research in AI-driven telecom intelligence.


## Benchmark Overview

Our benchmark suite covers the following key tasks:

| Task | Evaluation Metrics | Size |
|------|---------------------|---------|
| **5G Faults Multi Correct MCQ (NEW)** | Accuracy | 350 |
| **Multiple-Choice Telecom Question Answering** | Accuracy | 10,000 |
| **Multi-Hop Multi-Choice QA** | Accuracy | 2,000 |
| **Long Telecom Question Answering** | BLEU, ROUGE, BERTScore | 3,000 |
| **Long Telecom Question Answering V2 Multi_hop** | BLEU, ROUGE, SemScore, LLM Judge | 2,500 |
| **Long-Form Telecom Blog QA** | BLEU, ROUGE, BERTScore | 1,000 |
| **Telecom Information Retrieval** | Top-K Accuracy (K=1,3,5) | 1,000 queries, 10,000 docs |
| **Named Entity Recognition (NER)** | Accuracy | 1,000 entities |
| **Named Entity Type Classification** | Accuracy | 1,000 |
| **Scenario-Based Filter Generation (Wireshark Filters)** | BLEU, ROUGE, SemScore, LLM Judge | 500 |
| **Image-based Multi-Choice QA** | Accuracy | 2,000 |
| **Image Caption Generation** | BLEU, ROUGE, SemScore | 1,000 images |
| **Image-Based Long QA** | BLEU, ROUGE, BERTScore | 1,000 |
| **Image Classification** | Accuracy | 1,000 |
| **Image Retrieval** | Top-K Accuracy | 1,000 queries, 3,000 images |


### 1. Multiple-Choice Telecom Question Answering
Evaluates factual telecom knowledge using MCQs generated from 3GPP clauses via an agentic refinement pipeline.

### 2. Multi-Hop Multi-Choice QA
Tests multi-step reasoning across multiple 3GPP documents through globally referenced subclauses.

### 3. Long Telecom Question Answering
Assesses the ability to generate coherent, detailed explanations using multi-subclause context.

### 4. Long-Form Telecom Blog QA
Evaluates high-level conceptual telecom understanding using questions generated from popular blog content.

### 5. Information Retrieval
Measures telecom-specific embedding quality by checking Top-K retrieval of relevant specification sections.

### 6. Named Entity Type Classification
Tests classification of telecom entities into SME-defined domain-specific categories.

### 7. Scenario-Based Filter Generation
Evaluates troubleshooting skill by selecting correct Wireshark filters for telecom PCAP scenarios.

### 8. Image-Based Multiple Choice Questions
Assesses understanding of telecom diagrams using MCQs generated from structured image descriptions.

### 9. Image-Based Long Answer Questions
Tests the ability to provide detailed explanations of complex telecom diagrams.

### 10. Image Retrieval
Evaluates multimodal alignment by retrieving correct telecom diagrams for structured technical queries.

### 11. Image Caption Generation
Measures the ability to generate accurate captions for telecom diagrams using 3GPP reference captions.

### 12. Image Classification
  Classification of telecom-related images (e.g., packet structure, network architecture, and call ladder/flow diagrams) into predefined categories.


## Areas Covered
Our benchmarks comprehensively span all major domains defined in the 3GPP Release 17 Technical Specifications. This includes core network protocols, system architecture and services, radio resource control, radio performance, and protocol aspects across RAN, SA, and CT working groups. Additionally, the benchmarks cover user equipment procedures, service management and orchestration, network security and privacy, and interworking with external networks and policy control. Together, these areas capture the full breadth of Release 17 radio access and core network functionalities, ensuring that the benchmark reflects real-world telecom challenges across both protocol-level and system-level dimensions.

## Why This Benchmark?

Current benchmarks are not designed to evaluate LLMs within the context of real-world telecom tasks. Our benchmark addresses this by offering:

- **Telecom-Specific Tasks**: Tailored to 3GPP specifications, providing a more realistic evaluation of LLMs' domain proficiency.
- **Multi-Modal Evaluation**: Covers both textual and visual data, ensuring comprehensive assessment across different data modalities.
- **PCAP Analysis for RCA & 5G Faults**: Includes Packet Capture–based troubleshooting tasks focused on root cause analysis and 5G network faults—an area missing from existing open benchmarks.
- **Open Source**: The dataset is freely available, encouraging community collaboration and model evaluation on a large, diverse dataset.


## Interested in Collaborating ? 
- We invite you to help validate our benchmark and contribute to future developments. Please fill out this [expression of interest form](https://docs.google.com/forms/d/e/1FAIpQLSdt5PiCNI3dCf9Vw9jfjSMbpyfQPfyJhnAXF1MEcoWsCFEfPA/viewform?usp=sf_link).

  
## Future Work 
- **LLMs Evaluation**: We will evaluate some of the state-of-the-art LLMs on these benchmarks and share the results and analysis of their strengths and weakness.
- **Finetune Shortlisted Models**: We will Try to increase the performance of the best-performing models on our benchmark using fine-tuning.
- **Large Benchmark Release**: We will release a large version of these Benchmarks soon.

## People/Collaborators
* Dr. Gagan Raj Gupta, Associate Professor, IIT Bhilai (ex. LMTS, AT&T Labs, CA, USA)
* Dr. Brejesh Lall, Professor, IIT Delhi
* Dr. Ashutosh Modi, Associate Professor, IIT Kanpur
* Dr. Abdelaali CHAOUB, Associate Professor, INPT
* Dr. Soumajit Pramanik, Assistant Professor, IIT Bhilai

* Anshul Kumar (MTech, Jawaharlal Nehru University)
* Manish Rai (MTech, IIT Bhilai)
* Yashwant Holla (MTech, IIT Kanpur)
* Moyank Giri (MTech, IIT Bhilai)
* Apu Chakraborty 
* Sunny Kumar
* M V Kiran Sooraj

## License

This benchmark is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
