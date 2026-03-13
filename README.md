# Heart-Disease-Detection

📌 Overview
This repository contains my full machine learning pipeline for the Kaggle S6E2 Heart Disease Prediction Challenge, where the goal was to predict the probability of heart disease using tabular patient data.
I developed and compared two strong ensemble models — Random Forest Classifier and XGBoost Classifier — and achieved ROC–AUC scores above 0.95 on both.

🚀 Key Results
Random Forest Classifier ROC-AUC score:  0.9545719887196342
XGBoost Classifier ROC-AUC score:  0.9545348422535078

ModelROC–AUC ScoreRandom Forest Classifier0.954572XGBoost Classifier0.954535
Both models performed extremely well, with almost identical discrimination ability.

📂 Project Workflow
1. Importing & Inspecting the Data

Loaded the training and test CSV files from Kaggle.
Verified dataset health:

Checked for null values
Checked data types & consistency
Ensured no corrupted or ill‑formed entries



2. Feature Engineering
Added informative derived features to enhance signal in the dataset, such as:

New interaction columns
Encoded categorical features
Domain‑based transformations
Normalization / scaling when necessary

3. Train/Validation Split

Used a 90/10 split, keeping 10% for validation.
Ensured stratification to preserve the distribution of the target variable.

4. Model Training
Trained two separate models:
🔹 Random Forest Classifier

Tuned base hyperparameters
Robust to non‑linearities
Performs well on tabular datasets

🔹 XGBoost Classifier

Gradient‑boosted trees
Excellent performance with fine‑grained control
Handles feature interactions efficiently

5. Model Evaluation
Used ROC–AUC as the primary metric, reflecting the model’s ability to distinguish between heart‑disease and non‑heart‑disease cases.
6. Building the Final Submission

Processed test data using the same feature engineering steps as train
Ensured test columns matched training columns perfectly
Generated probability predictions using the final chosen model
Created submission.csv with required format:

id
heart disease probability



Example submission rows:
id       Churn
594194   0.073583
594195   0.000983
594196   0.116173
594197   0.003208
594198   0.503741

7. Submission
Exported final file:
submission.csv

uploaded to Kaggle for scoring.

📁 Repository Structure
├── data/
├── notebooks/
├── models/
├── submission.csv
├── README.md


🛠 Tools & Libraries

Python
Pandas, NumPy
Scikit‑learn
XGBoost
Random Forest
Matplotlib / Seaborn
Jupyter Notebook


📌 Conclusion
This project demonstrates a complete end‑to‑end ML workflow for tabular health data, applying strong ensemble models with competitive performance (>0.95 ROC–AUC).
The methodology is reproducible, clean, and competition‑ready.
