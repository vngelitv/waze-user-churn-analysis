# Waze User Churn Analysis

## Project Overview

This educational project examines synthetic Waze user data using Python and pandas. The analysis was completed as part of the Google Advanced Data Analytics Professional Certificate.

The broader goal of the project is to prepare user data for a future machine learning model that predicts monthly user churn.

## Business Problem

User churn occurs when users uninstall the Waze app or stop using it. Predicting which users are most likely to churn could help Waze improve retention, provide a better user experience, and support company growth.

This stage of the project focuses on inspecting, organizing, and understanding the dataset before performing more detailed exploratory data analysis and building a predictive model.

## Dataset

The dataset contains 14,999 unique Waze users and 13 original variables.

The variables include:

- User retention or churn label
- Monthly app sessions
- Monthly drives
- Device type
- Total estimated sessions
- Days since onboarding
- Navigations to favorite locations
- Kilometers driven
- Driving duration
- Activity days
- Driving days

The dataset is synthetic and was created for educational purposes. It does not represent Waze's actual internal user data.

## Tools and Skills

- Python
- pandas
- NumPy
- Jupyter Notebook
- Data inspection
- Missing-value analysis
- Descriptive statistics
- Grouping and aggregation
- Feature engineering
- Churn analysis
- Exploratory data analysis preparation
- Matplotlib
- Seaborn
- Exploratory Data Analysis
- Data Visualization
- Feature Engineering
  
## Tasks Completed

- Imported the dataset into a pandas DataFrame
- Inspected the dataset structure and data types
- Identified missing values
- Compared users with and without missing labels
- Examined device distributions
- Compared churned and retained users
- Used median statistics to reduce the influence of outliers
- Created new driving-behavior variables
- Prepared recommendations for future analysis

## New Variables Created

- `km_per_drive`
- `km_per_driving_day`
- `drives_per_driving_day`

These variables provide additional information about the driving behavior of retained and churned users.

## Key Findings

- The dataset contains 14,999 users and 13 original variables.
- The `label` column contains 700 missing values.
- Missing labels appear to be randomly distributed and are not strongly associated with device type.
- Approximately 82% of labeled users were retained and 18% churned.
- Approximately 64.5% of users used an iPhone and 35.5% used Android.
- Device proportions were nearly identical among churned and retained users.
- Churned users completed more drives over fewer driving days.
- Churned users drove farther and for longer durations than retained users.
- The median churned user drove approximately 698 kilometers per driving day, compared with approximately 290 kilometers for retained users.
- High-mileage or frequent drivers may represent a user group that requires further investigation.

## Recommended Next Steps

- Investigate the cause of the missing churn labels
- Conduct more detailed exploratory data analysis
- Examine correlations between driving behavior and churn
- Investigate unusually high-mileage users
- Determine whether the sample includes a large number of professional or long-haul drivers
- Select useful predictors for a churn classification model
- Build and evaluate a machine learning model

## Project File

- `waze_user_churn_analysis.ipynb` — completed Python notebook

## Note

This is an educational project based on synthetic data and course materials from the Google Advanced Data Analytics Professional Certificate.

## Project Progression

### Course 1: Data Inspection and Organization

- Imported and inspected the Waze user dataset
- Reviewed data types and missing values
- Compared retained and churned users
- Examined device distributions
- Created initial behavioral features
- Prepared the data for deeper exploratory analysis

### Course 2: Exploratory Data Analysis and Visualization

- Examined distributions using box plots, histograms, pie charts, and scatterplots
- Compared activity days with driving days
- Analyzed retention and churn by device type
- Created a kilometers-per-driving-day feature
- Investigated churn rates by driving frequency and distance
- Created a percentage-of-sessions-in-the-last-month feature
- Identified and capped selected outliers at the 95th percentile
- Summarized behavioral patterns associated with user churn

## Key Course 2 Findings

- Approximately 17% of users churned and 83% were retained.
- Device type did not show a meaningful difference in churn rate.
- Users who drove longer distances per driving day were more likely to churn.
- Users with more driving days and activity days were less likely to churn.
- Many numerical variables were strongly right-skewed.
- Some long-term users completed a surprisingly large percentage of their lifetime sessions during the most recent month.
- The causes of churn among long-distance drivers warrant further investigation.

### Course 3: Statistical Analysis and Hypothesis Testing

- Compared average numbers of drives by device type
- Encoded iPhone and Android users for analysis
- Used descriptive statistics to compare groups
- Formulated null and alternative hypotheses
- Conducted a two-sample t-test
- Used a 5% significance level
- Found no statistically significant difference in mean drives between iPhone and Android users
- Interpreted the result for business stakeholders

## Key Course 3 Finding

The difference in mean number of drives between iPhone and Android users was not statistically significant (`p ≈ 0.143`).

Because the p-value was greater than the 0.05 significance level, the null hypothesis was not rejected. Device type alone does not appear to be an important predictor of driving behavior.

### Course 4: Logistic Regression

- Performed EDA in preparation for predictive modeling
- Examined missing values, class balance, outliers, and correlations
- Engineered `km_per_driving_day` and `professional_driver` features
- Handled missing target values and imputed extreme outliers
- Encoded categorical and target variables for modeling
- Evaluated multicollinearity among predictors
- Split the data into training and testing sets
- Built a binomial logistic regression model to predict user churn
- Evaluated predictions using accuracy, precision, recall, and a confusion matrix
- Interpreted model coefficients and assessed logistic regression assumptions

## Key Course 4 Findings

Professional drivers had a churn rate of approximately 7.6%, compared with approximately 19.9% for non-professional drivers.

The logistic regression model demonstrated reasonable precision but low recall when identifying churned users. This means the model missed many users who actually churned.

Because identifying users at risk of leaving is the primary business objective, the model would benefit from additional feature engineering, model tuning, and comparison with other classification methods before deployment.

### Course 5: Machine Learning

- Engineered new user-behavior features for churn prediction
- Prepared and encoded variables for machine learning
- Split data into training, validation, and test sets
- Built and tuned Random Forest and XGBoost classifiers
- Used GridSearchCV and cross-validation
- Evaluated models using recall, precision, F1 score, and accuracy
- Selected XGBoost as the champion model
- Evaluated the champion model on unseen test data
- Created a confusion matrix
- Examined feature importance

## Key Course 5 Findings

Approximately 18% of users in the dataset churned.

Recall was prioritized because failing to identify users who actually churn could limit the usefulness of the model for retention efforts.

XGBoost outperformed the Random Forest model on validation data and was selected as the champion model.

The final model still had difficulty identifying a large portion of churned users, suggesting that additional behavioral features and further model development would be needed before deployment.

## Project Files

### Course 1

- `waze_user_churn_analysis.ipynb` — initial data inspection and organization notebook

### Course 2

- `course-2-eda/waze_course2_eda.ipynb` — exploratory data analysis notebook
- `course-2-eda/README.md` — Course 2 project summary

### Course 3

- `course-3-statistics/waze_course3_statistics.ipynb` — statistical analysis and hypothesis testing notebook
- `course-3-statistics/README.md` — Course 3 project summary

### Course 4

- `course-4-regression/waze_course4_logistic_regression.ipynb` — logistic regression churn modeling notebook
- `course-4-regression/README.md` — Course 4 project summary

### Course 5

- `course-5-machine-learning/waze_course5_machine_learning.ipynb` — Random Forest and XGBoost churn modeling notebook
- `course-5-machine-learning/README.md` — Course 5 project summary
