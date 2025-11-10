# 🌤️ Predicting the Weather Using Machine Learning

## 📖 Overview
This project applies **supervised machine learning algorithms** to predict daily weather types — **Rainy, Sunny, Cloudy, or Snowy** — using a dataset sourced from Kaggle.  
The goal is to enhance short-term weather forecasting accuracy by leveraging data-driven classification techniques.

## 🎯 Objectives
- Clean and preprocess meteorological data.  
- Perform feature selection and standardization.  
- Train and evaluate multiple ML models.  
- Compare model performance to determine the most accurate weather predictor.

## 🧠 Machine Learning Models
The following classification algorithms were implemented and optimized using **RandomizedSearchCV**:
- **K-Nearest Neighbors (KNN)**  
- **Decision Tree Classifier**  
- **Random Forest Classifier**  
- **Support Vector Machine (SVM)**  
- **Logistic Regression**

### ⚙️ Performance Summary
| Model | Accuracy | Precision | ROC AUC |
|:------|:----------|:-----------|:---------|
| Random Forest | 0.951 | 0.951 | 0.997 |
| Decision Tree | 0.947 | 0.947 | 0.991 |
| KNN | 0.945 | 0.946 | 0.989 |
| SVM | 0.943 | 0.944 | — |
| Logistic Regression | 0.912 | 0.913 | 0.967 |

**Best Model:** Random Forest — demonstrated strong generalization, minimal overfitting (train-test AUC gap of 0.003), and consistent performance across all weather classes.

## 📊 Dataset
- **Source:** [Weather Type Classification (Kaggle)](https://www.kaggle.com/datasets/nikhil7280/weather-type-classification)  
- **Size:** ~13,200 rows and 11 features  
- **Features include:** Temperature, Humidity, Precipitation %, Atmospheric Pressure, UV Index, Wind Speed, Visibility, Season, and Location.  
- **Target Variable:** `WeatherType` — categorized as *Rainy*, *Sunny*, *Cloudy*, or *Snowy*.

## 🧩 Data Preprocessing
- **Outlier Removal:** Three-sigma rule.  
- **Feature Selection:** Used `mutual_info_classif` to retain the most informative features.  
- **Standardization:** Applied `StandardScaler` for consistent feature scaling.  
- **Train/Test Split:** 80/20 with random state = 42.  

## 📚 Libraries Used
- Python 3.10+  
- Pandas 2.3.2  
- NumPy 2.3.2  
- Scikit-learn 1.7.1  
- Seaborn 0.13.2  
- SciPy 1.16.1  

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/Adamrakowski1/AI-Project.git
