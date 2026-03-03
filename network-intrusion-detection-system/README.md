Network Intrusion Detection System

1. Overview

This project builds and compares supervised and unsupervised machine learning models for detecting anomalous network traffic.
The goal is to evaluate model performance under a realistic intrusion detection scenario with ~5% anomaly rate.

The study highlights the performance trade-offs between classification-based and anomaly-based detection approaches.


2. Dataset

Network traffic dataset with labeled classes:
   normal
   anomaly

Imbalanced distribution (~95% normal, ~5% anomalies)
Tabular feature set including numerical and categorical variables
To simulate realistic intrusion detection conditions, anomaly samples were intentionally reduced to create a 95–5 imbalance ratio.

3. Preprocessing Pipeline

Train–validation split (no data leakage)
One-hot encoding for categorical features
Standard scaling for numerical features
PCA (95% variance retained) for LOF to mitigate high-dimensional effects
Normal-only training for anomaly detection models (IsolationForest, LOF, Autoencoder)

4. Models Implemented
🔹 Supervised Models
        RandomForest
        XGBoost

🔹 Unsupervised / Semi-Supervised Models
        IsolationForest
        Local Outlier Factor (LOF)
        Autoencoder (trained on normal data only)

5. Evaluation Metrics

Since the dataset is imbalanced, evaluation focused on:
    Precision
    Recall
    F1-score
    ROC-AUC
    PR-AUC (primary metric)

6. Results Summary

    Model	         PR-AUC	     Key Observation
    RandomForest	~0.999	   Best overall performance
    XGBoost	        ~0.999	   Comparable to RF
    IsolationForest	~0.90	   Strong unsupervised ranking ability
    Autoencoder	    ~0.88	   Balanced detection capability
    LOF (with PCA)	~0.60	   Sensitive to high-dimensional data
    
7. Key Insights

Supervised models significantly outperform unsupervised methods when labeled data is available.
IsolationForest is more robust than density-based LOF in high-dimensional network data.
PCA improves LOF performance by mitigating curse-of-dimensionality effects.
Autoencoders can detect deviations from normal traffic but are sensitive to threshold selection.
Unsupervised models remain useful for detecting unseen or zero-day attack patterns.

8. Tech Stack

Python
Scikit-learn
XGBoost
TensorFlow / Keras
Pandas, NumPy
Matplotlib, Seaborn


