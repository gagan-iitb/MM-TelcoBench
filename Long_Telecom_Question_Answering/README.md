# Long Telecom Question Answering

This dataset focuses on **long-form question answering**, where each question is accompanied by three candidate responses. The responses are evaluated based on their best match using the **BLEU**, **ROUGE**, and **BERTScore** metrics, providing a comprehensive assessment of the model’s ability to generate coherent and contextually accurate answers in the telecommunications domain.

## Dataset Structure

The dataset is stored in a CSV file containing the following fields:
- **Question**: The long-form question derived from 3GPP technical specifications.
- **Candidate Answer 1**: First possible long-form response to the question.
- **Candidate Answer 2**: Second possible long-form response.
- **Candidate Answer 3**: Third possible long-form response.

### Example Entry

- **Question**: How does the eNodeB measure and store the maximum E-RAB setup time per Quality of Service Class Identifier (QCI) during a granularity period, and what is the significance of reinitializing the gauge at the beginning of each granularity period in the context of packet-switched networks?

  - **Candidate Answer 1**: The eNodeB measures the maximum E-RAB (Evolved Radio Access Bearer) setup time per Quality of Service Class Identifier (QCI) by monitoring the time intervals between the receipt of an E-RAB SETUP REQUEST or INITIAL CONTEXT SETUP REQUEST message and the transmission of the corresponding E-RAB SETUP RESPONSE or INITIAL CONTEXT SETUP RESPONSE message. This measurement is recorded for each successfully established E-RAB. The highest recorded time within a granularity period is stored in a gauge. Reinitializing the gauge at the beginning of each granularity period ensures that the measurement reflects the current network performance and conditions, allowing for accurate and up-to-date monitoring of the network's ability to establish E-RABs efficiently. This is particularly important in packet-switched networks where timely and reliable data transmission is critical for maintaining quality of service.

  - **Candidate Answer 2**: The eNodeB captures the maximum E-RAB setup time per QCI by tracking the duration from the receipt of an E-RAB SETUP REQUEST or INITIAL CONTEXT SETUP REQUEST to the transmission of the corresponding E-RAB SETUP RESPONSE or INITIAL CONTEXT SETUP RESPONSE. This duration is measured for each E-RAB that is successfully established. The highest value recorded during a granularity period is stored in a gauge. Reinitializing the gauge at the start of each granularity period is significant because it resets the measurement, ensuring that the data collected is relevant to the current period. This practice helps in identifying and addressing any performance issues promptly, thereby maintaining the quality of service in packet-switched networks where data transmission efficiency is paramount.

  - **Candidate Answer 3**: The eNodeB measures the maximum E-RAB setup time per QCI by calculating the time taken from receiving an E-RAB SETUP REQUEST or INITIAL CONTEXT SETUP REQUEST to sending the corresponding E-RAB SETUP RESPONSE or INITIAL CONTEXT SETUP RESPONSE. This measurement is done for each successfully established E-RAB, and the highest time recorded within a granularity period is stored in a gauge. The significance of reinitializing the gauge at the beginning of each granularity period lies in its ability to provide a fresh start for measurements, ensuring that the data reflects the most recent network performance. This is crucial in packet-switched networks, where maintaining up-to-date performance metrics is essential for optimizing network operations and ensuring that quality of service requirements are consistently met.

## Metadata

Each question in the dataset is accompanied by the following metadata:
- **Source**: The 3GPP Technical Specification (TS) document from which the question and candidate answers are derived.
- **Section**: The specific section of the TS document used to generate the question.
- **Working Group**: The 3GPP Working Group responsible for the TS document.
- **Series**: The 3GPP series to which the Working Group belongs.

This metadata provides essential traceability, linking each question back to its originating 3GPP documentation, making this dataset a valuable resource for benchmarking models in telecom-specific question answering tasks.

## Evaluation

The candidate answers are evaluated using the following metrics:
- **BLEU**: Measures the overlap of n-grams between the generated answer and the ground truth.
- **ROUGE**: Assesses the recall and precision of word matches between the generated answer and the reference answer.
- **BERTScore**: Uses contextual embeddings to determine the similarity between the generated answer and the reference answer.

This dataset is designed to challenge models' abilities to generate detailed and contextually accurate responses in the telecom domain.


## Evaluation results for SOTA models 

| **ROUGE-L** | CT WG1 | CT WG3 | CT WG4 | RAN1 | RAN2 | RAN3 | RAN4 | SA WG1 | SA WG2 | SA WG3 | SA WG5 | Average |
|-------------|---------|---------|---------|-------|-------|-------|-------|---------|---------|---------|---------|----------|
| Gemma2 9B | 0.24 | 0.23 | 0.23 | 0.21 | 0.21 | 0.22 | 0.20 | 0.16 | 0.20 | 0.20 | 0.21 | 0.21 |
| Gemma2 27B | 0.27 | 0.24 | 0.26 | 0.22 | 0.23 | 0.24 | 0.22 | 0.18 | 0.23 | 0.23 | 0.23 | 0.24 |
| Llama 3.2 3B | 0.27 | 0.24 | 0.25 | 0.25 | 0.23 | 0.25 | 0.24 | 0.20 | 0.23 | 0.23 | 0.23 | 0.24 |
| Llama 3.1 8B | 0.269 | 0.261 | 0.26 | 0.23 | 0.245 | 0.251 | 0.253 | 0.223 | 0.246 | 0.246 | 0.24 | 0.25 |

| **BERTSCORE (F1)** | CT WG1 | CT WG3 | CT WG4 | RAN1 | RAN2 | RAN3 | RAN4 | SA WG1 | SA WG2 | SA WG3 | SA WG5 | Average |
|--------------------|---------|---------|---------|-------|-------|-------|-------|---------|---------|---------|---------|----------|
| Gemma2 9B | 0.610 | 0.610 | 0.609 | 0.590 | 0.60 | 0.63 | 0.59 | 0.58 | 0.60 | 0.59 | 0.60 | 0.606 |
| Gemma2 27B | 0.628 | 0.624 | 0.623 | 0.603 | 0.62 | 0.637 | 0.611 | 0.59 | 0.62 | 0.61 | 0.621 | 0.62 |
| Llama 3.2 3B | 0.647 | 0.643 | 0.638 | 0.641 | 0.637 | 0.66 | 0.638 | 0.617 | 0.639 | 0.628 | 0.641 | 0.638 |
| Llama 3.1 8B | 0.65 | 0.655 | 0.644 | 0.634 | 0.647 | 0.66 | 0.646 | 0.638 | 0.649 | 0.64 | 0.646 | 0.647 |

| **BLEU** | CT WG1 | CT WG3 | CT WG4 | RAN1 | RAN2 | RAN3 | RAN4 | SA WG1 | SA WG2 | SA WG3 | SA WG5 | Average |
|----------|---------|---------|---------|-------|-------|-------|-------|---------|---------|---------|---------|----------|
| Gemma2 9B | 7.44 | 6.02 | 7.0 | 6.5 | 4.5 | 5.6 | 6.4 | 3.5 | 5.1 | 5.52 | 5.63 | 5.84 |
| Gemma2 27B | 9.42 | 6.53 | 8.62 | 6.57 | 6.7 | 6.55 | 7.65 | 4.47 | 6.91 | 7.02 | 6.81 | 7.34 |
| Llama 3.2 3B | 10.0 | 7.39 | 9.05 | 9.43 | 7.29 | 8.07 | 9.68 | 5.97 | 7.8 | 7.77 | 7.7 | 8.2 |
| Llama 3.1 8B | 10.17 | 8.7 | 8.07 | 7.82 | 8.07 | 7.86 | 10.23 | 7.29 | 8.34 | 8.49 | 8.37 | 8.75 |

**Score Interpretations:**
- **ROUGE-L**: A score of 0.3 and above indicates that a fair portion of the reference content has been captured. Higher scores (>0.5) are good for long-form tasks, reflecting better content overlap.
- **BERTScore (F1)**: Scores around 0.6 or higher show strong semantic similarity between the generated and reference text. Anything above 0.7 suggests very high-quality responses.
- **BLEU**: For long-answer questions, scores between 10–20 are considered good. Higher scores (above 30) are excellent, especially when the task involves exact or near-exact matches to the reference.
