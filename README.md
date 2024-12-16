# COVID-19 Patient Risk Prediction

## Overview 
This project aims to build a machine learning model to predict the risk level of COVID-19 patients based on their current symptoms, status, and medical history. The main goal is to assist healthcare providers in efficiently allocating medical resources by identifying high-risk patients early on .

## Dataset
The dataset was provided by the Mexican government and contains anonymized patient-related information, including pre-existing conditions and outcomes. It consists of 21 unique features and data for 1,048,576 patients. Boolean features use 1 for "yes" and 2 for "no," with missing values indicated by 97-99.

### Key Features:
- **Sex:** 1 for female, 2 for male. 
- **Age:** Patient's age. 
- **Classification:** COVID-19 test results (1-3 for positive cases, 4+ for non-carriers or inconclusive results). 
- **Patient Type:** 1 for home care, 2 for hospitalization. 
- **Pneumonia, Diabetes, COPD, Asthma, Immunosuppressed, Hypertension, Cardiovascular, Renal Chronic, Other Disease, Obesity, Tobacco:** Indicates presence of these conditions (1 for yes, 2 for no). 
- **Medical Unit:** Type of healthcare institution. 
- **Date Died:** Date of death, with '9999-99-99' indicating survival.

## Project Workflow 
### 1. Data Preprocessing 
- Loaded and inspected the data. 
- Handled missing values and Boolean feature conversions. 
- Derived a new feature `DEATH` from the `DATE_DIED` column. 
- Dropped unnecessary columns and cleaned the data.

### 2. Data Visualization 
- Created bar charts to visualize patient data distribution over time.

### 3. Handling Class Imbalance 
- Split the dataset into training and testing sets. 
- Applied random under-sampling (RUS), random over-sampling (ROS), and SMOTE to balance the classes.

### 4. Model Training 
- Trained multiple classifiers: 
- Decision Tree (DTC) 
- Random Forest (RFC) 
- AdaBoost (ABC) 
- Gaussian Naive Bayes (GNB) 
- Logistic Regression

### 5. Model Evaluation 
- Evaluated models using accuracy, F1 score, precision, recall, ROC AUC, Matthews correlation coefficient, and Cohen’s kappa score. 
- Visualized results to compare classifier performance.

## Results 
- Provided a comprehensive comparison of various classifiers and sampling techniques. 
- Identified models and methods that perform best in predicting high-risk COVID-19 patients.

## Future Work 
- **Hyperparameter Tuning:** Further improve model performance. 
- **Feature Engineering:** Create new features for better prediction. 
- **Model Interpretation:** Use SHAP values to interpret model predictions and understand feature importance.

## How to Use 
### Prerequisites 
- Python 3.6+ 
- Required libraries: pandas, numpy, seaborn, matplotlib, scikit-learn, imbalanced-learn.

### Installation Clone the repository and install the required libraries: 
```shell 
git clone https://github.com/20pouya04/covid-risk-prediction.git 
cd covid-risk-prediction 
pip install -r requirements.txt
