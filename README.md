# Fraud Detection in Financial Transactions
### Problem
Detecting fraudulent transactions is a critical yet challenging task in modern financial systems. Traditional supervised machine learning methods rely on datasets where fraudulent and legitimate transactions are explicitly labeled. However, in real-world applications, such labeled data are often scarce, highly imbalanced, or entirely unavailable. This necessitates the use of unsupervised and semi-supervised methods capable of detecting anomalies without prior label information. The core challenge lies in accurately identifying fraudulent activity while minimizing false positives and ensuring model scalability for large datasets. Models typically underperform on datasets with severe class imbalance, where one class (e.g., fraud) represents a tiny fraction of the data.
### Solution
In this work, we aim to identify optimal anomaly detection tools for highly imbalanced data across three learning paradigms:
#### Unsupervised Learning: 
Models are trained on unlabeled data (containing both normal and anomalous transactions). However, labeled data will be partially utilized to:

Specify the assumed proportion of anomalies (contamination parameter).
Select the most informative features.
Determine the decision threshold between anomalies and normal transactions.

#### Semi-Supervised Learning: 
Models are trained exclusively on normal transactions, with no exposure to anomalous data during training.

#### Supervised Learning: 
Models leverage fully labeled datasets containing both normal and fraudulent transactions.

In this work We also investigate the impact of low-information features on prediction performance and the effect of feature reduction (noise reduction) on model outcomes.
### Data Strategy
The dataset will be split into three subsets: training, validation, and test sets. The anomaly ratio (0.1727%) will be preserved across all splits to reflect real-world class imbalance. Maintaining this imbalance is critical, as artificially reducing class imbalance artificially inflates performance metrics. For instance, experiments show that increasing the anomaly ratio by ~5x (to 0.85%) improves the F1-score of a Multivariate Gaussian model from 0.5 to 0.8.
### Evaluation Framework
For each learning paradigm, we will:

Test one benchmark model (selected based on prior performance for the given paradigm and dataset) and evaluate a neural network architecture.

Compare performance metrics (precision, recall, F1-score).

Quantify the effect of feature selection on prediction accuracy.