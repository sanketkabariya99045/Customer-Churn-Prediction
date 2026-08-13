# Customer Churn Prediction

A machine learning project that predicts whether a telecom customer is likely to churn based on customer demographics, account information, services, contract details, and billing information.

## 📌 Project Overview

Customer churn is an important business problem for telecom companies. Identifying customers who are likely to leave can help businesses take proactive actions to improve customer retention.

In this project, multiple machine learning classification algorithms are trained and compared for predicting customer churn.

The project includes:

* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Categorical data preprocessing
* Multiple machine learning models
* Model accuracy comparison
* Confusion matrix and classification reports
* Random Forest feature importance
* Churn visualization and analysis

## 📊 Dataset

The project uses the **Telco Customer Churn dataset**.

The dataset contains customer information such as:

* Customer demographics
* Gender
* Senior citizen status
* Partner and dependents
* Tenure
* Phone and internet services
* Contract type
* Payment method
* Monthly charges
* Total charges
* Churn status

The target variable is:

```text
Churn
```

where:

* `Yes` → Customer churned
* `No` → Customer did not churn

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## 🤖 Machine Learning Models

The following classification algorithms are implemented and compared:

1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**
4. **K-Nearest Neighbors (KNN)**

Each model is trained using the training dataset and evaluated using the test dataset.

## 🔄 Machine Learning Workflow

```text
Dataset
   ↓
Data Cleaning
   ↓
Remove Customer ID
   ↓
Convert TotalCharges to Numeric
   ↓
Handle Missing Values
   ↓
Feature / Target Separation
   ↓
Categorical Feature Encoding
   ↓
Train-Test Split
   ↓
Model Training
   ↓
Model Prediction
   ↓
Model Evaluation
```

## 🧹 Data Preprocessing

The following preprocessing steps are performed:

### Remove Customer ID

The `customerID` column is removed because it is an identifier and does not provide useful predictive information.

### Convert TotalCharges

`TotalCharges` is converted to a numeric data type.

```python
df['TotalCharges'] = pd.to_numeric(
    df['TotalCharges'],
    errors='coerce'
)
```

### Handle Missing Values

Rows containing missing values after conversion are removed.

### Encode Categorical Variables

Categorical features are converted into numerical representations so that machine learning algorithms can process them.

### Train-Test Split

The dataset is divided into:

* 80% training data
* 20% testing data

## 📈 Exploratory Data Analysis

The notebook contains several visualizations to understand customer churn.

### Churn Distribution

Shows the distribution of customers who churned versus customers who stayed.

### Correlation Heatmap

Used to understand relationships between numerical features.

### Model Accuracy Comparison

Compares the accuracy of the four machine learning models.

### Random Forest Feature Importance

Identifies the most important features used by the Random Forest model for churn prediction.

### Additional Analysis

The project also explores:

* Tenure distribution by churn
* Monthly charges distribution by churn
* Churn by contract type
* Churn by payment method

## 📋 Model Evaluation

The models are evaluated using:

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1-score
* Classification Report

The project also generates a model comparison table containing the accuracy of each classifier.

## 📂 Project Structure

```text
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction_Model.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
└── README.md
```

> Make sure the dataset filename matches the filename used in the notebook.

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/sanketkabariya99045/Customer-Churn-Prediction.git
```

### 2. Navigate to the project

```bash
cd Customer-Churn-Prediction
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open

```text
Customer_Churn_Prediction_Model.ipynb
```

Run the notebook cells sequentially.

## 🎯 Project Goals

The main objectives of this project are:

* Understand the factors associated with customer churn
* Perform data preprocessing on a real-world dataset
* Compare different classification algorithms
* Evaluate machine learning model performance
* Identify important features related to customer churn
* Demonstrate an end-to-end machine learning workflow

## 🔮 Future Improvements

Possible improvements for this project include:

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* Cross-validation
* Handling class imbalance
* ROC-AUC analysis
* Precision-Recall analysis
* Feature engineering
* Model explainability using SHAP
* Building a Streamlit prediction application
* Deploying the best-performing model as an API

## 👨‍💻 Author

**Sanket Kabariya**

MSc IT | Aspiring Data Analyst

GitHub:
https://github.com/sanketkabariya99045

---

⭐ If you find this project useful, consider giving the repository a star!
