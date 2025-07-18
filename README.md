# CODECRAFT_DS_02

# Internship Task 2

# 🛳️ Titanic - Machine Learning from Disaster 🚢

This repository contains my solution to the **Perform data cleaning and exploratory data analysis (EDA) on a Titanic dataset from Kaggle.**. The goal is to explore the relationships between variables and
identify patterns and trends in the data.


## 📁 Dataset

The dataset is provided by Kaggle and includes:

- `train.csv`: Training data with features and survival labels.
- `test.csv`: Test data (no survival labels).
- `gender_submission.csv`: A sample submission file.



## 🧪 Task

Predict survival (`0 = No`, `1 = Yes`) on the test set based on the training set.

## 📌 Project Highlights

| Stage                | Action                                                                 |
|---------------------|------------------------------------------------------------------------|
| ✅ Data Cleaning     | Handled missing values (`Age`, `Embarked`), removed unused columns     |
| 🛠 Feature Engineering | Encoded categorical features (`Sex`, `Embarked`)                      |
| 🤖 Model Training     | Used **RandomForest** from `scikit-learn`                       |
| 📈 EDA & Visualization | Visualized survival rates and age distribution using `seaborn`        |



## 🔍 Steps Followed

### ✅ 1. Data Loading & Inspection
- Loaded training and test CSV files using `pandas`.
- Checked for null values and basic statistics.

### 🔧 2. Data Cleaning
- Filled missing `Age` values with the median.
- Filled missing `Embarked` values with the mode.
- Dropped unused columns: `Cabin`, `Ticket`, and `Name`.

### 🧬 3. Feature Engineering
- Converted categorical columns:
  - `Sex` → `SexLabel` (0 for male, 1 for female).
  - `Embarked` → `EmbarkedLabel` (label encoded).
- Final features used: `Pclass`, `SexLabel`, `Age`, `SibSp`, `Parch`, `Fare`, `EmbarkedLabel`.

### 🤖 4. Model Training
- Model Used: **Logistic Regression**
- Trained the model on cleaned training data.
- Achieved validation accuracy around **0.82**.

(((- ⚙️ Model Building
Algorithm: Random Forest
Target Variable: Survived

Features Used:

Pclass

SexLabel (0 = male, 1 = female)

Age

SibSp

Parch

Fare

EmbarkedLabel

🧪 Validation Accuracy: ~82.34%
)))


### 📈 5. Prediction & Submission
- Predicted survival values on test data.
- Created submission file with:
  - `PassengerId`
  - `Survived`
- Saved as `submission.csv` and submitted to Kaggle.

---

## 📊 Visualizations

- **Survival Count by Gender**  
  `sns.countplot(x='Survived', hue='Sex', data=train_df)`

- **Age Distribution of Passengers**  
  `sns.histplot(train_df['Age'].dropna(), bins=30, kde=True)`


## 📦 Libraries Used

- Python 3.x
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn

⭐️ If you liked this project, consider giving it a star!

