# Course 4 – Logistic Regression

This folder contains the regression modeling phase of the Waze user churn analysis project completed as part of the Google Advanced Data Analytics Professional Certificate.

## Objective

The objective of this phase was to build and evaluate a binomial logistic regression model to predict whether a Waze user will churn.

## Work Completed

- Performed exploratory data analysis before modeling
- Examined missing values, class balance, correlations, and potential outliers
- Engineered a `km_per_driving_day` feature
- Created a `professional_driver` feature
- Handled missing target values
- Imputed outliers using 95th-percentile thresholds
- Encoded churn as a binary target variable
- Examined multicollinearity among predictor variables
- Encoded device type for modeling
- Split the data into training and testing sets
- Built a binomial logistic regression model
- Generated churn predictions
- Evaluated model accuracy
- Created and interpreted a confusion matrix
- Evaluated precision and recall
- Examined model coefficients and predictor relationships

## Key Findings

- Professional drivers had a substantially lower churn rate than non-professional drivers.
- Professional drivers had a churn rate of approximately 7.6%, compared with approximately 19.9% for non-professional drivers.
- User activity and driving behavior provided useful information for predicting churn.
- Some predictor variables were highly correlated and were excluded to reduce multicollinearity.
- The logistic regression model achieved reasonable precision but low recall for churned users.
- The low recall indicates that the model failed to identify many users who actually churned.
- Because identifying at-risk users is important for a churn model, additional modeling and feature engineering would be recommended before deployment.

## Tools & Skills

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- Exploratory data analysis
- Feature engineering
- Logistic regression
- Train-test splitting
- Classification metrics
- Confusion matrices
- Precision and recall
- Model evaluation

## Files

- `waze_course4_logistic_regression.ipynb` — completed Course 4 logistic regression notebook

## Note

This is an educational project using synthetic data created for the Google Advanced Data Analytics Professional Certificate.
