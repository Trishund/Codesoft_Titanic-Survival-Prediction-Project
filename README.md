# Titanic Passenger Survival Prediction

This repository contains a machine learning pipeline developed to predict the survival of passengers aboard the Titanic. It is part of a series of projects undertaken during a Data Science internship at **CodSoft**.

## Project Overview

The objective of this project is to build a supervised machine learning model that predicts whether a passenger survived the Titanic disaster. This problem is a classic classification task using structured data. The solution employs a Random Forest Classifier and incorporates robust preprocessing and feature engineering techniques.

## Dataset

* **Source**: [Kaggle - Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)
* **Files Used**:

  * `train.csv`: Labeled training data
  * `test.csv`: Unlabeled test data for prediction
  * `gender_submission.csv`: Sample submission format

## Project Workflow

### Data Preprocessing

* **Handling Missing Values**:

  * `Age`: Mean imputation
  * `Fare`: Median imputation
  * `Embarked`: Mode imputation
* **Encoding**:

  * Categorical variables encoded using `OneHotEncoder`
* **Feature Scaling**:

  * Standardization of numerical features using `StandardScaler`

### Feature Engineering

New informative features were created to improve model performance:

* `FamilySize`: Combines `SibSp` and `Parch` to reflect total family size
* `IsAlone`: Binary indicator of whether the passenger was traveling alone
* `Title`: Extracted from the name to capture social status

### Model Building

* **Model Used**: `RandomForestClassifier`
* **Pipeline**: Preprocessing and classification are combined using `Pipeline`
* **Model Evaluation**:

  * Accuracy on training data
  * Cross-validation scores to check generalization
  * Feature importance analysis

### Output

* Predictions are saved as:

  * `titanic_predictions.csv`: Basic submission format
  * `titanic_predictions_detailed.csv`: Includes prediction probabilities and confidence

## Technologies Used

* Python 3.x
* Jupyter Notebook
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn
## Acknowledgments

* This project is one of the three required tasks for the **Data Science Internship at CodSoft**.
* I have actively used the **Data Science course by Krish Naik** and various **YouTube tutorials** to guide my learning and implementation throughout this project.

## Upcoming Tasks

As part of the CodSoft internship, I will also complete two additional data science projects:

1. **Movie Rating Prediction**
2. **Iris Flower Classification** (or another task from the provided list)
