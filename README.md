# Student-Performance-Analysis-
End-to-end Student Performance ML project using EDA, Linear Regression, and Logistic Regression to analyze and predict exam performance and student Pass/Fail outcomes.


# 🎓 Student Performance Analysis & Machine Learning

An end-to-end Machine Learning project that analyzes student habits, academic behavior, and personal factors to understand and predict **exam performance**.

The project follows a complete Data Science workflow — from **Exploratory Data Analysis (EDA)** and data preprocessing to **Regression and Classification**, model evaluation, interpretation, and business-style insights.

---

## 📌 Project Overview

Student academic performance can be influenced by several factors such as:

* 📚 Study hours
* 🏫 Attendance
* 😴 Sleep duration
* 📱 Social media usage
* 🎬 Netflix usage
* 🏃 Exercise frequency
* 🧠 Mental health rating
* 👨‍👩‍👧 Parental education
* 💻 Other lifestyle and academic factors

This project investigates these relationships and builds Machine Learning models to answer two important questions:

1. **Regression:** Can we predict a student's `exam_score`?
2. **Classification:** Can we predict whether a student will **Pass or Fail** based on a 50-mark threshold?

---

## 🎯 Project Objectives

* Understand the structure and quality of the student dataset.
* Perform detailed Exploratory Data Analysis.
* Identify numerical and categorical variables.
* Analyze distributions and relationships between variables.
* Detect missing values, duplicates, and potential outliers.
* Identify factors associated with exam performance.
* Prepare the dataset for Machine Learning.
* Build a Linear Regression model for exam-score prediction.
* Convert exam scores into Pass/Fail categories.
* Build a classification model for Pass/Fail prediction.
* Evaluate both models using appropriate metrics.
* Compare training and testing performance.
* Check for overfitting and underfitting.
* Generate meaningful conclusions about student performance.

---

## 📂 Dataset

**Dataset:** Student Habits & Performance Dataset

The dataset contains student-level information related to academic habits, lifestyle behavior, and exam performance.

### Target Variable

For Regression:

`exam_score`

For Classification:

`Pass_Fail`

where:

* `exam_score >= 50` → **Pass**
* `exam_score < 50` → **Fail**

---

## 🔍 Exploratory Data Analysis

The notebook performs a detailed EDA covering:

### Dataset Understanding

* Dataset shape
* First and last records
* Random samples
* Column names
* Data types
* Numerical variables
* Categorical variables
* Unique values

### Data Quality

* Missing-value analysis
* Duplicate-record detection
* Invalid-value checks
* Data-type validation
* Range validation
* Potential outlier identification

### Statistical Analysis

The project examines:

* Mean
* Median
* Standard deviation
* Minimum and maximum values
* Quartiles
* IQR
* Distribution characteristics

### Visual Analysis

Visualizations include:

* Histograms
* Boxplots
* Bar charts
* Count plots
* Scatter plots
* Correlation heatmap
* Actual vs. predicted plots
* Residual plots

---

## 📊 Important EDA Variables

Particular attention is given to factors that may influence `exam_score`, including:

* `study_hours_per_day`
* `attendance_percentage`
* `sleep_hours`
* `social_media_hours`
* `netflix_hours`
* `exercise_frequency`
* `mental_health_rating`
* `parental_education_level`

The analysis compares these variables with exam performance to identify meaningful patterns and relationships.

---

## 🧹 Data Preprocessing

Before Machine Learning, the data is prepared using an appropriate preprocessing pipeline.

### Numerical Features

Numerical variables are:

* Checked for missing values
* Imputed where necessary
* Standardized when required

### Categorical Features

Categorical variables are:

* Checked for missing values
* Imputed using the most frequent category
* Converted into numerical form using One-Hot Encoding

### Feature Selection

`student_id` is excluded because it is an identifier rather than a meaningful predictive feature.

For both models, `exam_score` is excluded from the input features to prevent **target leakage**.

---

# 📈 Regression Model

## Linear Regression

A Linear Regression model is trained to predict the continuous `exam_score`.

The model uses relevant student habit, lifestyle, and demographic variables.

### Evaluation Metrics

The regression model is evaluated using:

* **MAE — Mean Absolute Error**
* **RMSE — Root Mean Squared Error**
* **R² Score — Coefficient of Determination**

These metrics help determine how accurately the model predicts exam scores.

---

# 🎯 Classification Model

## Pass/Fail Prediction

The continuous `exam_score` is converted into a binary classification target.

| Exam Score | Result |
| ---------- | ------ |
| `>= 50`    | Pass   |
| `< 50`     | Fail   |

A **Logistic Regression** model is then trained to predict the student's Pass/Fail outcome.

### Classification Metrics

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Classification Report

---

## 📉 Confusion Matrix

The confusion matrix helps identify:

* True Positives
* True Negatives
* False Positives
* False Negatives

This provides a deeper understanding of how well the model distinguishes between students who pass and fail.

---

# ⚖️ Model Performance Comparison

Training and testing performance is compared to determine whether the models generalize well to unseen data.

The project specifically checks for:

### Overfitting

When the model performs significantly better on training data than testing data.

### Underfitting

When the model performs poorly on both training and testing data.

### Good Generalization

When training and testing performance are reasonably close.

---

# 💡 Key Insights

The analysis produces five major student-performance insights based on the actual dataset and model results.

Examples of the types of findings investigated include:

1. **Study habits and academic performance**
   Students who spend more time studying tend to achieve higher exam scores.

2. **Attendance and performance**
   Attendance is analyzed to determine whether consistent classroom participation is associated with better results.

3. **Lifestyle balance**
   Sleep, exercise, and entertainment usage are examined to understand their relationship with academic outcomes.

4. **Digital entertainment and study behavior**
   Social media and Netflix usage are analyzed alongside study time and exam performance.

5. **Overall predictive factors**
   Model coefficients and EDA relationships are used to identify which available variables contribute most strongly to predicting student outcomes.

> These findings describe relationships in the dataset and should not automatically be interpreted as proof of causation.

---

# 📝 Recommendations

Based on the analysis, students and educational institutions can consider:

* Encouraging consistent study schedules.
* Monitoring attendance and academic engagement.
* Promoting healthy sleep habits.
* Encouraging regular physical activity.
* Maintaining a balanced approach to social media and entertainment.
* Providing additional academic support to students predicted to be at risk of failing.
* Using data-driven analysis to identify students who may benefit from early intervention.

---

# 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**
* **Google Colab**

---

# 📁 Project Structure

```text
Student-Performance-ML/
│
├── Day18_19_student_habits_performance.csv
├── Student_Performance_ML.ipynb
├── README.md
└── requirements.txt
```

---

# ▶️ How to Run

## Google Colab

1. Open Google Colab.
2. Upload the `.ipynb` notebook.
3. Upload the CSV dataset.
4. Run the cells from top to bottom.

## Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Then open the notebook:

```bash
jupyter notebook
```

Run all cells sequentially.

---

# 📌 Machine Learning Workflow

```text
Dataset
   ↓
Data Understanding
   ↓
Data Quality Checks
   ↓
Exploratory Data Analysis
   ↓
Feature Analysis
   ↓
Data Preprocessing
   ↓
Train/Test Split
   ↓
   ┌───────────────────────┐
   │                       │
Regression            Classification
   │                       │
Linear Regression     Logistic Regression
   │                       │
Exam Score            Pass / Fail
   │                       │
MAE / RMSE / R²       Accuracy / Precision
                       Recall / F1
   │                       │
   └───────────┬───────────┘
               ↓
      Model Comparison
               ↓
       Insights & Conclusion
```

---

# 🚀 Future Improvements

Future versions of this project could include:

* Random Forest Regression
* Random Forest Classification
* Gradient Boosting
* XGBoost
* Hyperparameter tuning
* Cross-validation
* Feature importance using tree-based models
* SHAP-based model explainability
* Streamlit dashboard
* Interactive student-performance prediction
* Deployment as a web application

---

# 📌 Conclusion

This project demonstrates a complete Machine Learning workflow for understanding student performance.

By combining **EDA, preprocessing, regression, classification, model evaluation, and interpretation**, the project provides a data-driven view of the factors associated with academic outcomes.

The project also demonstrates an important Machine Learning principle: model performance should be evaluated on **unseen testing data**, not only on training data.

---

## 👨‍💻 Project Type

**Machine Learning | Regression | Classification | Exploratory Data Analysis | Student Performance Analytics**

---

⭐ If you found this project useful, consider giving the repository a star!
