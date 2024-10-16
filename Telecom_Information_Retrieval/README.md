# Telecom Information Retrieval

This task focuses on **query-based retrieval** of relevant sections from 3GPP documents. The goal is to evaluate how effectively models can retrieve pertinent sections based on given queries. The evaluation is conducted using **Top-K accuracy**, with K values set at 1, 3, and 5. These metrics assess the retrieval process's ability to identify the most relevant sections from the documents.

## Dataset Structure

The dataset is organized into three main files:
- **Queries**: Contains the query text derived from 3GPP documents.
- **Documents**: Contains the sections of the 3GPP documents that serve as potential retrieval targets.
- **Qrels**: Provides the relevance judgments, mapping each query (by query ID) to its corresponding document (by document ID).

Each query has a single document mapped to it, ensuring a clear relevance link between the query and the document. The queries themselves are generated based on the contents of the associated documents.

## Metadata

The metadata for each query and document includes:
- **Source**: The 3GPP Technical Specification (TS) document from which the query and document are derived.
- **Section**: The specific section of the TS document used for generating the queries and the corresponding relevant document.
- **Working Group**: The 3GPP Working Group responsible for the TS document.
- **Series**: The 3GPP series to which the Working Group belongs.

This metadata provides essential context and traceability, ensuring that each query and document pair is accurately linked back to its original source.

## Evaluation

The evaluation is performed using **Top-K accuracy** at K=1, K=3, and K=5. This metric measures the system’s ability to retrieve the correct document within the top K results, where:
- **Top-1 Accuracy**: Measures if the most relevant document is retrieved as the top result.
- **Top-3 Accuracy**: Measures if the relevant document is within the top 3 retrieved results.
- **Top-5 Accuracy**: Measures if the relevant document is within the top 5 retrieved results.

This task is designed to challenge retrieval models' effectiveness in identifying the most relevant sections from highly technical telecommunications documents.
