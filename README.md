# Classification Model Comparison — Logistic Regression, KNN & Random Forest

## Project Overview

This project focuses on building and comparing multiple machine learning classification models to identify the best-performing model for a classification problem.

The project follows a complete machine learning workflow, starting with data cleaning and exploratory data analysis (EDA), followed by feature preparation, model training, prediction, and evaluation.

Three classification algorithms were implemented and compared:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest

A key part of the project was identifying and removing **725 duplicate records** from the dataset. Model performance was evaluated both before and after removing duplicates to understand how duplicate observations affected the results.

---

## Objectives

The main objectives of this project are:

- Understand and clean the dataset before applying machine learning.
- Identify and remove duplicate observations.
- Explore the data and understand relationships between features.
- Prepare the data for machine learning.
- Train multiple classification models.
- Compare model performance using multiple evaluation metrics.
- Select the best-performing model based on Accuracy, Precision, Recall, and F1-score.
- Understand how duplicate records can affect machine learning model performance.

---

## Project Workflow

The project follows these major steps:

1. **Data Collection**
2. **Data Understanding**
3. **Data Cleaning**
4. **Duplicate Detection and Removal**
5. **Exploratory Data Analysis**
6. **Feature Preparation**
7. **Train-Test Split**
8. **Model Training**
9. **Model Prediction**
10. **Model Evaluation**
11. **Model Comparison**
12. **Final Model Selection**

---

## Data Cleaning

Before building the machine learning models, the dataset was examined for common data-quality issues.

The following checks were performed:

- Missing values
- Duplicate records
- Data types
- Numerical and categorical variables
- Potential outliers
- Feature distributions

### Duplicate Records

A significant number of duplicate records were identified in the dataset.

**725 duplicate rows were removed** before the final model comparison.

Removing duplicates is important because repeated observations can cause a machine learning model to see essentially the same information multiple times. This can lead to overly optimistic evaluation results and may reduce the reliability of the model on unseen data.

---

## Exploratory Data Analysis

Exploratory Data Analysis was performed to better understand the dataset before modeling.

The analysis included:

- Distribution analysis
- Descriptive statistics
- Feature relationships
- Categorical variable analysis
- Target variable distribution
- Identification of unusual or duplicate observations

Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn were used for data exploration and visualization.

---

## Machine Learning Models

Three classification algorithms were implemented and compared.

### 1. Logistic Regression

Logistic Regression was used as a baseline classification model.

It is a simple and interpretable algorithm that works well when the relationship between the features and target variable can be represented effectively using a linear decision boundary.

### 2. K-Nearest Neighbors (KNN)

KNN classifies an observation based on the classes of its nearest neighboring observations.

The model was included to compare a distance-based approach against the linear Logistic Regression model and the tree-based Random Forest model.

### 3. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees to make predictions.

It can capture nonlinear relationships and interactions between features and was included to determine whether a more flexible model could improve classification performance.

---

## Model Evaluation

The models were evaluated using four important classification metrics:

### Accuracy

Accuracy measures the overall percentage of predictions that were classified correctly.

### Precision

Precision measures how many of the observations predicted as positive were actually positive.

A higher precision means fewer false-positive predictions.

### Recall

Recall measures how many of the actual positive observations were correctly identified by the model.

A higher recall means fewer false-negative predictions.

### F1-Score

F1-score provides a balance between Precision and Recall.

It is particularly useful when both false positives and false negatives are important.

---

## Final Model Results

After removing the 725 duplicate records, the models produced the following results:

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 77.05% | 93.10% | 69.23% | 79.41% |
| KNN | 77.05% | 89.66% | 70.27% | 78.79% |
| **Random Forest** | **85.25%** | **93.10%** | **79.41%** | **85.71%** |

---

## Model Comparison

### Logistic Regression

Logistic Regression achieved:

- Accuracy: **77.05%**
- Precision: **93.10%**
- Recall: **69.23%**
- F1-score: **79.41%**

The model had good precision but lower recall, meaning it was relatively good at avoiding false positives but missed a larger number of actual positive cases.

### KNN

KNN achieved:

- Accuracy: **77.05%**
- Precision: **89.66%**
- Recall: **70.27%**
- F1-score: **78.79%**

KNN performed similarly to Logistic Regression in terms of accuracy but had slightly lower precision and F1-score.

### Random Forest

Random Forest achieved:

- Accuracy: **85.25%**
- Precision: **93.10%**
- Recall: **79.41%**
- F1-score: **85.71%**

Random Forest achieved the highest Accuracy, Recall, and F1-score while also matching Logistic Regression's highest Precision.

---

## Final Model Selection

### Random Forest was selected as the final model.

The main reasons are:

- It achieved the **highest accuracy (85.25%)**.
- It achieved the **highest recall (79.41%)**.
- It achieved the **highest F1-score (85.71%)**.
- Its **precision of 93.10%** was tied for the highest among the models.
- It provided the best overall balance between precision and recall.

Therefore, based on the evaluation results, **Random Forest provides the strongest overall classification performance for this dataset**.

---

## Impact of Removing Duplicate Records

One of the important findings of this project was the impact of duplicate records on model performance.

Before duplicate removal, Random Forest achieved approximately:

- Accuracy: **98.54%**
- Precision: **97.09%**
- Recall: **100%**
- F1-score: **98.52%**

After removing 725 duplicate rows, performance changed to:

- Accuracy: **85.25%**
- Precision: **93.10%**
- Recall: **79.41%**
- F1-score: **85.71%**

The significant reduction in performance indicates that duplicate records were contributing to an overly optimistic evaluation.

This demonstrates why **data cleaning is an important part of a machine learning project**. A model should be evaluated on unique and representative observations so that its performance better reflects how it may behave on unseen data.

---

## Technologies Used

### Programming Language
- Python

### Data Manipulation
- Pandas
- NumPy

### Data Visualization
- Matplotlib
- Seaborn

### Machine Learning
- Scikit-learn

### Models
- Logistic Regression
- K-Nearest Neighbors
- Random Forest

### Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score
- Classification Report

---

## Project Structure

```text
Classification-Model-Comparison/
│
├── dataset/
│   └── dataset.csv
│
├── notebooks/
│   └── classification_model.ipynb
│
├── README.md
└── requirements.txt
```

---

## Key Learnings

Through this project, I gained practical experience in:

- Data cleaning and preprocessing
- Identifying duplicate observations
- Exploratory Data Analysis
- Preparing data for machine learning
- Building classification models
- Comparing multiple machine learning algorithms
- Understanding Accuracy, Precision, Recall, and F1-score
- Evaluating the effect of duplicate records on model performance
- Selecting a model based on multiple evaluation metrics
- Using Scikit-learn for end-to-end machine learning workflows

---

## Conclusion

This project demonstrates a complete classification workflow from **data preprocessing to final model selection**.

Although Random Forest initially showed extremely high performance, removing 725 duplicate records resulted in a more realistic evaluation. After cleaning the dataset, Random Forest continued to outperform Logistic Regression and KNN with an **85.25% accuracy and 85.71% F1-score**.

The project highlights an important machine learning principle: **good model performance depends not only on the algorithm but also on the quality and reliability of the data used to train and evaluate it.**

Based on the final evaluation, **Random Forest was selected as the best-performing model for this classification task.**
