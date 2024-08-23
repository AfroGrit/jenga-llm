# Vector search

- **Introduction to Vector Search and Semantic Search:** The session begins by explaining vector databases and their role in semantic search, illustrated with examples like how Google distinguishes between "Apple" as a company and "apple" as a fruit.

- **Rise of Vector Databases:** The popularity of vector databases is attributed to the explosion of diverse data types (text, images, audio) and the limitations of classical databases, which are less effective for handling such data.

- **Vector Embeddings:** Vector embeddings are numerical representations of data capturing relationships and meanings. These embeddings are created through a process involving data collection, preprocessing, and model training to generate meaningful vectors.

- **Functionality of Vector Databases:** Vector databases store and index large amounts of data to optimize search and retrieval processes. They allow for efficient semantic searches by comparing vector similarities using techniques like cosine similarity and dot product.

- **Applications and Future Lab Session:** Vector databases are useful for semantic search, personalized recommendations, and text generation. The next session will include a lab exercise to set up a semantic search engine using Elastic Search, applying the concepts discussed.

### building a semantic search engine with Elasticsearch:

- **Embedding Generation**: Use the `sentence-transformers` package to create embeddings from the documents. These embeddings are dense vector representations of the documents that will be indexed for semantic search.

- **Elasticsearch Configuration**: Set up Elasticsearch by creating an index with mappings that define how documents and fields are stored and queried. The index uses similarity metrics like cosine similarity to match search queries with documents.

- **Search and Query**: Implement a search functionality where user queries are converted to vectors and matched against indexed documents. Results are ranked by relevance scores, similar to how search engines like Google operate.

### Evaluation Metrics for Retrieval:

- **Overview of Evaluation in Retrieval Systems**:
  The video introduces the concept of evaluating search results in retrieval systems, which includes various methods such as Min search, Elastic search, and Vector search, emphasizing that the best method depends on data and requirements.

- **Importance of Evaluation Metrics**:
  The use of evaluation metrics is crucial for assessing the effectiveness of retrieval methods. These metrics help determine how well a search system performs by comparing its results against a gold standard or ground truth dataset.

- **Gold Standard Data Sets**:
  A gold standard dataset is essential for evaluation. It consists of queries and corresponding relevant documents. The video discusses generating this dataset using an LLM (large language model) when a production system is not available.

- **Common Evaluation Metrics for Ranking**:
  The video covers common evaluation metrics for ranking search results, including metrics like **Hit Rate** and **Mean Reciprocal Rank (MRR)**. These metrics help evaluate how well the retrieval system ranks relevant documents.

- **Next Steps in the Series**:
  The next part of the series will delve into how to create a gold standard dataset using an LLM and further explore various evaluation metrics, with explanations available in a future video.

### Ground Truth Dataset Generation for Retrieval Evaluation"

- **Importance of Ground Truth Datasets**: The video discusses the significance of creating a ground truth or gold standard dataset for evaluating retrieval results. This dataset includes many queries and their corresponding relevant documents, helping to measure the effectiveness of retrieval techniques.

- **Simplified Approach for Dataset Creation**: Instead of a complex setup with multiple relevant documents per query, the video demonstrates a simpler method where each query has one relevant document. This involves generating a set of queries from FAQ records and mapping them to their relevant answers.

- **Methods for Creating Ground Truth Data**: The video covers various methods for creating such datasets, including manual annotation by experts, user observation, and using language models (LLMs). The focus is on using LLMs to automate the generation of queries and evaluate retrieval performance.

- **Document ID Management**: The video explains challenges in assigning unique IDs to documents and proposes solutions. One method involves using content-based hashes for IDs, while acknowledging issues with hash collisions and proposing a practical approach to handle these problems.

- **Generating and Saving Data**: The process involves generating user questions using a prompt template, creating a dataset with these questions, and saving the results to a CSV file. This data is then used to test and refine retrieval techniques in search systems.



#### Refences
- https://logz.io/blog/elasticsearch-mapping/#:~:text=Within%20a%20search%20engine%2C%20mapping,indexes%20and%20stores%20its%20fields
- https://www.sbert.net/docs/sentence_transformer/pretrained_models.html
- https://www.elastic.co/search-labs/tutorials
- https://www.elastic.co/search-labs/blog/text-similarity-search-with-vectors-in-elasticsearch
