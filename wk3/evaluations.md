Evaluations

1. **Precision at k (P@k)**:
   - Measures the proportion of relevant documents in the top k results of a search query. High precision at k indicates that the top results are highly relevant.
   - Formula: \( P@k = \frac{\text{Number of relevant documents in top k results}}{k} \)

2. **Recall**:
   - Measures the proportion of relevant documents retrieved out of the total number of relevant documents available. High recall means that the system retrieves most of the relevant documents.
   - Formula: \( \text{Recall} = \frac{\text{Number of relevant documents retrieved}}{\text{Total number of relevant documents}} \)

3. **Mean Average Precision (MAP)**:
   - Computes the average precision for each query and then averages these values over all queries. It provides a single-figure measure of quality across recall levels.
   - Formula: \( \text{MAP} = \frac{1}{|Q|} \sum_{\text{q} \in Q} \text{Average Precision(q)} \)

4. **Normalized Discounted Cumulative Gain (NDCG)**:
   - Measures the usefulness (gain) of a document based on its position in the result list, considering that highly relevant documents appearing lower in the ranking are less useful.
   - Formula: \( \text{NDCG} = \frac{\text{DCG}}{\text{IDCG}} \)
     - \( \text{DCG} = \sum_{i=1}^{p} \frac{2^{\text{rel}_i} - 1}{\log_2(i + 1)} \)
     - \(\text{IDCG}\) is the ideal DCG where documents are perfectly ranked by relevance.

5. **Mean Reciprocal Rank (MRR)**:
   - Evaluates the rank position of the first relevant document. It is useful for queries where finding one relevant document is sufficient.
   - Formula: \( \text{MRR} = \frac{1}{|Q|} \sum_{i=1}^{|Q|} \frac{1}{\text{rank}_i} \)

6. **F1 Score**:
   - Harmonic mean of precision and recall. It balances the two metrics, providing a single score that penalizes extreme values of precision and recall.
   - Formula: \( \text{F1} = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}} \)

7. **Area Under the ROC Curve (AUC-ROC)**:
   - Measures the model's ability to distinguish between relevant and non-relevant documents. An AUC of 1 indicates perfect distinction, while an AUC of 0.5 indicates random performance.
   - AUC is the area under the Receiver Operating Characteristic (ROC) curve, which plots true positive rate (TPR) against false positive rate (FPR).

8. **Mean Rank (MR)**:
   - The average rank of the first relevant document across all queries. Lower values indicate that relevant documents appear higher in the ranking, reflecting better performance.
   - Formula: \( \text{MR} = \frac{1}{|Q|} \sum_{\text{q} \in Q} \text{rank of first relevant document for q} \)

9. **Hit Rate (HR) or Recall at k**:
   - Measures the proportion of queries for which at least one relevant document is retrieved in the top k results. It indicates the likelihood that a user finds a relevant document within the top k results.
   - Formula: \( \text{HR@k} = \frac{\text{Number of queries with at least one relevant document in top k}}{|Q|} \)

10. **Expected Reciprocal Rank (ERR)**:
    - Measures the probability that a user finds a relevant document at each position in the ranked list, assuming a cascading model of user behavior. It considers the diminishing probability of continuing to view lower-ranked documents.
    - Formula: \( \text{ERR} = \sum_{i=1}^{p} \frac{1}{i} \left( \prod_{j=1}^{i-1} (1 - r_j) \right) r_i \)
      - Where \( r_i \) is the relevance probability of the document at position i.