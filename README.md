# Customer Churn Prediction (Telco)

## Project Description
This project aims to predict customer churn using machine learning techniques on real-world telecommunications data.

The approach combines exploratory data analysis (EDA), preprocessing, modeling, and evaluation, with a strong focus on business-oriented decision making.

The following supervised models were evaluated:
- Logistic Regression (baseline and balanced)
- Random Forest (baseline and balanced)

The main objective is to identify customers at risk of leaving in order to support retention strategies.

---

## Dataset
- Source: Kaggle  
- Link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn  
- Name: Telco Customer Churn  
- Description: Customer data from a telecommunications company, including services, billing, and behavior.

Main variables:
- `tenure`: Customer tenure  
- `MonthlyCharges`: Monthly charges  
- `TotalCharges`: Total accumulated charges  
- `Contract`: Contract type  
- `InternetService`: Type of internet service  
- `PaymentMethod`: Payment method  
- `Churn`: Target variable (Yes/No)  

---

## Methodology

### 1. Data Cleaning
- Data type conversions  
- Handling missing values  
- Consistency checks for numerical variables  

### 2. Exploratory Data Analysis (EDA)
- Distribution analysis  
- Outlier detection  
- Relationship between variables and churn  
- Categorical analysis vs churn  

### 3. Preprocessing
- Separation of numerical and categorical features  
- Scaling using `StandardScaler`  
- Encoding using `OneHotEncoder`  
- Use of `ColumnTransformer` and `Pipeline` to prevent data leakage  

### 4. Modeling
The following models were trained:

- Logistic Regression (baseline)
- Logistic Regression with `class_weight="balanced"`
- Random Forest (baseline)
- Random Forest with `class_weight="balanced"`

### 5. Evaluation
Models were evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion matrix  
- ROC-AUC  

---

## Results

### Key Findings
- Customers with lower tenure have a higher probability of churn  
- Month-to-month contracts show higher churn risk  
- Customers with higher monthly charges tend to churn more  
- Class imbalance significantly affects model performance  

### Model Performance
- Logistic Regression baseline shows good accuracy but low recall for churn  
- Random Forest baseline fails to properly detect churn  
- Using `class_weight="balanced"` significantly improves detection  

### Final Model
The selected model was:

 **Balanced Random Forest**

- Recall (churn): 0.71  
- Precision (churn): 0.55  
- F1-score: 0.62  
- Accuracy: 0.77  

This model provides the best trade-off between performance metrics.

---

## Conclusions
The project shows that:

- Churn is influenced by key variables such as tenure, contract type, and monthly charges  
- Handling class imbalance is critical  
- More complex models do not always improve performance without proper adjustments  

The final model achieves a balance between precision and detection capability, making it suitable for retention strategies.

---

## Limitations
- No hyperparameter tuning was performed  
- Advanced models (XGBoost, LightGBM) were not evaluated  
- No temporal variables were included  
- Threshold optimization was not implemented as final solution  
- Dataset size and scope are limited  

---

## Next Steps

### Version 2 (V2)
- Implement advanced models (XGBoost, LightGBM)  
- Perform hyperparameter tuning  
- Optimize threshold based on business needs  
- Apply techniques such as SMOTE  

### MLOps & Deployment
- Deploy using AWS (SageMaker / Lambda / API Gateway)  
- Build real-time inference pipeline  
- Monitor model performance  
- Automate retraining  

---

## Technologies Used
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  

---

## Author

**Immani Trejo**  
Data Science | Machine Learning | IT Background  

Experience in data analysis, applied statistics, machine learning, and cloud-based deployment.

---

⭐ **Recruiter Note**

This project builds a churn prediction model using real-world telecom data, applying best practices such as handling class imbalance, using pipelines, and robust evaluation.

It demonstrates the ability to create business-oriented solutions ready for production environments.
