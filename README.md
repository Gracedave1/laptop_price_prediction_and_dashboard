# 💻 Laptop Price Prediction & Power BI Dashboard

This project demonstrates how laptop specifications influence their prices and how machine learning can be used to predict prices accurately. It involves data preprocessing, exploratory data analysis (EDA), visualization through Power BI, and building multiple regression models to forecast laptop prices.

---

## 📌 Project Objectives

- Understand the relationship between laptop specifications and pricing.
- Create an interactive dashboard for data visualization and exploration.
- Build and compare different machine learning models for price prediction.

---

## 🧩 Dataset

The dataset includes various laptop specifications:

- Brand
- Processor (CPU)
- RAM
- Storage (HDD/SSD)
- GPU
- Operating System
- Display (inches, touchscreen)
- Price

---

## 📊 Exploratory Data Analysis (EDA)

Performed EDA to identify:

- Key variables impacting laptop prices
- Distribution of prices across brands and configurations
- Correlation between features such as RAM, processor, and storage with price
- Patterns in user reviews and ratings
- Detection of outliers and data inconsistencies

---

## 🧹 Data Cleaning

- Converted RAM and storage units to numeric values
- Created new features: `Total Storage (GB)`, `Is Touchscreen`, `Processor Brand`
- Removed duplicates and standardized categorical entries
- ✅ **No missing values** were found in the dataset.
- 🔎 **Outliers detected** in the following columns using Z-score:
  - `Price`
  - `Number of Ratings`
  - `Number of Reviews`
- ✂️ **Outliers handled** using the **Interquartile Range (IQR)** method for robustness.
- Saved cleaned data as `laptop_data_cleaned.csv`

---

## 📈 Power BI Dashboard

An interactive dashboard was built using Power BI. Key features include:

- Average laptop prices by brand
- Price distribution filters by Brand, RAM, OS, and processor
- Slicers for OS, weight etc.

---

## 🤖 Machine Learning: Price Prediction

Multiple regression models were trained to predict prices from laptop specs.

## 🔍 Model Evaluation

| **Model**                | **R² Score**     | **RMSE**     | **MSE**         |
|--------------------------|------------------|--------------|-----------------|
| 📉Linear Regression      | 0.9704           | 4,134.20     | 17.09M          |
| 🌲Decision Tree          | 0.9359           | 6,080.75     | 36.98M          |
| 🔧Ridge Regression       | 0.9711           | 4,085.70     | 16.69M          |
| 🧬Lasso Regression       | 0.9704           | 4,132.16     | 17.07M          |
| 🎯Gradient Boosting 🌟   | **0.9892**      | 2,496.36      | 6.23M          |


#### 🧠 Model Insights

- **Best Model:** Gradient Boosting offers the best performance with the highest R² and lowest RMSE, explaining 98.92% of the variance.
- **Decision Tree:** A strong but slightly less generalizable model; potential risk of overfitting.
- **Ridge/Lasso:** Trade off some performance for better interpretability and regularization.
- **Linear Regression:** Least accurate in this case due to inability to model complex relationships.

---

## 🛠️ Tools Used

- **Python**: `pandas`, `numpy`, `scikit-learn`, `seaborn`, `matplotlib`
- **Power BI**: For dashboard and interactive visualizations
- **Jupyter Notebook**: For analysis and modeling

---

