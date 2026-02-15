# Breast_Cancer_Prediction
Implement multiple classification models - Build an interactive Streamlit web application


# Breast Cancer Prediction Project

This project implements and evaluates six different classification models (Logistic Regression, Decision Tree, K-Nearest Neighbor, Naive Bayes, Random Forest, and XGBoost) to predict breast cancer based on the Breast Cancer Wisconsin (Diagnostic) dataset from the UCI Machine Learning Repository.

## Installation

To set up the project locally, clone the repository and install the required dependencies:

```bash
git clone <your-repo-url>
cd project-folder
pip install -r requirements.txt
```

## Usage

To run the Streamlit application, navigate to the `project-folder` directory and execute:

```bash
streamlit run app.py
```

## Problem statement

Implements and evaluates six different classification models (Logistic Regression, Decision Tree, K-Nearest Neighbor, Naive Bayes, Random Forest, and XGBoost) to predict breast cancer based on the Breast Cancer Wisconsin (Diagnostic)

Deploy an streamlit app with interactive user interface which can provide the description of model performance and also capble of predicted whether a cancer is Benign or Malignant based on parameters of the patient

## Dataset description

Breast Cancer Wisconsin Diagnostic Datset was used to train the 6 models.The datset conttains contains 569 instances with 30 real‑valued features, and the target variable indicates whether the tumor is benign or malignant.

# Models used and their Performance Metrics Comparison

| ML Model Name       | Accuracy | AUC Score | Precision | Recall | F1 Score | MCC Score |
|---------------------|----------|-----------|-----------|--------|----------|-----------|
| Logistic Regression | 0.9737   | 0.9974    | 0.9722    | 0.9859 | 0.9790   | 0.9439    |
| Decision Tree       | 0.9474   | 0.9440    | 0.9577    | 0.9577 | 0.9577   | 0.8880    |
| K-Nearest Neighbor  | 0.9474   | 0.9817    | 0.9577    | 0.9577 | 0.9577   | 0.8880    |
| Naive Bayes         | 0.9649   | 0.9974    | 0.9589    | 0.9859 | 0.9722   | 0.9253    |
| Random Forest       | 0.9649   | 0.9953    | 0.9589    | 0.9859 | 0.9722   | 0.9253    |
| XGBoost             | 0.9561   | 0.9908    | 0.9583    | 0.9718 | 0.9650   | 0.9064    |


## Observations on the performance of each model

| ML Model Name             | Observation about model performance                                                                 |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| Logistic Regression       | Delivered the best overall performance across all metrics. Highest accuracy (0.9737), near-perfect AUC (0.9974), top precision (0.9722), recall (0.9859), F1 (0.9790), and MCC (0.9439). Very few errors (3 false positives, 2 false negatives). Strengths: simple, interpretable, and highly effective. Weaknesses: may struggle with highly non-linear data, though not an issue here. |
| Decision Tree             | Achieved good accuracy (>0.94) but lowest AUC (0.9440) and MCC (~0.89). Errors slightly higher (3 false positives, 3 false negatives). Strengths: highly interpretable and easy to understand. Weaknesses: prone to overfitting, rigid decision boundaries, and less robust generalization compared to ensemble methods. |
| kNN                       | Accuracy above 0.94 with balanced errors (3 false positives, 3 false negatives). Strengths: simple, non-parametric, intuitive. Weaknesses: computationally expensive for large datasets, sensitive to feature scaling and noisy data, less robust than global models. Performance comparable to Decision Tree but less consistent. |
| Naive Bayes               | Excellent performance with accuracy >0.94, AUC (0.9974), and recall (0.9859). Very few errors (3 false positives, 2 false negatives). Strengths: fast, efficient, handles high-dimensional data well. Weaknesses: assumes feature independence, which can be limiting in other datasets, but worked well here. Overall highly competitive. |
| Random Forest (Ensemble)  | Strong and consistent performance: accuracy >0.94, AUC (0.9953), recall (0.9859), MCC (0.9253). Errors low (3 false positives, 2 false negatives). Strengths: robust, reduces overfitting via ensembling, provides feature importance. Weaknesses: less interpretable than Logistic Regression. Excellent balance of metrics. |
| XGBoost (Ensemble)        | High accuracy (>0.94), strong AUC (0.9908), and good overall metrics, though slightly lower recall and MCC compared to Logistic Regression, Naive Bayes, and Random Forest. Errors: 3 false positives, 4 false negatives. Strengths: powerful boosting algorithm, excels on complex datasets. Weaknesses: computationally intensive, marginally edged out by simpler models here. |






