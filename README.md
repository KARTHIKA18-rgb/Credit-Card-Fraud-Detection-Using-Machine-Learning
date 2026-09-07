# 💳 Credit Card Fraud Detection Using Machine Learning

## 📌 Project Overview

This project focuses on detecting fraudulent credit card transactions using **Machine Learning** techniques. The system analyzes transaction-related features and learns patterns that help classify transactions as **Genuine** or **Fraudulent**.

The project includes **Exploratory Data Analysis (EDA), Data Visualization, Feature Analysis, Machine Learning Model Comparison, Hyperparameter Tuning, and Model Evaluation**.

---

## 🎯 Objectives

* Detect fraudulent credit card transactions.
* Analyze transaction patterns and risk factors.
* Identify features that have a strong relationship with fraud.
* Compare multiple Machine Learning algorithms.
* Improve model performance through hyperparameter tuning.
* Evaluate the final model using classification metrics and a confusion matrix.

---

## 📂 Dataset

The project uses a **Credit Card Fraud Detection** dataset containing transaction-related information.

### Important Features

| Feature                  | Description                                               |
| ------------------------ | --------------------------------------------------------- |
| Transaction Amount       | Monetary value of the transaction                         |
| Account Balance          | Account balance associated with the transaction           |
| Age                      | Age of the customer                                       |
| Merchant Risk Score      | Risk score associated with the merchant                   |
| Transaction Hour         | Hour at which the transaction occurred                    |
| Foreign Transaction      | Indicates whether the transaction is foreign              |
| Previous Fraud Flag      | Indicates previous fraudulent activity                    |
| Merchant Distance        | Distance between customer and merchant                    |
| Average Transactions/Day | Average transaction frequency                             |
| Fraud                    | Target variable indicating fraudulent/genuine transaction |

---

## 🛠️ Technologies & Tools Used

### Programming Language

* Python

### Libraries

* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical computations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Scikit-learn** – Machine Learning and model evaluation

### Development Environment

* Jupyter Notebook

---

## 🔍 Exploratory Data Analysis

The dataset was explored to understand transaction characteristics and identify patterns associated with fraudulent activities.

The analysis included:

* Dataset structure and information
* Missing value analysis
* Statistical summary
* Fraud distribution analysis
* Feature distributions
* Outlier analysis
* Correlation analysis
* Fraud patterns across different transaction features

---

## 📊 Data Visualization & Key Insights

Several visualizations were created to understand the relationship between transaction features and fraud.

### 1. Fraud Distribution

The dataset contains approximately:

* **51.8% Genuine transactions**
* **48.2% Fraudulent transactions**

This indicates that the target classes are relatively balanced.

### 2. Transaction Amount

Fraudulent transactions generally show higher transaction amounts, with noticeable concentration around the **8,000–12,000** range.

This indicates that transaction amount can be an important factor for identifying suspicious transactions.

### 3. Account Balance

Account balance values show considerable overlap between fraudulent and genuine transactions. Therefore, account balance alone is not sufficient to identify fraud.

### 4. Age

Customer age shows some differences between fraudulent and genuine transactions, particularly among younger age groups. However, there is still substantial overlap.

### 5. Merchant Risk Score

Higher merchant risk scores show a somewhat stronger association with fraudulent transactions, making merchant risk score a potentially useful predictive feature.

### 6. Transaction Hour

Fraud rates vary according to transaction time. Some later hours show relatively higher fraud rates, with the highest observed rate around **11 PM (~56%)**.

### 7. Foreign Transactions

Foreign transactions show a stronger association with fraudulent activity compared with domestic transactions.

### 8. Previous Fraud Flag

The **Previous Fraud Flag** is one of the strongest indicators of fraudulent behavior. Transactions associated with previous fraud activity show significantly higher fraud occurrence.

### 9. Transaction Frequency

Fraudulent transactions have a slightly higher average transaction frequency:

* Genuine: **23.28 transactions/day**
* Fraudulent: **26.69 transactions/day**

### 10. Merchant Distance

Merchant distance ranges widely and has considerable overlap between fraudulent and genuine transactions, making it less useful as an individual fraud indicator.

---

## 🤖 Machine Learning Models

Multiple classification algorithms were implemented and compared:

1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Support Vector Classifier (SVC)**
4. **K-Nearest Neighbors (KNN)**
5. **Gradient Boosting Classifier**
6. **Bagging Classifier with KNN**

Feature scaling and class balancing were applied where appropriate.

---

## ⚙️ Model Training

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

A stratified train-test split was used with a fixed random state to maintain the class distribution between training and testing datasets.

---

## 📈 Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Classification Report
* Confusion Matrix

The models were compared based on their classification performance, with particular attention given to the **F1-score**, since both precision and recall are important for fraud detection.

---

## 🔧 Hyperparameter Tuning

**RandomizedSearchCV** was applied to the Gradient Boosting model to identify better hyperparameter combinations.

The tuning process used:

* 5-fold Cross-Validation
* Weighted F1-score as the scoring metric
* Randomized hyperparameter search

The tuned Gradient Boosting model was then evaluated on the test dataset.

---

## ⭐ Feature Importance

Feature importance was extracted from the tuned Gradient Boosting model to understand which transaction characteristics contributed most to fraud prediction.

Important predictive factors identified during the analysis include:

* Previous Fraud Flag
* Transaction Amount
* Merchant Risk Score
* Foreign Transaction
* Transaction Hour
* Transaction Frequency

---

## 🚨 Outlier Analysis

Boxplots were used to identify potential outliers in numerical features.

Instead of automatically removing these observations, the project retained them because extreme transaction values may represent **legitimate but unusual financial behavior or actual fraudulent activity**.

---

## 📌 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Cleaning & Exploration
   ↓
Exploratory Data Analysis
   ↓
Data Visualization
   ↓
Feature Analysis
   ↓
Train-Test Split
   ↓
Feature Scaling / Class Balancing
   ↓
Machine Learning Models
   ↓
Model Comparison
   ↓
Hyperparameter Tuning
   ↓
Final Model Evaluation
   ↓
Fraud Detection
```

---

## 💡 Conclusion

This project demonstrates how Machine Learning can be used to identify suspicious credit card transactions based on transaction behavior and risk-related features.

The analysis shows that factors such as **previous fraud activity, transaction amount, merchant risk, foreign transactions, transaction timing, and transaction frequency** can provide valuable information for fraud detection.

Machine Learning models can therefore support financial institutions in identifying potentially fraudulent transactions and improving transaction security.
