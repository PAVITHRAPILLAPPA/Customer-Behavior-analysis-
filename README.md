# Customer-Behavior-analysis for Toyko Software Cataloger

This project focuses on building two predictive models using customer data from Tayko Software Cataloger: one to classify customers as purchasers or non-purchasers, and another to predict the spending amount among purchasers. Both models are designed to support targeted marketing strategies by leveraging customer attributes and behavior.

# DataSet details
- Records: 2,000 customers
- Purpose: Predict purchase behavior and spending
- Target Variables:
     Purchase (1 = yes, 0 = no)
     Spending (amount spent, for purchasers only)
- Key Features
   Demographics: Salary, Age, Gender, Zip_Code
   Marketing Info: History, Catalogs, Promotion, Channel

# Objective
1. **Classification** – Build a logistic regression model to classify whether a customer is likely to make a purchase.
2. **Spend Prediction** – Develop a regression model to estimate how much a purchasing customer is likely to spend.

# Techniques & Tools Used
- Logistic Regression (Classification)
- Multiple Linear Regression (Spend Prediction)
- Feature Engineering & Dummy Variable Management
- Train/Validation/Test Partitioning
- Correlation Analysis & PCA for Variable Selection
- Model Evaluation: Accuracy, AUC, R², RMSE, Residual Analysis

# Data Partitioning
  - Training Set: 800 records
  - Validation Set: 700 records
  - Test Set: 500 records

# Model Performance
**Purchase Classification**  
![image](https://github.com/user-attachments/assets/bb42be54-4b1a-49d6-9480-d3f21b95888e)
📊 Validation Results (700 records):
Accuracy: 81.1%
Precision & Recall: Both ~0.81 for each class
AUC Score: 0.91 – indicating excellent ability to separate purchasers from non-purchasers

🧪 Test Results (500 records):
Accuracy: 78.8%
Precision: 0.76 (non-purchasers), 0.82 (purchasers)
Recall: 0.84 (non-purchasers), 0.73 (purchasers)
AUC Score: 0.90 – consistently strong performance on unseen data
📈 The model shows solid generalization, with balanced performance across precision, recall, and AUC, making it reliable for real-world marketing use.

**Spend Prediction Model Summary**
🧪 Model Results:
Linear Regression (Stepwise Selection):
RMSE: 173.98
R² Score: 0.47

Regression Tree:
RMSE: 185.78
R² Score: 0.39

Best Model: Linear Regression using stepwise feature selection

# Key Findings
- Logistic regression achieved strong classification performance with high AUC and precision, driven by predictors like `Salary`, `Spending Score`, and selected `Source` variables.
- Spend prediction model demonstrated an R² of 0.68 on the validation set, indicating strong predictive power for marketing spend estimation.
- Principal component analysis and correlation filtering helped reduce dimensionality and multicollinearity.




