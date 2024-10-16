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
