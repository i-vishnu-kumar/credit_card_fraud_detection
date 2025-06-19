# credit_card_fraud_detection

This project focuses on identifying fraudulent credit card transactions using both unsupervised anomaly detection methods and a supervised learning model (XGBoost). The dataset is highly imbalanced, making this a great real-world use case to explore the challenges of fraud detection.

📂 Dataset
	•	Source: Kaggle – Credit Card Fraud Detection
	•	Total transactions: 284,807
	•	Fraudulent transactions: 492 (about 0.17%)
	•	Features: Time, Amount, and PCA-transformed variables (V1–V28)
	•	Target: Class (0 = Normal, 1 = Fraud)

🧪 Objective

To compare and evaluate different machine learning models for fraud detection:
	•	Isolation Forest (Unsupervised)
	•	Local Outlier Factor (Unsupervised)
	•	One-Class SVM (Unsupervised)
	•	XGBoost Classifier (Supervised)

🔍 Exploratory Data Analysis (EDA)
	•	Checked for missing values (None found)
	•	Visualized class imbalance (highly skewed)
	•	Analyzed transaction amounts for fraud and normal cases
	•	Explored patterns between transaction time and amount

💡 Models and Summary

1. Isolation Forest
	•	Unsupervised, tree-based model
	•	Good for imbalanced data
	•	Recall for fraud: 29%
	•	Accuracy: 99.75%

2. Local Outlier Factor (LOF)
	•	Density-based outlier detection
	•	Poor performance on fraud class
	•	Recall for fraud: 2%
	•	Accuracy: 99.66%

3. One-Class SVM
	•	Learns boundary of normal class
	•	High false positive rate
	•	Recall for fraud: 37%, but 0% precision
	•	Accuracy: 70.09%

4. XGBoost Classifier
	•	Supervised gradient boosting model
	•	Best performance overall
	•	Recall for fraud: 57%
	•	Precision: 80%
	•	Accuracy: 99.93%

✅ Key Observations
	•	XGBoost outperforms all other models in both accuracy and fraud detection.
	•	Isolation Forest is the best among the unsupervised methods.
	•	LOF and SVM are not suitable for this highly imbalanced problem without additional tuning.
	•	Precision-recall trade-off is crucial due to the rarity of fraudulent transactions.

📌 Final Notes
	•	Class imbalance is a significant challenge in fraud detection.
	•	Anomaly detection models work without labels but have limited precision.
	•	XGBoost, with labeled data, provides high accuracy and reasonable fraud detection performance.
	•	This project shows that combining EDA, sampling, and choosing the right algorithm can significantly improve model outcomes.
