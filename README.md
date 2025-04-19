# SC1015: Data Science Mini Project - Credit Risk Analysis
**School of Computer Science and Engineering**  
**Nanyang Technological University**

**Lab:** FR1  
**Group:** 7 

**Members:**  
- Chua Yu Hui (YCHUA056@e.ntu.edu.sg) 
- Megan Phua Wei Lin (MPHUA006@e.ntu.edu.sg)
- Khoo An Xian (KHOO0212@e.ntu.edu.sg)  

---

## Description
This repository contains the datasets, Jupyter Notebooks, and source materials used in our SC1015 Mini Project. The focus of this project is to analyze credit risk using financial and loan-related data to derive actionable insights and improve loan approval decision-making processes.
---

## Table of Contents
## 1. Problem Formulation

### Dataset:
The dataset is sourced from Kaggle: [Credit Risk Analysis Dataset](https://www.kaggle.com/datasets/zaurbegiev/my-dataset?resource=download).  
It contains financial and credit-related information, such as loan amounts, credit scores, income levels, credit history length, and delinquency records.

### Objective:
The primary goal of this project is to analyze credit risk by:
1. Identifying factors that influence loan approval and risk.
2. Predicting customer creditworthiness using machine learning models.
3. Highlighting actionable insights to help financial institutions mitigate risks and improve decision-making.

### Key Questions:
1. What trends and patterns can be observed in loan approvals, credit scores, and customer demographics?
2. How do factors like income, credit history, and delinquencies contribute to loan defaults?
3. Can we build a reliable predictive model for loan default risk?

### Relevance:
Credit risk analysis is critical for financial institutions to minimize losses and improve lending strategies. 
Our team identified the problem of predicting loan default risks using a real-world credit dataset (credit_train.csv). The primary goal is to determine whether a borrower will fully repay their loan or default, using various financial, personal, and credit-related features. We chose this problem due to its real-world relevance in banking, risk assessment, and lending institutions.

## 2. Data Preparation and Cleaning

### Dataset Overview:
The dataset consists of various features, including:
- **Loan Information:** Loan amount, interest rates, loan status.
- **Customer Details:** Income level, age, employment length.
- **Credit Information:** Credit score, credit history length, delinquency records.

### Steps Taken:
1. **Loading the Dataset:** 
   - Imported the dataset and examined the structure, size, and data types.
   - Selecting the first 20,000 rows for manageable processing.

2. **Feature Selection:**
   - Retained relevant features for analysis, such as `Credit Score`, `Loan Amount`, `Annual Income`, `Loan Status`, `Debt-to-Income Ratio`, and `Number of Delinquencies`.
   - Dropped unrelated or redundant columns (e.g., IDs).

3. **Handling Missing Values:**
   - Identified missing data and filled numerical features (e.g., `Annual Income`, `Credit Score`) using median imputation.
   - For categorical features (e.g., `Loan Status`), used mode imputation or dropped rows with excessive missing data.

4. **Encoding Categorical Variables:**
   - Converted categorical features into numerical format using one-hot encoding or label encoding. 

5. **Feature Engineering:**
   - Derived new features such as:
     - `Debt-to-Income Ratio` = `Total Debt` / `Annual Income`.
     - `Loan-to-Income Ratio` = `Loan Amount` / `Annual Income`.

6. **Data Splitting:**
   - Split the dataset into training and test sets for machine learning analysis (e.g., 80% training, 20% testing).

   This allowed for more insightful relationships to be modeled in our analysis and prediction stages.

## 3. Exploratory Data Analysis

### Objectives:
1. Understand the distribution and trends in key variables.
2. Identify relationships between features that may affect loan approvals or defaults.
3. Detect patterns and outliers for further investigation.

### Key Insights:
1. **Loan Amount Distribution:**
   - Examined the distribution of loan amounts across customers.
   - Identified any outliers or anomalies, such as extremely high or low loan amounts.

2. **Credit Score Analysis:**
   - Analyzed the distribution of credit scores and its relationship with loan status.
   - Found trends such as higher credit scores correlating with loan approval.

3. **Annual Income Trends:**
   - Explored income levels and their impact on default risk.
   - Observed whether income had a significant influence on approved loans.

4. **Debt-to-Income Ratio:**
   - Analyzed the ratio to understand its correlation with loan status.
   - Identified whether customers with higher debt ratios were more likely to default.

5. **Loan Status Analysis:**
   - Compared the proportion of approved, rejected, and defaulted loans.
   - Cross-examined loan status with features like income and credit score.

6. **Outlier Detection:**
   - Detected anomalies in variables such as `Credit Score`, `Loan Amount`, and `Debt-to-Income Ratio`.

### Observed Key Relationships:
   - High correlation between Monthly Debt and Annual Income.
   - Business loans had a lower repayment rate compared to personal or education loans.
   - Short-term loans showed higher full repayment rates.

This helped refine the features most likely to influence repayment behavior.

## 4. Machine Learning Model & Methodology

### We built a supervised classification model using:
   - Logistic Regression
   - Random Forest Classifier
   - XGBoost Classifier

### Approach:
   - Feature selection via correlation filtering.
   - Train-test split (80/20).
   - Standardization of numerical features.
   - Hyperparameter tuning using GridSearchCV.

### Evaluation Metrics:
   - Accuracy
   - Precision
   - Recall
   - F1 Score
   - Confusion Matrix

XGBoost outperformed the others in terms of both precision and recall, making it our primary model.

## 5. Insights & Recommendations:

### From the model and data insights, we recommend:
   - Business loans should be subject to tighter approval criteria due to higher default rates.
   - Focus marketing on individuals with high Income-to-Loan Ratios.
   - Consider adding more recent behavioral data to improve prediction power (e.g., transaction patterns).

## 7. References:
