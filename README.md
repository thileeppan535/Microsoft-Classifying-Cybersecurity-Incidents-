# Microsoft-Classifying-Cybersecurity-Incidents-
Project Overview: Microsoft - Classifying Cybersecurity Incidents with Machine Learning
This project aims to classify cybersecurity incidents into three categories: True Positive (TP), Benign Positive (BP), and False Positive (FP) using machine learning techniques. The goal is to build a model that can generalize effectively to unseen data and offer actionable insights to improve incident management.

Approach:
Data Exploration and Understanding

Initial Inspection: Loaded the train.csv dataset to analyze its structure, including the number of features, types of variables (categorical and numerical), and the distribution of the target labels (TP, BP, FP).
Exploratory Data Analysis (EDA): Used visualizations like heatmaps and count plots, along with statistical summaries, to detect patterns, correlations, and any anomalies in the dataset. Class imbalances were addressed as needed.
Data Preprocessing

Handling Missing Data: Used SimpleImputer to fill in missing values.
Feature Engineering: Extracted new features from timestamps (e.g., hour of the day, day of the week) to improve the model's predictive power.
Encoding Categorical Variables: Applied LabelEncoder to convert categorical features into numerical representations.
Data Splitting

Train-Validation Split: Divided the dataset into training and validation sets, using a typical split of either 70-30 or 80-20.
Stratification: Employed stratified sampling to maintain balanced class distributions across both sets.
Model Selection and Training

Baseline Model: Started with a logistic regression model as a benchmark for performance.
Advanced Models: Tested more sophisticated models, including RandomForestClassifier and XGBClassifier, using RandomizedSearchCV for hyperparameter tuning.
Cross-Validation: Implemented StratifiedKFold to ensure model performance was consistent across multiple data subsets.
Handling Class Imbalance: Addressed class imbalance using SMOTE (Synthetic Minority Over-sampling Technique) to improve model accuracy.
Model Evaluation and Tuning

Performance Metrics: Evaluated model performance using the macro-F1 score, precision, and recall. Results were analyzed across all classes (TP, BP, FP) to ensure balanced accuracy.
Hyperparameter Tuning: Fine-tuned model parameters to optimize performance based on validation results.
Feature Importance: Analyzed key features using permutation importance to identify which features had the most impact on predictions.
Final Evaluation

Testing: Assessed the final model on the test.csv dataset to evaluate its generalization capabilities.
Comparison to Baseline: Compared the model's test results with the baseline to confirm improvements and consistency.
