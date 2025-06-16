# Online-Fraud-Detection-Model
Objective: Using a historical dataset, the main goal is to identify fraudulent and non-fraudulent online payment transactions.

Data: The project utilises a dataset from Kaggle containing various details about online transactions, including step (time unit), transaction type, amount, customer information (originator and recipient), account balances before and after the transaction, and a flag indicating whether the transaction is fraudulent (isFraud).

Exploratory Data Analysis (EDA): The notebook performs an in-depth EDA to understand the data characteristics. This includes: Checking data types and missing values. Analysing the distribution of key features like transaction amount and account balances, noting their right-skewed nature. Investigating the frequency of different transaction types and identifying that fraudulent transactions primarily occur in 'CASH_OUT' and 'TRANSFER' types. Identifying steps (time units) and customer/recipient profiles most associated with fraudulent activities.

Visualising correlations between numerical features.

Data Preprocessing: The data is prepared for modelling by: Handling categorical features (although the mapping of 'type' seems to have been repeated). Dropping irrelevant or redundant columns (isFlaggedFraud, nameOrig, nameDest, newbalanceOrig, newbalanceDest, and the created amount/balance quantity columns). Scaling numerical features using StandardScaler. Addressing class imbalance by using RandomUnderSampler on the training data.

Model Building and Evaluation: Two classification models, Random Forest and Logistic Regression, are selected. K-Fold Cross-Validation evaluates the models based on various metrics (accuracy, precision, recall, f1-score, and ROC AUC). The Random Forest Classifier is identified as the best-performing model based on the cross-validation results and its high AUC score (0.996) on the test set. A detailed classification report and confusion matrix are provided for the Random Forest model, highlighting its performance in correctly identifying fraudulent and non-fraudulent transactions.
