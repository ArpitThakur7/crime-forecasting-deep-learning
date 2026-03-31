# 🚔 Calgary Crime Prediction using LSTM

## 📌 Overview
This project focuses on analyzing crime patterns in Calgary and predicting future crime occurrences using a Deep Learning model (LSTM).

The dataset contains crime records from **2018 to 2024**, including community, crime category, and monthly crime counts.

The goal is to:
- Understand crime trends
- Identify high-risk areas and categories
- Build a predictive model for future crime forecasting

---

## 📊 Dataset
- Source: City of Calgary Open Data
- Records: ~70,000 entries
- Features:
  - Community
  - Crime Category
  - Crime Count
  - Year
  - Month

📌 The dataset is clean with **no missing values** :contentReference[oaicite:0]{index=0}

---

## ⚙️ Technologies Used
- Python 🐍
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- TensorFlow / Keras (LSTM)

---

## 🔍 Data Preprocessing
- Checked for missing values (none found)
- Converted categorical features using **Label Encoding**
- Prepared sequential data for time-series modeling
- Split data into:
  - Training set
  - Validation set
  - Test set

---

## 📈 Exploratory Data Analysis (EDA)

### Key Insights:

### 🏙️ Community Analysis
- **Beltline** has the highest crime rate (~11.4%)
- Followed by Forest Lawn and Downtown Core :contentReference[oaicite:1]{index=1}

### 🚨 Crime Categories
- Most common:
  - Theft from Vehicle (~21.7%)
  - Theft of Vehicle (~16.7%)
- Least common:
  - Commercial & Street Robbery

### 📅 Yearly Trends
- Highest crime reported in **2019**
- Slight drop in recent years (2024 incomplete data)

### 📆 Monthly Trends
- Crime varies across months → indicates seasonal patterns

---

## 🤖 Model: LSTM Neural Network

### Why LSTM?
LSTM is suitable for time-series data as it captures temporal dependencies.

---

## 🏗️ Model Architecture
- LSTM Layer (50 units)
- Dropout (0.2)
- Dense Output Layer

---

## ⚙️ Training Details
- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Epochs: 100

---

## 📊 Model Performance

- Test Loss: **~4.89** :contentReference[oaicite:2]{index=2}  
- Training and validation loss decreased significantly over epochs

### 📉 Evaluation
- Actual vs Predicted values plotted
- Residual analysis performed

---

## 📊 Visualizations
- Community crime distribution
- Crime category distribution
- Year-wise and month-wise trends
- Actual vs predicted plots
- Residual plots

---

## 🔮 Predictions
The model successfully predicts future crime counts based on past patterns.

Example:
```python
model.predict(X_test)
