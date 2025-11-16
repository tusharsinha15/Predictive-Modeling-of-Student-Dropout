

🎓 JEE Dropout Risk Prediction

 Project Overview
This repository presents a machine learning project dedicated to predicting student dropout risk after Class 12, specifically targeting aspirants preparing for highly competitive exams like the JEE. The primary objective is to build an effective classification model that identifies students at risk of dropping out based on a diverse set of academic, socio-economic, and personal factors.

 Methodology

 1. Data Preprocessing
The dataset, comprising 5,000 student records, was preprocessed to prepare it for machine learning. Key steps included:
* **Handling Categorical Features:** One-hot encoding was applied to all categorical columns (e.g., `school_board`, `family_income`, `parent_education`) to convert them into a suitable numerical format for the models.
* **Data Splitting:** The data was split into 80% for training (4,000 samples) and 20% for testing (1,000 samples). A stratified split was used to ensure the dropout ratio (approximately 21%) was maintained across both sets.
* **Feature Scaling:** Numerical features were standardized using `StandardScaler`, which is essential for algorithms like Logistic Regression.

 2. Model Implementation and Evaluation
Three robust classification models were implemented and compared:
1.  **Logistic Regression:** A linear model providing baseline performance and coefficient insights.
2.  **Random Forest Classifier:** An ensemble tree-based model known for high accuracy and implicit feature selection.
3.  **Gradient Boosting Classifier:** A powerful ensemble technique that builds models sequentially, correcting errors of previous models.

The models were evaluated using standard classification metrics: **Accuracy, Precision, Recall, and F1-Score**.

 Key Findings

 Top Performing Model
The **Gradient Boosting Classifier** achieved the highest performance, demonstrating exceptional predictive capability with a superior **Accuracy** and a nearly perfect **F1-Score** and **Precision** on the test data. This model proved to be highly effective at correctly identifying both dropout and non-dropout cases.

 Most Impactful Predictors
Analysis of the feature importance scores from the tree-based models (Random Forest and Gradient Boosting) highlighted critical factors driving dropout risk:

* **Admission Status:** The primary predictor was the student's status regarding **admission taken** (`admission_taken_Yes`).
* **Socio-economic Status:** Students categorized under **Low Family Income** (`family_income_Low`) showed a very high correlation with dropout, underscoring the influence of financial background.
* **Study Habits and External Pressure:** **Daily study hours** was a significant numerical factor, with lower hours strongly linked to dropout. Additionally, the student's perception of **peer pressure** (Low/Medium levels) was found to be highly influential in the prediction.

 Usage
The `DROPOUT1.py` file contains the complete machine learning pipeline, including data loading, preprocessing, model training, evaluation, and feature importance analysis. The accompanying notebook contains the initial Exploratory Data Analysis (EDA) visualizations.

***
