# Airline Passenger Satisfaction Classification
This project focuses on predicting airline passenger satisfaction using supervised machine learning techniques. The goal is to analyze passenger-related features and build classification models that can accurately determine whether a passenger is satisfied or dissatisfied.

 ## Dataset
 **Source:** 
 
 [https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction/data]
 
 [https://www.kaggle.com/datasets/sjleshrac/airlines-customer-satisfaction]

 **Target Variable:** Satisfaction/Dissatisfaction


## Data Preprocessing

The following preprocessing steps were applied:

* Column name cleaning and reorganization

* Merging datasets

* Duplicate value detection and removal

* Missing value handling

* Feature encoding

* Feature scaling (for applicable models)

## Exploratory Data Analysis (EDA)

To better understand the dataset, multiple visualization techniques were used:

* Histograms for numerical features

* Count plots for categorical variables

* Box plots to detect outliers

* Correlation Analysis

These analyses helped identify feature distributions and potential data quality issues.

## Models Used

Three different classification models were implemented and compared:

* Logistic Regression (baseline model)

* K-Nearest Neighbors (KNN)

* Random Forest Classifier


## Overfitting Analysis

Overfitting was initially analyzed manually by comparing training and test set performance for all models.

* Logistic Regression showed stable generalization performance.

* KNN demonstrated sensitivity to the choice of k value.

* Random Forest exhibited clear signs of overfitting due to its high model complexity.

## Hyperparameter Optimization

To address overfitting observed in the Random Forest model, hyperparameter optimization was applied using GridSearchCV with 5-fold cross-validation.

A constrained parameter grid was used to explicitly control model complexity:

* Number of trees (n_estimators)

* Tree depth (max_depth)

* Minimum samples for node split and leaf nodes

This approach favored models with limited depth and improved generalization behavior.


## Model Evaluation

Model performance was evaluated using:

* Accuracy
* Precision/Recall/F1-score
* Confusion Matrix
* Learning Curve

Comparisons were performed before and after hyperparameter optimization for the Random Forest model. Results indicate a reduced gap between training and test performance after optimization.


## Model Performance & Comparison

| Model              | Accuracy | F1-score |
|-------------------|----------|----------|
| Logistic Regression | 0.82   | 0.83     |
| KNN                | 0.92     | 0.93     |
| Random Forest (Before Tuning) | 0.95 | 0.95 |
| Random Forest (After Tuning)  | 0.95 | 0.94 |

> Although the Random Forest model achieved similar test performance before and after tuning,
learning curve analysis revealed that hyperparameter optimization significantly reduced overfitting
by narrowing the gap between training and validation scores.


## Author
**Muhammed Doğru**  
Computer Engineering Student
