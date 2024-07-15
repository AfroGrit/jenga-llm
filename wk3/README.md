# Vector search

- **Introduction to Vector Search and Semantic Search:** The session begins by explaining vector databases and their role in semantic search, illustrated with examples like how Google distinguishes between "Apple" as a company and "apple" as a fruit.

- **Rise of Vector Databases:** The popularity of vector databases is attributed to the explosion of diverse data types (text, images, audio) and the limitations of classical databases, which are less effective for handling such data.

- **Vector Embeddings:** Vector embeddings are numerical representations of data capturing relationships and meanings. These embeddings are created through a process involving data collection, preprocessing, and model training to generate meaningful vectors.

- **Functionality of Vector Databases:** Vector databases store and index large amounts of data to optimize search and retrieval processes. They allow for efficient semantic searches by comparing vector similarities using techniques like cosine similarity and dot product.

- **Applications and Future Lab Session:** Vector databases are useful for semantic search, personalized recommendations, and text generation. The next session will include a lab exercise to set up a semantic search engine using Elastic Search, applying the concepts discussed.

#### building a semantic search engine with Elasticsearch:

- **Embedding Generation**: Use the `sentence-transformers` package to create embeddings from the documents. These embeddings are dense vector representations of the documents that will be indexed for semantic search.

- **Elasticsearch Configuration**: Set up Elasticsearch by creating an index with mappings that define how documents and fields are stored and queried. The index uses similarity metrics like cosine similarity to match search queries with documents.

- **Search and Query**: Implement a search functionality where user queries are converted to vectors and matched against indexed documents. Results are ranked by relevance scores, similar to how search engines like Google operate.

These steps outline the process of setting up a semantic search engine from data preparation to search query execution using Elasticsearch.

#### Refences
- https://logz.io/blog/elasticsearch-mapping/#:~:text=Within%20a%20search%20engine%2C%20mapping,indexes%20and%20stores%20its%20fields
- https://www.sbert.net/docs/sentence_transformer/pretrained_models.html
- https://www.elastic.co/search-labs/tutorials
- https://www.elastic.co/search-labs/blog/text-similarity-search-with-vectors-in-elasticsearch
