# Multiple-Choice Telecom Question Answering

This dataset comprises multiple-choice questions derived from **3GPP specification documents**. The questions are designed to be complex, with closely related options to rigorously assess domain-specific knowledge and performance in telecommunications. The **primary evaluation metric** for this dataset is accuracy.

## Dataset Structure

The dataset is stored in a CSV file containing the following fields:
- **Question**: The multiple-choice question derived from 3GPP technical specifications.
- **Option 1**: First possible answer.
- **Option 2**: Second possible answer.
- **Option 3**: Third possible answer.
- **Option 4**: Fourth possible answer.
- **Answer**: The correct option (e.g., Option 2).
- **Explanation**: A detailed explanation of why the correct answer was chosen, providing context from the 3GPP standards.

### Example Entry

- **Question**: What is the primary purpose of collecting information related to energy consumption and efficiency in a 5G system?
  - **Option 1**: To optimize network security
  - **Option 2**: To enable network internal optimization and facilitate service adjustments for third-party services
  - **Option 3**: To improve user equipment battery life
  - **Option 4**: To enhance Quality of Service (QoS) for specific applications
- **Answer**: Option 2
- **Explanation**: Collecting information on energy consumption and efficiency is crucial for optimizing the network's internal operations, as well as enabling third-party services to make informed decisions about their service adjustments. This aligns with the concept of a more open and collaborative 5G ecosystem, where data sharing can drive mutual benefits.

## Metadata

Each question in the dataset is accompanied by the following metadata:
- **Source**: The 3GPP Technical Specification (TS) document from which the question and answers are derived.
- **Section**: The specific section of the TS document used to generate the question.
- **Working Group**: The 3GPP Working Group responsible for the TS document.
- **Series**: The 3GPP series to which the Working Group belongs.

This metadata ensures traceability and relevance by linking each question back to its originating 3GPP documentation, making it a valuable resource for benchmarking and testing in telecom-specific tasks.

## Usage

The dataset is intended to evaluate the ability of models to understand and answer complex telecom-related questions, providing a challenging benchmark for **Multiple-Choice Question Answering** in the telecom domain.


## Evaluation Result for some state-of-the-art models

| Model Name | CT WG1 | CT WG3 | CT WG4 | RAN1 | RAN2 | RAN3 | RAN4 | SA WG1 | SA WG2 | SA WG3 | SA WG5 | Overall Accuracy |
|------------|--------|--------|--------|-------|-------|-------|-------|---------|---------|---------|---------|-----------------|
| Gemma2 9B | 76.1 | 80.7 | 81.2 | 46.6 | 71.8 | 80.0 | 66.6 | 82.5 | 82.7 | 73.3 | 81.2 | 77.49 |
| Gemma2 27B | 76.3 | 79.3 | 74.6 | 62.5 | 73.2 | 69.2 | 56.6 | 78.6 | 83.6 | 75.6 | 80.0 | 77.39 |
| Llama 3.2 3B | 66.3 | 71.4 | 65.2 | 58.3 | 60.3 | 61.5 | 52.8 | 76.6 | 79.1 | 59.7 | 67.5 | 68.58 |
| Llama 3.1 8B | 70.0 | 73.0 | 65.9 | 62.5 | 68.0 | 76.9 | 50.9 | 77.2 | 81.8 | 61.8 | 70.0 | 71.91 |
| Llama 3.1 70B | 79.7 | 76.1 | 72.4 | 66.6 | 75.5 | 73.0 | 54.7 | 83.4 | 84.5 | 75.1 | 82.5 | 78.89 |
| Nemotron | 80.7 | 71.4 | 74.6 | 66.6 | 77.4 | 76.9 | 56.6 | 84.4 | 86.9 | 79.3 | 84.1 | 80.69 |
| GPT-4o | 82.8 | 84.1 | 83.3 | 66.6 | 82.8 | 84.6 | 64.1 | 86.4 | 88.7 | 82.5 | 85.0 | 84.14 |
| GPT-4o-mini | 83.2 | 84.1 | 83.3 | 66.6 | 82.0 | 80.0 | 62.2 | 86.4 | 88.9 | 82.0 | 85.8 | 84.09 |
| Aya-Expanse:32B | 67.7 | 71.4 | 67.15 | 66.66 | 70.22 | 57.69 | 50.04 | 79.61 | 81.58 | 66.66 | 75.0 | 72.27 |
| IMB granite3 dense 8B | 52.8 | 60.3 | 57.24 | 58.33 | 56.1 | 57.69 | 45.28 | 69.9 | 65.0 | 53.43 | 68.33 | 58.91 |
