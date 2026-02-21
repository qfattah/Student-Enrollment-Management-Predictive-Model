# Enrollment Yield Prediction Using Logistic Regression and Decision Trees

This project develops predictive models to identify prospective students most likely to enroll as new freshmen using the INQ2021 dataset. The analysis includes data cleaning, preprocessing, feature engineering, multicollinearity assessment, and classification modeling to support data-driven enrollment management decisions.

You can review the code here:  
[INQ2021_Enrollment_Modeling]()

---

## Table of Contents
- [Introduction](#introduction)
- [Setup](#setup)
- [Data Preparation](#data-preparation)
- [Feature Engineering](#feature-engineering)
- [Multicollinearity Assessment](#multicollinearity-assessment)
- [Modeling Approach](#modeling-approach)
- [Conclusion](#conclusion)

---

## Introduction

In Fall 2022, university leadership sought to improve enrollment forecasting by identifying which prospective students were most likely to enroll. Historically, the university received over 90,000 inquiries and enrolled approximately 2,400–2,800 freshmen each year.

This project uses Fall 2021 inquiry data (INQ2021) to build predictive classification models.

The workflow includes:

1. **Data Importation** – Loading the INQ2021 dataset into Python.
2. **Data Cleaning & Variable Selection** – Removing irrelevant, constant, and ethically sensitive variables.
3. **Missing Value Treatment** – Handling missing data using mean and mode imputation.
4. **Feature Engineering** – Creating dummy variables and applying log transformations.
5. **Multicollinearity Analysis** – Using Variance Inflation Factor (VIF) to assess predictor redundancy.
6. **Model Development** – Applying logistic regression and decision tree classification models.
7. **Model Evaluation** – Comparing performance to support enrollment strategy decisions.

---

## Setup

### Prerequisites
- Python 3.x
- Jupyter Notebook

### Libraries

Install required libraries using pip:

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
