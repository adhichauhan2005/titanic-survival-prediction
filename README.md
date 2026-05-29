# Titanic Survival Prediction

## Project Overview

This project was completed as part of Week 1 of an AI/ML internship program. The goal of the project was to practice the complete beginner machine learning workflow, including data loading, exploratory data analysis, data cleaning, feature engineering, model training, and model evaluation.

The project uses the Titanic dataset to predict whether a passenger survived based on passenger-level information such as gender, age, passenger class, fare, family size, and embarkation port.

## Dataset

Dataset used: Titanic Dataset from Kaggle

The dataset contains passenger-level information, including:

- Passenger class
- Gender
- Age
- Number of siblings/spouses aboard
- Number of parents/children aboard
- Fare
- Cabin
- Embarkation port
- Survival status

The target variable is `Survived`.

## Problem Type

This is a binary classification problem.

The target variable has two possible values:

- `0` = Passenger did not survive
- `1` = Passenger survived

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

1. Loaded and understood the dataset
2. Checked data types and missing values
3. Performed exploratory data analysis
4. Analyzed survival patterns by gender, passenger class, age, fare, embarked port, and family size
5. Cleaned missing values
6. Created new features
7. Converted categorical variables into numeric format
8. Trained baseline machine learning models
9. Evaluated models using accuracy, precision, recall, and F1 score
10. Selected the best baseline model

## Exploratory Data Analysis Findings

Key findings from EDA:

- Female passengers had a much higher survival rate than male passengers.
- First-class passengers had better survival chances than second- and third-class passengers.
- Passenger class and gender together showed strong survival patterns.
- Fare was right-skewed and appeared related to passenger class and survival.
- Family size appeared related to survival, so it was used for feature engineering.

## Data Cleaning and Feature Engineering

The following cleaning and feature engineering steps were performed:

- Missing `Age` values were filled using the median age.
- Missing `Embarked` values were filled using the mode.
- `Cabin` was dropped because it had many missing values.
- `FamilySize` was created using `SibSp + Parch + 1`.
- `IsAlone` was created to identify passengers traveling alone.
- `Title` was extracted from passenger names.
- Rare titles were grouped together.
- Categorical columns were converted into numeric dummy variables.

## Models Trained

Three baseline classification models were trained:

1. Logistic Regression
2. Decision Tree
3. Random Forest

## Model Performance

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------: | --------: | -----: | -------: |
| Logistic Regression |    0.849 |     0.850 |  0.739 |    0.791 |
| Random Forest       |    0.827 |     0.779 |  0.754 |    0.770 |
| Decision Tree       |    0.799 |     0.743 |  0.725 |    0.735 |

## Best Model

Logistic Regression performed best among the three baseline models.

It achieved:

- Accuracy: 0.849
- Precision: 0.850
- Recall: 0.739
- F1 Score: 0.791

Because Logistic Regression had the highest accuracy and F1 score, it was selected as the best baseline model.

## Final Conclusion

This project completed the full Week 1 machine learning workflow. The dataset was explored, cleaned, transformed, and used to train multiple baseline classification models.

The project helped build understanding of:

- Exploratory data analysis
- Missing value handling
- Feature engineering
- Train-test split
- Model training
- Model comparison
- Classification metrics

## Next Steps

Future improvements could include:

- Cross-validation
- Hyperparameter tuning
- ROC-AUC evaluation
- Additional feature engineering such as AgeGroup and FareGroup
- Testing predictions on Kaggle's test dataset
