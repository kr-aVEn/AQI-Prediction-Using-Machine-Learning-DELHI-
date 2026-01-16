# AQI-Prediction-Using-Machine-Learning-DELHI-
A machine learning project to predict Air Quality Index (AQI) using pollutant concentration data. The project compares Linear Regression, Decision Tree, and Random Forest models and analyzes the impact of temporal and holiday factors on air quality. focusing on Delhi
This project focuses on predicting the Air Quality Index (AQI) using daily air pollutant concentrations such as PM2.5, PM10, NO₂, SO₂, CO, and Ozone. Multiple machine learning models including Linear Regression, Decision Tree, and Random Forest are trained and evaluated. The study also analyzes the effect of holidays and weekends on AQI and demonstrates that pollutant levels are the primary drivers of air quality. Random Forest achieved the best performance with high predictive accuracy.
# AQI Prediction Using Machine Learning


## 📊 Dataset Description
The dataset contains daily records of:
- PM2.5 (µg/m³)
- PM10 (µg/m³)
- NO₂ (µg/m³)
- SO₂ (µg/m³)
- CO (mg/m³)
- Ozone (µg/m³)
- Holiday indicator (0 = Working day, 1 = Holiday)
- Day type (Weekend / Weekday)
- Air Quality Index (AQI)

## 🎯 Objective
- Predict AQI using pollutant concentrations
- Analyze the effect of holidays and weekends on AQI
- Compare machine learning models
- Improve prediction accuracy using ensemble methods

## 🛠️ Models Used
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

## 📈 Model Performance

| Model | RMSE | MAE | R² |
|------|------|------|------|
| Linear Regression | 38.13 | 26.85 | 0.888 |
| Decision Tree | 32.13 | 20.54 | 0.920 |
| Random Forest | **28.92** | **18.58** | **0.936** |

## 🧠 Key Findings
- Pollutant concentrations are strong predictors of AQI
- Holidays and weekends have minimal impact on AQI
- Random Forest outperformed other models due to its ability to capture non-linear relationships

## 🧪 Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
