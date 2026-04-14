# Burnout-Driven Job Switching Prediction

## Overview

This project analyzes mental health and burnout patterns among professionals in the tech industry using a synthetic dataset sourced from Kaggle. The objective is to identify key factors contributing to burnout and predict whether an employee is likely to switch jobs.

The project demonstrates an end-to-end data science workflow including:

* Exploratory Data Analysis (EDA)
* Data cleaning and validation
* Feature engineering
* Classification modeling (Logistic Regression)
* Model tuning and evaluation
* Feature importance interpretation

---

## Problem Statement

Burnout and poor mental health are significant concerns in the tech industry. This project aims to:

* Analyse behavioral and workplace factors influencing burnout
* Identify patterns in job satisfaction and work-life balance
* Predict whether an employee is likely to leave their job ("will_switch")

---

## Dataset

* **Source:** Kaggle (Synthetic Dataset)
* **File Used:** `tech_mental_health_burnout.csv`

### Key Features

* Demographics: Age, Gender, Experience
* Mental Health: Stress, Anxiety, Depression Scores
* Work Metrics: Work hours, Overtime, Meetings
* Lifestyle: Sleep, Physical Activity, Screen Time
* Workplace Factors: Company Size, Work Mode, Manager Support

---

## Data Preprocessing

* Checked for missing values and duplicates
* Identified invalid entries (e.g., experience > age)
* Explored distributions using boxplots
* Analysed categorical feature uniqueness
* Created pivot tables for demographic insights

---

## Exploratory Data Analysis (EDA)

* Boxplots for:

  * Work hours
  * Overtime hours
  * Job satisfaction
  * Work-life balance
  * Manager support
* Correlation heatmap for numerical variables
* Grouped analysis by job roles
* Identified high-risk burnout groups

---

## Feature Engineering

A target variable **`will_switch`** was created based on:

* Low job satisfaction
* Poor work-life balance
* Moderate/High burnout levels
* High overtime hours
* Startup work environment

This resulted in a **binary classification problem**.

---

## Model Development

### Data Splitting

* Train: 60%
* Validation: 20%
* Test: 20%
* Stratified sampling used to handle class imbalance

### Baseline Model

* Logistic Regression with class balancing

### Pipeline

* StandardScaler for normalization
* Logistic Regression classifier

### Hyperparameter Tuning

* GridSearchCV with 5-fold cross-validation
* Optimized for **F1-score**

Parameters tuned:

* Regularisation strength (C)
* Class weights

---

## Model Evaluation

Metrics used:

* Precision, Recall, F1-score
* Confusion Matrix
* ROC-AUC Score

### Threshold Tuning

* Adjusted decision threshold to improve recall vs precision trade-off

### Evaluation Stages

* Validation set performance
* Final test set performance

---

## Feature Importance

Extracted coefficients from Logistic Regression to identify:

### Top Positive Factors (Increase Switching)

* High burnout score
* High stress and anxiety
* Increased overtime hours
* Poor sleep and work-life balance

### Top Negative Factors (Reduce Switching)

* Strong social support
* Better physical activity levels
* Higher job satisfaction

---

## Key Insights

* Employees with high burnout and low satisfaction are significantly more likely to switch jobs
* Overtime and poor work-life balance are strong predictors of attrition
* Manager support and social support play a critical role in retention
* Startup environments show higher switching tendencies

---

## Project Structure

```
Tech-Mental-Health/
│── data/
│   ├── tech_mental_health_burnout.csv
│
│── notebook.ipynb / script.py
│── README.md
```

---

## Technology Stack

* **Python**
* **Pandas, NumPy** – Data manipulation
* **Matplotlib, Seaborn** – Data visualization
* **Scikit-learn** – Machine learning and evaluation

---

## Installation

```bash
git clone https://github.com/your-username/tech-mental-health.git
cd tech-mental-health
pip install -r requirements.txt
```

---

## Usage

Run the notebook or script:

```bash
python script.py
```

---

## Future Improvements

* Apply advanced models (Random Forest, XGBoost)
* Handle class imbalance using SMOTE
* Deploy as an interactive dashboard (Streamlit)
* Integrate real-world datasets
* Add explainability using SHAP or LIME

---

## Author

**Jigisha Tomar**
[LinkedIn](http://www.linkedin.com/in/jigishatomar)
[GitHub](https://github.com/jigisha789)

---

## License

This project is licensed under the MIT License.

