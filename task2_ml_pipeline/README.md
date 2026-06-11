# Task 2: End-to-End ML Pipeline (Churn Prediction)

## Objective
The goal of this project is to build a reusable, production-ready machine learning pipeline to predict customer churn using the Telco Churn dataset.

## Methodology / Approach
1. **Data Preprocessing:** Engineered a comprehensive Scikit-learn preprocessing pipeline using `ColumnTransformer` to handle missing values, scale numeric features (`StandardScaler`), and encode categorical variables (`OneHotEncoder`).
2. **Model Training:** Integrated the preprocessor with baseline models, specifically training both Logistic Regression and Random Forest classifiers.
3. **Hyperparameter Tuning:** Utilized `GridSearchCV` to systematically tune the hyperparameters of the Random Forest model (e.g., number of estimators, max depth).
4. **Evaluation:** Compared models using classification reports, confusion matrices, and ROC curves.
5. **Deployment Readiness:** Exported the final, optimized pipeline as a single reproducible artifact using `joblib`.

## Key Results & Observations
* **Performance:** The tuned Random Forest model outperformed the baseline, achieving an accuracy of ~82% and an ROC-AUC score of ~0.87.
* **Feature Importance:** Tenure, Monthly Charges, and Total Charges were identified as the strongest numerical predictors for churn. Categorically, month-to-month contracts showed the highest churn risk.
* **Pipeline Efficiency:** Encapsulating both the preprocessing steps and the model into a single `joblib` file ensures seamless inference on new, raw data in a production environment.