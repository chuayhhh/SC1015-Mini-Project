# SC1015: Data Science Mini Project - Credit Risk Analysis
**School of Computer Science and Engineering**  
**Nanyang Technological University**

**Lab:** FR1  
**Group:** 7 

**Members:**  
- Chua Yu Hui (YCHUA056@e.ntu.edu.sg) 
- Megan Phua Wei Lin, (MPHUA006@e.ntu.edu.sg)
- Khoo An Xian (KHOO0212@e.ntu.edu.sg)  

---

## Description
This repository contains the datasets, Jupyter Notebooks, and source materials used in our SC1015 Mini Project. The focus of this project is to analyze credit risk using financial and loan-related data to derive actionable insights and improve loan approval decision-making processes.

Through this project, we aim to:
- Explore patterns in the dataset related to loan approvals, defaults, and financial stability.
- Implement machine learning models to predict creditworthiness.
- Provide data-driven recommendations for financial institutions to minimize risk and maximize efficiency.

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
Credit risk analysis is critical for financial institutions to minimize losses and improve lending strategies. By understanding customer behaviors and risk factors, in

## 2. Data Preparation and Cleaning

### Dataset Overview:
The dataset consists of various features, including:
- **Loan Information:** Loan amount, interest rates, loan status.
- **Customer Details:** Income level, age, employment length.
- **Credit Information:** Credit score, credit history length, delinquency records.

### Steps Taken:
1. **Loading the Dataset:** 
   - Imported the dataset and examined the structure, size, and data types.

2. **Feature Selection:**
   - Retained relevant features for analysis, such as `Credit Score`, `Loan Amount`, `Annual Income`, `Loan Status`, `Debt-to-Income Ratio`, and `Number of Delinquencies`.
   - Dropped unrelated or redundant columns (e.g., IDs).

3. **Handling Missing Values:**
   - Identified missing data and filled numerical features (e.g., `Annual Income`, `Credit Score`) using median imputation.
   - For categorical features (e.g., `Loan Status`), used mode imputation or dropped rows with excessive missing data.

4. **Encoding Categorical Variables:**
   - Converted categorical features into numerical format using one-hot encoding or label encoding. For example:
     - `Loan Status`: Converted "Approved", "Rejected", "Default" into numerical labels.

5. **Feature Engineering:**
   - Derived new features such as:
     - `Debt-to-Income Ratio` = `Total Debt` / `Annual Income`.
     - `Loan-to-Income Ratio` = `Loan Amount` / `Annual Income`.

6. **Data Splitting:**
   - Split the dataset into training and test sets for machine learning analysis (e.g., 80% training, 20% testing).

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

## 4. Add

## 5. Add

## 6. Add

## 7. References
   - Add later
