# Titanic Survival Prediction using Machine Learning
 This project is based on the famous Titanic dataset from Kaggle. The goal is to predict passenger survival based on features like class, gender, age, and family relations using machine learning models like Logistic Regression and Random Forest.

## Dataset Info
Source: Kaggle Titanic Dataset

Rows: 891

Columns: 12

Target: Survived (0 = No, 1 = Yes)

## Data Preprocessing
Handled missing values in:
 * Age: filled with mean (29.7)
 * Embarked: filled with mode
 * Cabin: dropped due to ~77% missing values

Converted categorical features (Sex, Embarked) using one-hot encoding

Selected relevant features for training:
Survived, Pclass, Sex, Age, SibSp, Parch, Embarked

## Exploratory Data Analysis
Boxplots and descriptive statistics used to understand data distribution

Pclass, Sex, and Age were found to be highly correlated with survival

Family-related features (SibSp, Parch) analyzed

## Models Used
* Random Forest Classifier
* Logistic Regression

## Model Evaluation
Metric	Random Forest	Logistic Regression
Accuracy	0.83	0.83
Precision	0.85	0.85
Recall	0.72	0.72
F1 Score	0.78	0.78
Classification Report (Both Models):
markdown

        precision    recall  f1-score   support
           0       0.82      0.91      0.86       105
           1       0.85      0.72      0.78        74
           
    accuracy                           0.83       179
    macro avg       0.84      0.82      0.82       179
    weighted avg       0.83      0.83      0.83       179

Confusion Matrix:
[[96  9]
 [21 53]]

 
## Conclusion
Both Random Forest and Logistic Regression achieved 83% accuracy

Precision and F1 Score are higher for class 1 (survived), but recall is slightly lower

Could be improved with:

Hyperparameter tuning

Feature engineering

Ensemble models
