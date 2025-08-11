# Algerian Forest Fire Prediction - Model Training & Flask UI

## 📌 Project Overview
This project focuses on **predicting fire weather index (FWI)** for Algerian forest regions using **machine learning**.  
We utilize the **Algerian Forest Fires Dataset** containing meteorological and fire weather parameters, perform **Exploratory Data Analysis (EDA)**, **Feature Engineering (FE)**, train a **Ridge Regression model** ,Built a Flask web application so users can input weather data and get real-time predictions.
---

## 📊 Dataset
The dataset contains **daily weather and fire index measurements** from Algeria’s Bejaia and Sidi-Bel Abbes regions.

**Key Features:**
- Temperature (°C)  
- Relative Humidity (%)  
- Wind Speed (km/h)  
- Rain (mm)  
- FFMC, DMC, DC, ISI (Fire Weather Index components)  
- Region & Date  
- Target Variable: **FWI (Fire Weather Index)**

---

## 🛠 Steps Performed

### 1️⃣ Data Loading
- Loaded raw dataset (`Algerian_forest_fires_dataset_UPDATE.csv`).
- Inspected shape, data types, and missing values.

### 2️⃣ Data Cleaning
- Removed inconsistent entries & handled missing data.
- Corrected column names and ensured proper formatting.
- Converted date columns to `datetime` type.
- Encoded categorical features like region.

### 3️⃣ Exploratory Data Analysis (EDA)
- **Statistical Summary**: Mean, median, min, max for all features.
- **Visualizations**:
  - Histograms & boxplots for feature distribution.
  - Heatmap for feature correlations.
  - Region-wise comparison of FWI and weather conditions.

### 4️⃣ Feature Engineering
- Applied **One-Hot Encoding** for categorical variables.
- Standardized numerical features using `StandardScaler`.
- Selected important features for model training.

### 5️⃣ Model Training
- Chose **Ridge Regression** to handle multicollinearity.
- Used `train_test_split` to split data into training & testing sets.
- Hyperparameter tuning using `GridSearchCV`.

### 6️⃣ Model Evaluation
- Metrics:
  - **R² Score**
  - **Mean Absolute Error (MAE)**
  - **Root Mean Squared Error (RMSE)**
- Compared performance between training and test sets.

### 7️⃣ Saving Artifacts
- Saved trained model as `ridge.pkl`.
- Saved preprocessing scaler as `scaler.pkl`.

---

### 8️⃣ 📈 Results
Best Model: Ridge Regression

Achieved a high R² score indicating good predictive capability.

Preprocessing and model pipeline saved for deployment.

----


### 9️⃣ Flask UI Prediction
The trained Ridge Regression model is integrated into a Flask web application for real-time predictions.
[Link Text](http://127.0.0.1:5000/)

----

## 🚀 How to Run This Project

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/Algerian-Forest-Fire-Prediction.git
cd Algerian-Forest-Fire-Prediction

