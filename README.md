# Customer Churn Prediction (Telco) - ML Modeling v1

## Project Overview

This repository represents the first stage of a multi-stage end-to-end Machine Learning project focused on customer churn prediction.

The objective of this phase is to:
- Analyze customer churn behavior
- Build and evaluate machine learning models
- Handle class imbalance
- Select and package a production-ready model

The project combines exploratory data analysis (EDA), preprocessing, modeling, evaluation, and business-oriented interpretation using real-world telecommunications data.

---

# Project Ecosystem

This repository is part of a complete Machine Learning deployment workflow.

## Repository Flow

| Stage | Repository | Purpose |
|---|---|---|
| 1 | [customer-churn-ml-v1](https://github.com/ImmaniTr/customer-churn-ml-v1) | Data analysis, preprocessing, modeling and evaluation |
| 2 | [customer-churn-ml-api-v1](https://github.com/ImmaniTr/customer-churn-ml-api-v1) | Local FastAPI implementation for real-time predictions |
| 3 | [customer-churn-ml-api-aws-v1](https://github.com/ImmaniTr/customer-churn-ml-api-aws-v1) | Initial AWS deployment using Docker and ECS |
| 4 | [customer-churn-aws-deployment-v1](https://github.com/ImmaniTr/customer-churn-aws-deployment-v1) | Production-oriented deployment with ALB, monitoring and CI/CD |

---

# Project Evolution

This repository represents the modeling and experimentation phase of the project.

The project later evolved into:
- API serving with FastAPI
- Docker containerization
- AWS deployment using ECS Fargate
- Application Load Balancer integration
- Monitoring with CloudWatch
- CI/CD automation with GitHub Actions

---

## Dataset

- Source: Kaggle  
- Dataset: Telco Customer Churn  
- Link: https://www.kaggle.com/datasets/blastchar/telco-customer-churn

### Dataset Description

Customer data from a telecommunications company, including:
- customer behavior
- billing information
- service subscriptions
- churn status

### Main Variables

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
- Missing value handling
- Numerical consistency validation

### 2. Exploratory Data Analysis (EDA)
- Distribution analysis
- Outlier inspection
- Churn relationship analysis
- Categorical feature analysis

### 3. Preprocessing
- Numerical and categorical feature separation
- Scaling using `StandardScaler`
- Encoding using `OneHotEncoder`
- Use of `ColumnTransformer` and `Pipeline`
- Data leakage prevention

### 4. Modeling

The following models were evaluated:

- Logistic Regression (baseline)
- Logistic Regression with `class_weight="balanced"`
- Random Forest (baseline)
- Random Forest with `class_weight="balanced"`

### 5. Model Evaluation

Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC

---

## Results

### Key Findings

- Customers with lower tenure have higher churn probability
- Month-to-month contracts show elevated churn risk
- Higher monthly charges correlate with higher churn
- Class imbalance significantly impacts model behavior

### Model Performance

#### Logistic Regression
- Good overall accuracy
- Lower recall for churn detection

#### Random Forest
- Better non-linear learning capability
- Baseline version struggled with churn detection

#### Balanced Random Forest (Selected Model)

Final selected model:

**Balanced Random Forest**

Performance:
- Recall: 0.71
- Precision: 0.55
- F1-score: 0.62
- Accuracy: 0.77

This model achieved the best balance between churn detection and overall predictive performance.

---

## Business Perspective

From a business standpoint, customer retention is often less expensive than acquiring new customers.

For this reason, the project prioritizes recall performance to better identify customers at risk of leaving the company.

This allows companies to:
- improve retention strategies
- reduce customer acquisition costs
- focus interventions on high-risk customers

---

## Limitations

- No extensive hyperparameter tuning
- No advanced boosting models implemented
- No temporal feature engineering
- Limited dataset scope
- Threshold optimization not fully explored

---

## Implemented Extensions

The project was later expanded through additional repositories that introduced:

- FastAPI serving layer
- Docker containerization
- AWS ECS deployment
- Application Load Balancer
- CloudWatch monitoring
- CI/CD automation

See:
- [customer-churn-ml-api-v1](https://github.com/ImmaniTr/customer-churn-ml-api-v1)
- [customer-churn-ml-api-aws-v1](https://github.com/ImmaniTr/customer-churn-ml-api-aws-v1)
- [customer-churn-aws-deployment-v1](https://github.com/ImmaniTr/customer-churn-aws-deployment-v1)

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Author

**Immani Trejo**  
Data Science | Machine Learning | Cloud Deployment

Background in:
- IT consulting
- data analysis
- machine learning
- cloud-based deployment
- end-to-end ML workflows

---

## Recruiter Note

This repository demonstrates the modeling and experimentation phase of an end-to-end Machine Learning project.

The project evolved beyond experimentation into:
- API development
- cloud deployment
- monitoring
- CI/CD automation

showcasing the transition from traditional data science workflows to production-oriented machine learning engineering practices.
