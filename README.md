# 🚦 Traffic Prediction using Machine Learning

An end-to-end **Machine Learning project** that analyzes urban traffic patterns and predicts traffic conditions using historical traffic data.
The project covers the complete ML workflow including **data preprocessing, exploratory data analysis (EDA), feature engineering, model training, hyperparameter tuning, and evaluation**.

The model predicts traffic situations such as **Low Traffic, Normal Traffic, and High Traffic** using vehicle count data.

---

# 📌 Project Overview

Urban traffic congestion is a major challenge in modern cities. Accurate traffic prediction can help improve traffic management, optimize road usage, and support smart city infrastructure.

This project builds a machine learning system that learns traffic patterns based on different vehicle counts and time-based features.

---

# 📂 Dataset Information

Two datasets were combined and cleaned for analysis.

| Dataset             | Records |
| ------------------- | ------- |
| Traffic.csv         | 2976    |
| TrafficTwoMonth.csv | 5952    |

After removing duplicates and cleaning the data, the final dataset contains **6324 records**.

### Features

| Feature           | Description              |
| ----------------- | ------------------------ |
| Time              | Timestamp of observation |
| Date              | Day of month             |
| DayOfWeek         | Day of the week          |
| CarCount          | Number of cars           |
| BikeCount         | Number of bikes          |
| BusCount          | Number of buses          |
| TruckCount        | Number of trucks         |
| Total             | Total number of vehicles |
| Traffic Situation | Target variable          |

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed:

* Merged multiple datasets
* Removed duplicate records
* Converted **Time column to datetime**
* Extracted **Hour and Minute features**
* Handled categorical variables
* Prepared dataset for model training

---

# 📊 Exploratory Data Analysis (EDA)

EDA was conducted to understand traffic patterns and relationships between variables.

### Analysis Performed

* Hourly traffic trends
* Vehicle distribution analysis
* Traffic patterns across weekdays
* Correlation analysis between vehicle types
* Traffic situation distribution

### Visualization Tools

* Matplotlib
* Seaborn

Example analyses include:

* Hourly traffic pattern visualization
* Correlation heatmap
* Traffic distribution plots
* Vehicle contribution analysis

---

# ⚙️ Feature Engineering

New features were created to help the model understand time-based patterns:

* **Hour** extracted from Time
* **Minute** extracted from Time
* Encoded **DayOfWeek**

Feature engineering significantly improved the predictive capability of the model.

---

# 🤖 Machine Learning Model

The model used for prediction is:

**Random Forest Classifier**

### Why Random Forest?

* Handles nonlinear relationships well
* Works effectively with tabular datasets
* Reduces overfitting through ensemble learning
* Provides feature importance insights

---

# 🔧 Hyperparameter Tuning

Hyperparameter tuning was performed using:

**RandomizedSearchCV**

Cross-validation strategy:

**K-Fold Cross Validation (k = 5)**

Parameters tuned:

* Number of estimators
* Maximum depth
* Minimum samples split
* Minimum samples leaf
* Maximum features

---

# 📈 Model Performance

| Metric              | Score  |
| ------------------- | ------ |
| Validation Accuracy | 93.42% |
| Test Accuracy       | 92.03% |
| Precision           | 0.927  |
| Recall              | 0.920  |
| F1 Score            | 0.920  |

The model performs well in predicting traffic conditions with high accuracy and balanced precision-recall scores.

---

# 📉 Learning Curve Analysis

Learning curve analysis was performed to evaluate the model's training behavior.

Observations:

* Stable convergence
* Minimal overfitting
* Good generalization performance

---

# 💾 Model Persistence

The trained model was saved using **Joblib** so it can be reused without retraining.

```python
joblib.dump(best_model, "traffic_model.pkl")
```

---

# 🛠 Technology Stack

### Programming Language

Python

### Data Processing

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-learn
* Random Forest Classifier

---

# 📊 Key Insights

* Traffic peaks during **morning and evening rush hours**
* **Cars contribute the majority of traffic volume**
* Truck traffic behaves differently compared to other vehicles
* Total vehicle count is the most influential feature

---

# 📁 Project Structure

Traffic-Prediction-ML
│
├── dataset
│   ├── Traffic.csv
│   └── TrafficTwoMonth.csv
│
├── notebook
│   └── traffic_analysis.ipynb
│
├── models
│   └── traffic_model.pkl
│
├── images
│
└── README.md

---

# 🚀 Future Improvements

* Deploy model using **Flask or FastAPI**
* Build a **real-time traffic prediction API**
* Integrate real-time traffic data
* Create a **dashboard for traffic visualization**

---

# 👨‍💻 Author

**Sagar Rai**

Machine Learning Engineer focused on building **end-to-end ML systems, predictive models, and data-driven applications.**

GitHub: https://github.com/yourusername
LinkedIn: https://linkedin.com/in/yourprofile

---

# 🏷 Topics

machine-learning
data-science
traffic-prediction
random-forest
scikit-learn
python
eda
data-analysis
predictive-modeling
ml-project
