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
