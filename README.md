LOAN APPROVAL PREDICTOR
This project presents a complete machine learning pipeline for predicting loan approval status. It uses a dataset with details about loan applicants to train and compare two classification models: Logistic Regression and a Decision Tree. The goal is to identify which model performs best and to provide an interactive application for making predictions.

📂 Project Structure


Group assignment.ipynb: The main Jupyter notebook containing all the code for data loading, preprocessing, model training, and evaluation.

Loan_Train.csv: The dataset used for training and testing the models.

Report.pdf: A detailed report summarizing the project's findings, methodology, and conclusions.

📊 Dataset Overview


Source: Kaggle - Loan Prediction Practice Dataset


Rows: 614 loan applications.


Features: Includes applicant details such as Gender, Married, Education, ApplicantIncome, LoanAmount, and Credit_History.


Target Variable: Loan_Status, a binary column indicating whether the loan was approved ('Y') or rejected ('N').

Problem Type: Binary Classification.

🚀 Methodology

The project follows a standard machine learning workflow:

1. Data Exploration & Preprocessing
The initial analysis revealed missing values in several columns.


Missing Values: Handled by filling categorical columns with the mode and numerical columns with the median.

Encoding: Categorical features were converted into a numerical format. 

Label encoding was used for binary columns, and one-hot encoding was applied to features with multiple categories, like Property_Area and Dependents.


Scaling: Numerical features were normalized using StandardScaler for the Logistic Regression model.


Splitting: The data was divided into an 80% training set and a 20% test set.

2. Model Training & Evaluation


Two models were trained and their performance was compared using a variety of metrics.


Logistic Regression: A baseline classifier trained on the scaled data.


Decision Tree Classifier: A model that learns decision rules, trained on the unscaled data.

Metric	Logistic Regression	Decision Tree
Accuracy	78.9%	67.5%
Precision	75.9%	73.3%
Recall	98.7%	78.7%
F1 Score	85.9%	75.9%

Export to Sheets

Conclusion: Logistic Regression outperformed the Decision Tree, especially in recall, correctly identifying nearly all approved loan applications. This makes it a more suitable model for this problem, where avoiding the false rejection of a good applicant is crucial.

🛠️ Interactive Prediction App

A Gradio application is included in the notebook to allow users to interact with the trained models. Users can input a loan applicant's details and receive a predicted loan status from both the Logistic Regression and Decision Tree models.

🧠 Suggestions for Improvement


Explore more complex models such as 

Random Forest or XGBoost.

Use 

hyperparameter tuning with techniques like GridSearchCV to optimize model performance.

Implement a 

Streamlit app for a more robust and scalable user interface.

Incorporate 

k-fold cross-validation to ensure the models' robustness.
