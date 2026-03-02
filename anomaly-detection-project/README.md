Credit Card Fraud Detection – Anomaly Detection:

1. Overview

   Unsupervised anomaly detection project on a highly imbalanced credit card transaction dataset (fraud rate ≈ 0.17%).

   Compared multiple anomaly detection algorithms and evaluated performance using Precision-Recall AUC and F1-score.

   Credit Card Fraud Detection – Anomaly Detection

2. Dataset

   284,807 transactions

   492 fraud cases

   Fraud rate ≈ 0.0017

   PCA-transformed features (V1–V28) + Time + Amount

3. Models Implemented

   Isolation Forest:
      Tree-based anomaly detection
      Scales well to large datasets
      Produces anomaly scores for ranking

   Local Outlier Factor (LOF)
      Density-based anomaly detection
      Sensitive to high dimensionality
      Used with PCA for dimensionality reduction

   DBSCAN
      Density-based clustering
      Noise points treated as anomalies
      Does not produce continuous anomaly scores

   Isolation Forest trained on full dataset.
   LOF and DBSCAN trained on 50k sample for scalability.

4. Evaluation Strategy

   Used PR-AUC to measure ranking performance (suited for imbalanced data)
   Selected optimal decision threshold using F1-score
   Compared precision, recall, and F1 at chosen threshold

5. Results
   Model	           Precision	Recall	F1	    PR-AUC
   Isolation Forest	   0.248	    0.507	0.333	0.227
   LOF	               0.064	    0.440	0.111	0.029
   DBSCAN	           0.016	    0.840	0.032	—

6. Conclusion:
Isolation Forest performed best, achieving strong ranking ability and balanced precision-recall tradeoff.

