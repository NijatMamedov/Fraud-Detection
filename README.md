# Fraud-Detection
  Pre-Processing Steps
 Drop Unnecessary Columns
Remove columns you don’t need to keep the dataset clean.
________________________________________
 Convert 'Date of transaction' to DateTime
Convert the date column using dayfirst=True so the day comes first.
________________________________________
 Create Year, Month, Day Columns
Extract year, month, and day from the date and create new columns.
________________________________________
 Drop the Original Date Column
After creating the new columns, delete the old date column.
________________________________________
 Check for Missing Values
Look for any missing data and fix it before modeling.
________________________________________
 Create a Dummy Dataset
Turn categorical columns into numbers using one-hot encoding.
________________________________________
 Prepare Input Datasets
Make two sets:
•	One with numerical inputs
•	One with categorical inputs (fill missing values with "Missing value").
________________________________________
 Train-Test Split
Split both datasets into training and testing sets for model building.
 Model Preparation and Evaluation
 Create a List of Models
Prepare a list that includes:
1.	XGBoost
2.	LGBM
3.	CatBoost
4.	CatBoost with categorical features
5.	Random Forest
________________________________________
 Train and Evaluate Models
Use the train_and_evaluate_model function to train and test all the models from your list one by one.
  Hyperparameter Optimization with Optuna
 Optimize Model Parameters
Use Optuna to find the best hyperparameters for your models.
________________________________________
 Evaluate Optimized Models
Call the train_and_evaluate_model function to check the results of the optimized models.
  All Results of Models
 Combine Default and Optimized Models
Concat the results of default and optimized models' Gini scores.
________________________________________
 Decide the Best Model
Choose the model with the best Gini score.
 SHAP Value Analysis & Feature Importance
 Check SHAP and Feature Importance
For the best model, analyze SHAP values and feature importance.
________________________________________
 Select Important Variables
Choose variables with Importance > 1%.
 Build Best Model Using Final Inputs
 Train the Best Model
Train the best selected model on the final inputs.
________________________________________
 Check Results
If the result is higher than 40%, move the model into the production environment.
 Deployment
 Deploy Model
Deploy the model on the fraud_deploy_data.xlsx.
________________________________________
 Create 'Probability of Fraud' Column
Generate a new column with the probability of fraud.
________________________________________
 Extract Fraudulent Data
Filter and extract rows where probability of fraud > 10%.

