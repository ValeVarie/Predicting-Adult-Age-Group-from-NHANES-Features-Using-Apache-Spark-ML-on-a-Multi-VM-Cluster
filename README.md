Predicting Adult Age Group from NHANES Features Using Apache Spark ML

Author: Valeria Mudzindiko
Course: Statistical Machine Learning for Big Data Analysis with Spark

📘 Overview

This project builds a scalable classification pipeline in Apache Spark to predict whether a participant belongs to the older or younger adult age group using features from the NHANES dataset. Multiple machine learning models were trained and evaluated in a distributed 2-VM Spark cluster, demonstrating both predictive accuracy and computational efficiency.

🧠 Objectives

Develop a distributed machine learning pipeline using Spark MLlib.

Predict adult age groups based on demographic, clinical, and behavioral NHANES features.

Compare model performance and runtime efficiency across algorithms.

🗂️ Dataset

File: NHANES_age_prediction.csv

Target Variable: label (1 = older adult, 0 = younger adult)

Features: Demographic, clinical, and behavioral predictors (e.g., BMI, blood pressure, lab values).

Preprocessing: Null removal, label indexing, feature assembly via VectorAssembler.

⚙️ Computing Environment

Framework: Apache Spark (PySpark)

Cluster: 2 Virtual Machines (1 Master, 1 Worker)

Cluster Mode: Standalone

Timing Tool: Python time module

🧩 Methods

Load and preprocess data

Encode categorical variables

Assemble features

Split dataset (80/20)

Train models: Logistic Regression, Decision Tree, Random Forest

Evaluate on test data (Accuracy, AUC, Precision, Recall, F1, Specificity)

Measure computational performance

📊 Results
Model	Accuracy	Precision	Recall	F1-Score	AUC
Logistic Regression	0.87	0.85	0.82	0.83	0.89
Decision Tree	0.84	0.81	0.79	0.80	0.86
Random Forest	0.91	0.89	0.87	0.88	0.93

Key Finding: Random Forest achieved the best balance between accuracy and AUC, outperforming other models.

⏱️ Computational Performance (2-VM Cluster)
Model	Train Time (s)	Inference Time (s)
Logistic Regression	28.4	6.3
Decision Tree	46.7	8.9
Random Forest	92.5	11.2

The 2-VM cluster achieved up to 1.4× faster performance compared to single-VM local mode.

🧩 Discussion

Random Forest offered superior predictive performance but required higher computational cost.

Logistic Regression provided quick, interpretable results.

Distributed Spark setup significantly improved scalability and speed.

🏁 Conclusion

This project demonstrates how Apache Spark enables efficient, large-scale machine learning for public health data. Distributed training not only accelerates computation but also scales predictive modeling to handle complex healthcare datasets.
