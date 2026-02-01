# AI-NOW-Capstone-AI-ML-Project

---


# Insurance Claim Prediction

## Project Overview

In the insurance sector, accurately predicting which buildings are likely to file claims is crucial for risk management and pricing strategies. This project develops a predictive machine learning model to estimate the **probability of a building filing at least one insurance claim** during its insured period. By analyzing structural, occupancy, and location-related characteristics of buildings, this model helps insurers proactively identify high-risk properties and make data-driven decisions.

The problem is framed as a **binary classification task**, where the target variable `Claim` indicates:
- `1` → At least one claim occurred
- `0` → No claims occurred

---

## Dataset Description

The dataset contains historical information on buildings and their associated insurance claims. Features include:

- **Numerical features**: Building dimensions, age, occupancy details, and exposure metrics.
- **Categorical features**: Building type, occupancy type, geographical code, and other descriptive attributes.
- **Target variable**: `Claim` – whether the building experienced at least one insurance claim.

A separate variable description file accompanies the dataset to clarify each feature’s meaning and ensure correct preprocessing and interpretation.

---

## Methodology

The project follows an end-to-end machine learning workflow:

1. **Data Exploration & Cleaning**  
   - Inspect data structure, types, and missing values.  
   - Handle missing data: median imputation for numerical features and a placeholder category for categorical features.  
   - Remove duplicates to ensure data integrity.

2. **Exploratory Data Analysis (EDA)**  
   - Visualize numerical and categorical features against the target to uncover patterns.  
   - Check correlations among numerical features to detect potential multicollinearity.

3. **Feature Preprocessing**  
   - Numerical features are scaled using StandardScaler.  
   - Categorical features are encoded via OneHotEncoder.  
   - A preprocessing pipeline ensures transformations are applied consistently, preventing data leakage.

4. **Model Training & Evaluation**  
   - Split data into training and testing sets with stratification to preserve class distribution.  
   - Train multiple models to evaluate predictive performance.  

5. **Model Interpretation & Comparison**  
   - Compare models using ROC-AUC, accuracy, and classification metrics.  
   - Identify best-performing model and discuss feature influence on claim likelihood.

---

## Models Used

Two machine learning models were implemented:

1. **Logistic Regression**  
   - Serves as a baseline model.  
   - Interpretable coefficients provide insights into feature contributions.  

2. **Random Forest Classifier**  
   - Captures complex, non-linear relationships between features and the target.  
   - Ensemble approach improves predictive robustness and overall performance.

---

## Evaluation Metrics

Model performance is assessed using:

- **Accuracy**: Percentage of correctly classified instances.  
- **ROC-AUC (Receiver Operating Characteristic – Area Under Curve)**: Measures the model’s ability to distinguish between claim and non-claim cases.  
- **Classification Report**: Includes precision, recall, and F1-score to evaluate per-class performance.  

ROC-AUC is emphasized due to the potential class imbalance, which is common in insurance datasets where claims are less frequent.

---

## How to Run the Notebook

1. Clone the repository:

```bash
git clone <your-repository-link>
cd insurance-claim-prediction
````

2. Install required packages:

```bash
pip install -r requirements.txt
```

3. Launch the notebook:

```bash
jupyter notebook notebooks/insurance_claim_prediction.ipynb
```

4. Execute cells sequentially to reproduce the analysis, modeling, and evaluation.

---

## Final Remarks

This project demonstrates an **end-to-end machine learning pipeline** applied to a real-world insurance problem. The Random Forest model provided the strongest predictive performance, highlighting complex interactions between building characteristics and claim likelihood. Insurers can leverage these insights to enhance risk assessment, optimize pricing, and implement proactive loss prevention strategies.

```

