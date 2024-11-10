# PotatoCo Yield Prediction

## Overview
This repository contains the **Colab Notebook** and datasets for our **Hackathon Project**: _Analyzing the Impact of Climate and Agricultural Factors on Potato Yield in India_. The project uses **time series analysis** to predict potato yield, based on multiple data sources including climate, emissions, and fertilizer usage.

### Key Objectives:
- Analyze historical data on potato yield.
- Study the relationship between climate variables, emissions, and agricultural inputs.
- Build and compare regression models to predict potato yield accurately.

---

Based on the provided repository structure, here’s how you can better organize it and update the README accordingly.

### Repository Structure:

```
├── data/                  # Folder containing all combined datasets
│   ├── Emissions_FAOSTAT_data_en_12-3-2022.csv
│   ├── FAOSTAT_data_en_11-6-2024.csv
│   ├── Fertilizers_FAOSTAT_data_en_12-3-2022.csv
│   └── climate.csv
├── PotatoCo-ClimateImpact-PotatoYield-India.ipynb             # file for Jupyter/Colab notebooks
├── README.md              # Project documentation
```
---


### Datasets:
1. **Annual Emissions Statistics**: Contains yearly emissions of CO2, CH4, and N2O.
2. **Fertilizer Trends**: Tracks nutrient usage (Nitrogen, Phosphate, Potash) over time.
3. **Annual Potato Statistics**: Area harvested and yield data for potatoes.
4. **Climate Data**: Annual and monthly precipitation and temperature metrics.

---

## Notebook Walkthrough

### 1. **Data Loading and Exploration**
   - Loaded datasets from various sources, ensuring consistency.
   - Previewed datasets to understand structure and identify missing values.

### 2. **Data Cleaning and Transformation**
   - **Handling Missing Values**:
     - Interpolated missing values in emissions data using linear and mean methods.
   - **Feature Engineering**:
     - Combined datasets using `merge` to form a single, cohesive DataFrame on 'year'.
   - **Final DataFrame**:
     - The cleaned and merged dataset was structured for time series regression.

### 3. **Exploratory Data Analysis (EDA)**
   - Analyzed trends in climate, emissions, and agricultural inputs over time.
   - Visualized important features like precipitation, temperature, and potato yield.

### 4. **Correlation Analysis**
   - Computed correlation matrix to identify features most relevant to `Yield`.
   - Top features:
     - **Direct emissions (N2O)**
     - **Nutrient nitrogen usage**
     - **Area harvested**

### 5. **Model Building and Evaluation**
   - Built and evaluated various regression models:
     1. **Linear Regression**
     2. **Decision Tree Regressor**
     3. **Random Forest Regressor**
     4. **Gradient Boosting Regressor (GBR)**
     5. **XGBoost Regressor**
     6. **Support Vector Regressor (SVR)**
   - Compared models based on:
     - **R² Score**
     - **RMSE (Root Mean Squared Error)**

### 6. **Model Comparison**
   - Visualized model performance using bar charts.
   - Identified the best model for predicting potato yield.

---

## Key Insights
- **Nutrient Nitrogen Usage** and **Direct Emissions** showed a strong correlation with potato yield.
- **Linear Regression** and **Random Forest Regressor** provided the most accurate predictions with the lowest RMSE.

---

## How to Use This Repository

1. **Clone the Repository**:
   ```bash
   https://github.com/Praful-John2409/PotatoCo-Yield-Prediction.git
   ```
   
2. **Open the Colab Notebook**:
   - Link: [PotatoCo-ClimateImpact-PotatoYield-India.ipynb]([https://colab.research.google.com/drive/some-notebook-link](https://colab.research.google.com/drive/1Q9pjNmqGZ11Qrna1ZOyZ9nU8B9rnMqD8?usp=sharing))
   
3. **Run the Notebook**:
   - Follow the steps in the notebook to preprocess data, build models, and evaluate results.

---

## Conclusion
This project demonstrates the use of **time series analysis** and **regression modeling** to predict potato yield. By leveraging multiple data sources, we identified key factors affecting potato production and built accurate predictive models.

### Future Work:
- Explore additional time series forecasting techniques.
- Incorporate more granular data for improved predictions.
- Automate the process for real-time yield prediction.

---
