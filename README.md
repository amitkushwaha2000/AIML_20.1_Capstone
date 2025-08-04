# AIML_20.1 Capstone Project
## Project Title - *Predicting Air Quality Index (AQI) Category in Delhi Using Machine Learning*

**Author:** Amit Kumar

#### Executive Summary
This capstone project applies machine learning techniques to predict the **Air Quality Index (AQI) Category** for Delhi using daily pollution and meteorological data. Accurate classification of air quality levels (e.g., "Good", "Moderate", "Poor", etc.) enables early warnings, public health interventions and environmental policy decisions. After extensive exploratory data analysis and model experimentation, the project identifies the **Random Forest Classifier** as the most reliable model for predicting AQI categories with over **99.9% accuracy**.

#### Rationale
Air pollution is a persistent public health and environmental crisis in Delhi. Given the complex interactions between pollutants and weather variables, manual forecasting is inadequate. Predictive modeling offers a scalable, data-driven alternative. This project seeks to empower authorities and citizens with **category-level AQI predictions** (e.g., "Poor", "Severe") using **historical pollutant and weather data**.

---

## Research Question

> **Can we develop a robust machine learning model that accurately predicts the Air Quality Index (AQI) category — Good, Satisfactory, Moderate, Poor, Very Poor, Severe — for Delhi using daily pollutant concentration levels and weather data?**

---

## Data Sources

1. **Delhi Pollution Dataset**  
   Daily concentration values for pollutants (PM2.5, PM10, NO2, SO2, CO, NH3, O3, etc.)  
   [Source: Tumidata](https://hub.tumidata.org/dataset/air_quality_analysis_of_delhi_delhi)

2. **Delhi Weather Dataset**  
   Meteorological data including temperature, humidity, wind speed, pressure, etc.  
   [Source: Visual Crossing Weather Data](https://www.visualcrossing.com/weather-query-builder/)
   
3. **Changes in Dataset Identified During Assignment 16.1**
    Kaggle – Air Quality Analysis of Delhi dataset mentioned in submission for Assignement 16.1 has not been used as the requirement of pollution and weather dataset has been met from thee above sources.   
---

## Methodology

### 1. **Data Cleaning & Merging**
- Removed irrelevant columns (e.g., station codes)
- Converted timestamps and aligned formats
- Merged pollution and weather datasets on `datetime`
- Interpolated missing values and ensured temporal consistency

### 2. **Exploratory Data Analysis (EDA)**
- Visualized seasonal, daily, and category-wise AQI variations
- Boxplots, KDEs, and scatter matrices analyzed pollutant distributions
- Outlier detection via boxplots and value thresholds

### 3. **Feature Engineering**
- Extracted `month`, `weekday`, `hour` from datetime
- Converted AQI values to categories using CPCB thresholds
- Encoded categorical AQI labels using `LabelEncoder`

### 4. **Baseline & Comparative Modeling**
- **Logistic Regression (baseline)** with feature scaling
- **Decision Tree Classifier**
- **Random Forest Classifier**
- Models evaluated using:
  - Accuracy
  - Precision, Recall, F1-Score
  - Confusion Matrix
  - 5-Fold Cross-Validation with Stratified Sampling

---

## Results

### Logistic Regression
- Accuracy: 0.9785  
- F1 Score (weighted): 0.98  
- Strength: interpretable; weaker on class boundaries

### Decision Tree
- Accuracy: 1.00  
- F1 Score: 1.00  
- Caveat: Likely overfitting (no regularization applied)

### Random Forest (Selected Final Model)
- Accuracy: 1.00 (Test) | 0.9996 (CV)  
- F1 Score: 1.00  
- Strength: Excellent generalization and robustness

---

## Key Insights

- AQI category prediction is highly feasible using historical pollution and weather data.
- Random Forest provides the best balance of accuracy and generalizability.
- Even simpler models like logistic regression can achieve over 97% accuracy.
- Feature importance (next phase) will help interpret dominant pollutants driving category shifts.

---

## Next Steps

- Hyperparameter tuning for final model refinement
- Feature importance analysis 
- Final model selection
- Deploy model

---

## Project Structure and Notebooks

| Notebook | Description |
|----------|-------------|
| [Link to Notebook](https://github.com/amitkushwaha2000/AIML_20.1_Capstone/blob/main/20.1%20Capstone_AK_AQI%20Prediction.ipynb) | Jupyter Notebook for Assignment 20.1 Capstone Project |
| [Link to Datasets](https://github.com/amitkushwaha2000/AIML_20.1_Capstone/tree/main/data) | delhi_pollution.csv and delhi_weather.csv |

---

## Contact and Further Information

For feedback, collaboration, or deployment queries, feel free to reach out at:  
**[amitkushwaha2000@gmail.com]**

---
