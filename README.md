# Enrollment Yield Prediction | Logistic Regression & Decision Tree Modeling

## Project Overview

This project develops predictive classification models to identify prospective students most likely to enroll as freshmen using the **INQ2021** inquiry dataset.

Universities often receive tens of thousands of inquiries but enroll only a small fraction of students. Accurate yield prediction enables enrollment management teams to:

- Prioritize outreach efforts
- Allocate recruiting resources efficiently
- Improve forecasting accuracy
- Optimize scholarship and engagement strategy

This project builds an end-to-end predictive pipeline using logistic regression and decision tree models to estimate enrollment probability.

---

## Business Context

- ~90,000 annual inquiries  
- ~2,400–2,800 enrolled freshmen  
- Target variable: **Enroll (0/1)**  

The objective is to predict which inquiry students are most likely to convert to enrolled students, enabling data-driven decision making.

---

## Technical Approach

### 1. Data Preparation

**Dataset:** `inq2021.csv`

Steps performed:

- Removed constant and administrative variables
- Excluded ethically sensitive features (`ETHNICITY`, `sex`)
- Dropped high-missingness variables (>50%)
- Imputed missing numerical values using mean
- Imputed categorical values using mode
- Confirmed zero remaining missing values

This ensures ethical modeling practices and clean feature inputs.

---

### 2. Feature Engineering

- Created dummy variables for categorical features (`TERRITORY`, `Instate`)
- Excluded reference categories to prevent perfect multicollinearity
- Evaluated skewness using histograms
- Applied log transformation to:
  - `TOTAL_CONTACTS`
  - `avg_income`
  - `distance`

This improved distribution normality and model stability.

---

### 3. Multicollinearity Control (VIF)

Variance Inflation Factor (VIF) was computed for all predictors.

Features with **VIF > 10** were removed:

- `TOTAL_CONTACTS`
- `mailq`
- `distance`
- `avg_income`

Reducing multicollinearity improves:
- Coefficient interpretability
- Statistical stability
- Model generalizability

---

### 4. Model Development

Data was split into:

- 70% Training  
- 30% Validation  

#### Logistic Regression (Statsmodels Logit)

- Interpretable probabilistic model
- Coefficient significance analysis
- Enrollment probability scoring

#### Decision Tree (Scikit-learn)

- Captures nonlinear relationships
- Provides rule-based segmentation
- Visualizable decision structure

---

## Model Evaluation

Both models were evaluated using:

- Confusion Matrix
- ROC Curve
- ROC-AUC Score

Metrics used:

- True Positive Rate
- False Positive Rate
- Area Under Curve (AUC)

ROC curves were plotted to visually compare model performance.

---

## Key Skills Demonstrated

- Data Cleaning & Preparation  
- Ethical Feature Selection  
- Missing Value Imputation  
- Feature Engineering  
- Multicollinearity Diagnosis (VIF)  
- Logistic Regression Modeling  
- Decision Tree Modeling  
- Model Evaluation (ROC-AUC, Confusion Matrix)  
- Train/Test Splitting & Validation  

---

## Impact & Practical Application

This framework can be used by enrollment teams to:

- Rank prospects by enrollment likelihood  
- Prioritize high-probability students  
- Optimize marketing and recruiting spend  
- Improve yield forecasting  

The approach is scalable and can be extended with cross-validation, hyperparameter tuning, and production deployment pipelines.

---

## Future Enhancements

- K-Fold Cross Validation
- Hyperparameter tuning (GridSearch)
- Feature importance comparison
- Model calibration analysis
- Deployment-ready probability scoring system

---

## Tools & Libraries

- Python
- Pandas
- NumPy
- Statsmodels
- Scikit-learn
- Matplotlib

---

## Author

Qusai Fattah  
Advanced Business Analytics | Predictive Modeling | Data-Driven Decision Making
