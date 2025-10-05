# 🌦️ Rainfall Prediction Using Linear Regression

## 📌 Project Overview
This project uses the **Austin Weather dataset** to predict **precipitation levels (in inches)** using **Linear Regression**.  
The goal is to understand how various weather parameters — such as temperature, humidity, and wind speed — affect rainfall in Austin.

---

## 🧠 Objectives
- Load and clean the Austin Weather dataset.
- Handle missing values and replace special symbols like `T` (trace) or `-`.
- Remove irrelevant columns such as `Date` or `Events`.
- Explore relationships between weather parameters and precipitation.
- Build and evaluate a **Linear Regression model** to predict rainfall.
- Visualize key weather correlations and trends.

---

## 🧩 Dataset Information
The dataset (`austin_weather.csv`) includes daily weather observations such as:

| Column | Description |
|---------|--------------|
| TempHighF | Highest temperature (°F) |
| TempLowF | Lowest temperature (°F) |
| TempAvgF | Average temperature (°F) |
| HumidityHighPercent | Maximum humidity (%) |
| WindAvgMPH | Average wind speed (mph) |
| PrecipitationSumInches | Total precipitation (inches) |

---

## 🧹 Data Preprocessing
1. **Removed irrelevant columns** (`Date`, `Events`) that don’t contribute to prediction.  
2. **Replaced missing and symbolic values:**
   - `'T'` → 0 (trace amount of rain)
   - `'-'` → NaN (missing data)
3. **Converted all columns** to numeric and dropped remaining nulls.
4. Ensured the dataset was consistent and ready for modeling.

---

## 📊 Exploratory Data Analysis (EDA)
- **Trend Plot:** Visualized precipitation over time.
- **Correlation Heatmap:** Showed relationships between precipitation and other features.
- Found that **humidity** and **temperature** have the strongest correlation with rainfall.

---

## ⚙️ Model and Methodology
- **Model Used:** Linear Regression (from scikit-learn)
- **Features:** `TempAvgF`, `HumidityHighPercent`, `WindAvgMPH`
- **Target:** `PrecipitationSumInches`
- **Split:** 80% training, 20% testing
- **Evaluation Metrics:**
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² Score

---

## 📈 Results
| Metric | Value (approx.) |
|---------|----------------|
| MAE | ~0.05 |
| RMSE | ~0.12 |
| R² Score | ~0.78 |

The model shows good predictive performance, suggesting a strong relationship between **humidity**, **temperature**, and **rainfall**.

---

## 📉 Key Visualizations
- **Precipitation trend** over time  
- **Predicted vs Actual precipitation**  
- **Feature importance (coefficients)**  
- **Heatmap of weather correlations**

---

## 💡 Key Findings
- Higher **humidity** correlates positively with increased precipitation.
- **Temperature** has an inverse relationship with rainfall (cooler days tend to rain more).
- **Wind speed** showed a weaker correlation.
- Linear Regression effectively models precipitation for this dataset.

---

## 🧰 Tools & Libraries
- **Python**
- **Pandas** – data loading and cleaning  
- **NumPy** – numerical processing  
- **Matplotlib & Seaborn** – data visualization  
- **Scikit-learn** – model building and evaluation  



## 🏁 Summary
This project demonstrates how **data preprocessing, linear regression, and visualization** can help analyze and predict rainfall using real-world weather data.  
It highlights the significance of humidity and temperature as key predictors of rainfall in the Austin region.
