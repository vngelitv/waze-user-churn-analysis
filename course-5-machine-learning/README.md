# Waze User Churn Prediction – Course 5

## Project Overview

This project is part of the Waze user churn analysis capstone. In Course 5, I used machine learning to predict whether a Waze user would churn or remain retained.

The goal was to build and evaluate classification models that could help identify users who may stop using the Waze app.

## Machine Learning Process

For this stage of the project, I:

- Prepared the dataset for machine learning
- Engineered additional user-behavior features
- Encoded categorical variables
- Split the data into training, validation, and test sets
- Built a Random Forest classification model
- Built an XGBoost classification model
- Tuned model hyperparameters using GridSearchCV
- Evaluated model performance using accuracy, precision, recall, and F1 score
- Compared model performance and selected a champion model
- Evaluated the champion model on unseen test data
- Created and analyzed a confusion matrix
- Examined feature importance to understand the strongest predictors of churn

## Model Evaluation

Because the goal of the project is to identify users who may churn, recall was an important evaluation metric.

Missing a user who actually churns could prevent Waze from taking action to improve that user's experience or encourage them to remain active.

After comparing the models, XGBoost was selected as the champion model based on its validation performance.

## Key Findings

- Approximately 18% of users in the dataset were classified as churned.
- User behavior and engagement variables were useful for predicting churn.
- The champion model performed well at identifying retained users but had more difficulty correctly identifying users who churned.
- Feature importance analysis helped identify which user behaviors contributed most to the model's predictions.
- The results suggest that additional behavioral information and further model development could improve churn prediction.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

## Skills Demonstrated

- Machine Learning
- Classification Modeling
- Feature Engineering
- Random Forest
- XGBoost
- Hyperparameter Tuning
- Cross-Validation
- Model Evaluation
- Confusion Matrix Analysis
- Feature Importance Analysis
- Data Interpretation

## Files

- `waze_course5_machine_learning.ipynb` — Complete machine learning notebook containing data preparation, modeling, evaluation, and feature importance analysis.
