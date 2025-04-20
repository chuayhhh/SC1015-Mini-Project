# SC1015: Data Science Mini Project - Credit Risk Analysis
**School of Computer Science and Engineering**  
**Nanyang Technological University**

## About
This repository contains the datasets, Jupyter Notebooks, and source materials used in our SC1015 Mini Project. The focus of this project is to analyze credit risk using financial and loan-related data to derive actionable insights and improve loan approval decision-making processes.

### Dataset:
The dataset is sourced from Kaggle: [Credit Risk Analysis Dataset](https://www.kaggle.com/datasets/zaurbegiev/my-dataset?resource=download).  
It contains financial and credit-related information, such as loan amounts, credit scores, income levels, credit history length, and delinquency records.

For detailed walkthrough, please view the source code in order from:

1. [Data Preparation](https://github.com/chuayhhh/SC1015-Mini-Project/blob/main/data-preparation.ipynb)
2. [Data Visualization](https://github.com/chuayhhh/SC1015-Mini-Project/blob/main/data-visualisation.ipynb)
3. [Machine Learning Models](https://github.com/chuayhhh/SC1015-Mini-Project/blob/main/machine-learning.ipynb)
  
## Contributors

**Lab:** FR1  
**Group:** 7 

- Chua Yu Hui (U2323111H) 
- Megan Phua Wei Lin ()
- Khoo An Xian ()  

---

## 1. Problem Formulation

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

---

## 2. Models Used
We experimented with multiple classification algorithms and addressed class imbalance using SMOTE (Synthetic Minority Over-sampling Technique). The models include:
   - Random Forest
   - XGBoost
   - K-nearest neighbour (KNN)
   
SMOTE was applied to balance the number of Charged Off loans (minority class) with Fully Paid loans during training, significantly improving recall performance on default prediction.
   
## 3. Conclusion:
   - Random Forest with SMOTE and Class Weighting delivered the best balanced performance (accuracy ~81%, recall on Charged Off ~81%).
   - Business Loans exhibited a notably higher default rate (~30%) and should be considered for stricter lending policies or risk premiums.
   - Applicants with high Income-to-Loan Ratios tend to have better repayment behavior — ideal for targeted marketing or pre-approval campaigns.
   - Including behavioral features like recent spending or repayment patterns (e.g., late payments, transaction trends) could boost model performance and stability.
   - Outlier removal and feature engineering (e.g., dti, loan_income_ratio) were essential in reducing noise and improving model generalizability.
   - Business loans should be subject to tighter approval criteria due to higher default rates.

## 4. What we leaned from this project:
   - Data cleaning is critical: variables like Months Since Last Delinquent were dropped due to high missingness, while extreme outliers (e.g., Loan Amounts = 99,999,999) had to be handled before modeling.
   - Feature engineering adds significant value — variables like Debt-to-Income Ratio and Loan-to-Income Ratio improved signal strength.
   - Class imbalance can drastically skew model outcomes — SMOTE was essential to improve recall on the Charged Off class.
   - Credit risk is influenced more by credit behavior features (Credit Score, Utilization, Credit Problems) than raw financial metrics like Income alone.
   - Visualizations (heatmaps, violin plots, cluster segmentation) helped drive both modeling decisions and business recommendations.