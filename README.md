# Fraud-Detection-in-Financial-Transactions
### Problem
Identifying fraudulent transactions is a crucial yet complex task within contemporary financial systems. Traditional supervised machine learning methods depend on datasets where fraudulent and legitimate transactions are distinctly labeled. However, in practical applications, such labeled data is often scarce, significantly imbalanced, or not available at all. This situation calls for unsupervised techniques capable of detecting anomalies without pre-existing label information. The primary challenge lies in accurately identifying fraudulent activities while minimizing false positives and ensuring the model's scalability for large datasets. Models typically underperform on datasets with severe class imbalance, where one class represents a tiny fraction of the data.
### Solution
To tackle this issue, we employed the KMeans model, foregoing the use of labeled data for training purposes. Labeled data was utilized solely for preprocessing. Our approach involved:
- Selecting features that distinctly differed between the two classes,
- Reducing the volume of class 0 data to achieve a more balanced dataset,
- Training the model on this balanced dataset without supervision,
- Testing the model on the complete, highly imbalanced dataset, achieving a precision of 0.86 and a recall of 0.76 for class 1 (fraudulent transactions) recognition.

This method aligns with practices highlighted in various studies, such as those discussing the benefits of unsupervised learning in fraud detection source, and emphasizes the importance of preprocessing to balance datasets for improved model performance source.
