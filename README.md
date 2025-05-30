
# 🏠 Bengaluru House Price Prediction

This project builds a machine learning model to predict housing prices in Bengaluru, India, based on various features like location, size (BHK), total square footage, number of bathrooms, etc. It also includes data cleaning, outlier handling, feature engineering, and model evaluation.

---

## 📌 Problem Statement

The real estate market in Bengaluru is diverse and highly location-dependent. The goal of this project is to develop a regression model that accurately predicts house prices based on the available property features.

---

## 📊 Dataset

- **Source**: Kaggle – [Bengaluru House Price Data](https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data)
- **Size**: ~1300 rows, 9 columns
- **Target Variable**: `price` (in lakhs)

### Features:
| Column | Description |
|--------|-------------|
| location | Area/locality of the property |
| size | Number of BHKs |
| total_sqft | Total area in square feet |
| bath | Number of bathrooms |
| balcony | Number of balconies |
| area_type | Super built-up / built-up / plot area |
| availability | Ready to move or construction status |
| price | Property price (target variable) |

---

## 🧹 Data Cleaning and Preprocessing

- Removed unnecessary columns like `society`, `availability`
- Handled missing values in `bath`, `balcony`, and `size`
- Converted `size` column to numerical BHKs
- Handled non-numeric `total_sqft` values (e.g., ranges like "2100 - 2850")
- One-hot encoding for categorical features like `location` and `area_type`
- Removed outliers based on:
  - Price per square foot
  - Bathroom-to-BHK ratio
  - Unusual square footage per BHK

---

## ⚙️ Model Building

- **Train-test split**: 80-20
- **Algorithms Used**:
  - Linear Regression
  - Lasso Regression (for feature selection)
  - Ridge Regression
- **Model Evaluation**:
  - R² Score
  - Cross-validation (ShuffleSplit)

---

## 📈 Results

- Final model uses Linear Regression with L2 regularization
- R² Score on test data: ~0.90 (depending on random split)
- Predictive performance is reasonable for real-world use cases
- Model successfully handles location-based variation in pricing

---

## 🚀 Future Improvements

- Add Streamlit web app for interactive prediction
- Integrate location mapping using `folium` or `geopandas`
- Use advanced models like XGBoost or Random Forest for comparison
- Use external APIs for live pricing updates




