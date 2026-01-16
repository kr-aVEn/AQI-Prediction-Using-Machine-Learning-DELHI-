# AQI Prediction and Dual Classification System

This project implements a **robust machine learning system** for predicting **Air Quality Index (AQI)** and classifying air quality conditions using **two complementary approaches**:

1. **Rule-based classification derived from predicted AQI**
2. **Machine learning–based classification using Random Forest**

The dual-classification design improves reliability, interpretability, and real-world applicability.

---

## 📌 Problem Statement

Air pollution monitoring requires both **accurate AQI prediction** and **clear air quality categorization**. This project predicts numerical AQI values from pollutant concentrations and classifies air quality using both standard thresholds and a learned classifier.

---

## 📊 Dataset

* Daily air pollutant measurements:

  * PM2.5, PM10, NO₂, SO₂, CO, Ozone
* Target variables:

  * AQI (regression)
  * AQI Quality Category (classification)
* Time-series dataset with daily records

---

## 🧠 Methodology

### Notebook 1: EDA & Feature Engineering

* Data cleaning and missing value handling
* Creation of AQI quality labels using standard thresholds
* Exploratory data analysis and class distribution study

### Notebook 2: Model Comparison & Stability Analysis

* Regression models evaluated:

  * Linear Regression
  * Decision Tree Regressor
  * Gradient Boosting Regressor
  * Random Forest Regressor
* Metrics:

  * MAE, RMSE, R²
* Cross-validation stability analysis
* Time-series error drift analysis
* **Random Forest selected** due to superior robustness and stability

### Notebook 3: Final Dual-Classification Pipeline

* AQI prediction using Random Forest regression
* **Rule-based AQI classification** using government-defined thresholds
* **Random Forest–based AQI classification** for data-driven comparison
* Accuracy comparison between both classification approaches
* Real-time prediction logic

---

## 🔁 Dual Classification Strategy

### 1️⃣ Rule-Based Classification (Primary)

* Derived directly from predicted AQI
* Uses standard AQI thresholds
* Highly interpretable and policy-aligned
* Robust to class imbalance

### 2️⃣ ML-Based Classification (Secondary)

* Random Forest multi-class classifier
* Learns soft boundaries between AQI categories
* Provides probability confidence for each class
* Used for comparison and analytical insight

---

## 📈 Final Model Performance

* AQI Regression:

  * R² ≈ 0.90
  * RMSE within acceptable environmental limits
* Classification:

  * ML-based classifier achieves higher categorical accuracy
  * Rule-based classification ensures semantic correctness

---

## 🛠 Project Structure

```
AQI-Prediction-ML/
│
├── data/
│   ├── final_dataset.csv
│   └── cleaned_aqi_data.csv
│
├── notebooks/
│   ├── 01_EDA_and_Feature_Engineering.ipynb
│   ├── 02_Model_Comparison_and_Stability.ipynb
│   └── 03_Final_Regression_RuleBased_Classification.ipynb
│
├── src/
│   ├── train_models.py
│   └── predict_realtime.py
│
├── models/
│   ├── aqi_regression_model.pkl
│   ├── aqi_classification_model.pkl
│   └── features.pkl
│
├── results/
│   └── plots and evaluation figures
│
├── README.md
└── requirements.txt
```


