Breast Cancer Classification using Machine Learning
📌 Project Description
This project builds and evaluates multiple machine learning classification models to predict whether a breast tumor is Malignant (Cancerous) or Benign (Non-Cancerous) using medical diagnostic features.
The system is designed to support doctors by comparing single machine learning models with an ensemble learning approach to identify the most reliable model for real-world medical use.
📊 Dataset
Source: Scikit-learn (Breast Cancer Wisconsin Dataset)
Number of Features: 30 medical diagnostic features
Target Variable: Diagnosis
0 → Malignant (Cancer)
1 → Benign (Non-Cancer)
🧠 Models Used
🔹 Single Models
Logistic Regression (L1 regularization, liblinear solver)
Decision Tree Classifier
🔹 Ensemble Model
Random Forest Classifier
🔁 Methodology
Train–Test split (80% – 20%)
Feature scaling using StandardScaler (for Logistic Regression)
Model training using both single models and an ensemble model
Performance evaluation using:
Accuracy
Precision
Recall
F1-Score
ROC–AUC Score
Confusion Matrix
Classification Report
Comparative analysis between single vs ensemble models
📈 Evaluation Metrics (Medical Perspective)
Accuracy: Overall correctness of predictions
Precision: Correct malignant predictions among all predicted malignant cases
Recall (Critical Metric): Ability to detect actual cancer patients
F1-Score: Balance between precision and recall
ROC–AUC: Model’s ability to distinguish between malignant and benign tumors
⚠️ In healthcare, recall and ROC–AUC are more important than accuracy alone.
🔍 Single Model vs Ensemble Model Comparison
🔹 Single Models (Logistic Regression & Decision Tree)
Easier to interpret
Lower computational complexity
Decision Tree prone to overfitting
Slightly lower recall and ROC–AUC
Risk of missing malignant cases
🔹 Ensemble Model (Random Forest)
Combines predictions from multiple decision trees
Reduces overfitting
Higher accuracy, recall, and ROC–AUC
More robust and stable on unseen patient data
Lower false-negative rate (safer for medical diagnosis)
✅ Results & Model Evaluation
🔹 Logistic Regression
Good accuracy and recall
Interpretable and clinically explainable
Suitable as a baseline medical model
🔹 Decision Tree
Simple and interpretable
Lower generalization performance
Less reliable for clinical use
🔹 Random Forest (Ensemble Model)
Best overall performance
Highest ROC–AUC score
Strong recall (fewer missed cancer cases)
Most consistent predictions
🏆 Final Model Selection
The Random Forest Classifier (Ensemble Model) is identified as the most reliable model for real-world breast cancer prediction.
Reasons:
Superior performance compared to single models
Excellent generalization ability
Reduced false negatives
Higher robustness for clinical deployment
👉 Recommended Medical Strategy:
Use Random Forest for final predictions and Logistic Regression for interpretability and medical explanation.
🚀 Tools & Libraries
Python
NumPy
Pandas
Scikit-learn
Matplotlib
Google Colab
Hyperparameter Tuning Observations
During experimentation, key hyperparameters of the models were varied to analyze their impact on performance:
🔹 Logistic Regression (C parameter)
The regularization parameter C was tested with multiple values.
Changing C (regularization strength) did not significantly impact evaluation metrics such as:
Accuracy
Precision
Recall
F1-score
ROC–AUC
Reason:
The dataset is well-structured and linearly separable.
Logistic Regression already finds an optimal decision boundary with default settings.
Small to moderate changes in C do not alter the learned coefficients significantly.
Feature scaling further stabilizes model behavior.
🔹 Random Forest (n_estimators parameter)
The number of trees (n_estimators) was varied.
Increasing or decreasing n_estimators did not lead to noticeable improvement in evaluation metrics.
Reason:
Even a moderate number of trees is sufficient for this dataset.
The model converges quickly due to:
Low noise in the data
Strong feature signals
Additional trees mainly increase computational cost, not predictive performance.
📌 Conclusion
This study demonstrates that ensemble learning models outperform single models in breast cancer classification tasks.
The Random Forest Classifier provides the best balance between performance, reliability, and safety, making it suitable for clinical decision-support systems.
