# Bank Marketing Prediction Project

This project focuses on building a machine learning model to predict whether a client of a Portuguese banking institution will subscribe to a term deposit (`y`). The dataset originates from direct marketing campaigns (telephone calls) and is available on [Kaggle](https://www.kaggle.com/datasets/sahistapatel96/bankadditionalfullcsv). The file used in this repository is **`bank-additional-full.csv`**.

---

## Project Overview

The task is a **binary classification problem**, where the target variable `y` indicates whether a client subscribed to a term deposit (`yes`/`no`).  
The project includes a complete pipeline: **exploratory data analysis, preprocessing, model training, hyperparameter optimization, model explainability, and error analysis**.

---

## Dataset Description

The dataset contains information grouped into several categories:

### Client Information
- **age** – age of the client (numeric)  
- **job** – type of job (categorical: `admin.`, `blue-collar`, `entrepreneur`, `housemaid`, `management`, `retired`, `self-employed`, `services`, `student`, `technician`, `unemployed`, `unknown`)  
- **marital** – marital status (`divorced`, `married`, `single`, `unknown`)  
- **education** – level of education (`basic.4y`, `basic.6y`, `basic.9y`, `high.school`, `illiterate`, `professional.course`, `university.degree`, `unknown`)  
- **default** – has credit in default? (`yes`, `no`, `unknown`)  
- **housing** – has a housing loan? (`yes`, `no`, `unknown`)  
- **loan** – has a personal loan? (`yes`, `no`, `unknown`)  

### Current Campaign
- **contact** – type of communication used (`cellular`, `telephone`)  
- **month** – last contact month (`jan`, `feb`, …, `nov`, `dec`)  
- **day_of_week** – last contact day of the week (`mon`, `tue`, `wed`, `thu`, `fri`)  
- **duration** – last contact duration, in seconds (numeric)  
  ⚠ *Important*: this variable is highly correlated with the outcome but is not known before the call, therefore it is excluded from the final predictive model and used only for comparison purposes.  

### Campaign History
- **campaign** – number of contacts during this campaign for this client  
- **pdays** – number of days since the client was last contacted (999 means never contacted before)  
- **previous** – number of contacts before this campaign  
- **poutcome** – outcome of the previous campaign (`failure`, `nonexistent`, `success`)  

### Socioeconomic Indicators
- **emp.var.rate** – employment variation rate (quarterly)  
- **cons.price.idx** – consumer price index (monthly)  
- **cons.conf.idx** – consumer confidence index (monthly)  
- **euribor3m** – Euribor 3 month rate (daily)  
- **nr.employed** – number of employees (quarterly)  

### Target
- **y** – has the client subscribed a term deposit? (`yes`, `no`)  

---

## Workflow

The following steps were carried out:

### 1. Exploratory Data Analysis (EDA)
- Analysis of distributions, correlations, and relationships between features and the target variable  
- Hypotheses generation about feature impact on the subscription outcome  

### 2. Preprocessing
- Encoding of categorical variables  
- Grouping of categories where appropriate  
- Handling of missing values and `"unknown"` categories  
- Outlier detection and treatment  
- Feature engineering to create additional informative variables  

### 3. Model Training
- Logistic Regression  
- k-Nearest Neighbors (kNN)  
- Decision Tree  
- Boosting algorithms (e.g., XGBoost, LightGBM, CatBoost)  

### 4. Model Evaluation
- Comparison of models using appropriate metrics (AUC, F1-score, accuracy)  
- Cross-validation to assess stability  
- A results table summarizing model performance, hyperparameters, and evaluation metrics  

### 5. Hyperparameter Optimization
- Randomized Search (Scikit-learn)  
- Bayesian Optimization (Hyperopt)  
- Comparison of tuning results and discussion of model improvements  

### 6. Feature Importance & Explainability
- Analysis of feature importance for the best-performing model  
- SHAP (SHapley Additive exPlanations) analysis to interpret predictions  

### 7. Error Analysis
- Examination of misclassified records  
- Discussion of potential improvements to the solution  

---

## Results
- A comparative table of different models with their metrics  
- Identification of the most promising model after hyperparameter tuning  
- Insights into the most important features driving model predictions  
- SHAP visualizations for model interpretability  
