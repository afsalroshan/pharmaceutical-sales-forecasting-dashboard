#  Pharmaceutical Sales Forecasting & Market Analysis using Time Series Forecasting, Machine Learning, and Interactive Dashboard

##  Project Overview

The pharmaceutical industry generates massive volumes of sales data every day. Analyzing this data helps businesses understand sales trends, optimize inventory, forecast future demand, and make informed decisions.

This project focuses on predicting pharmaceutical sales using Machine Learning and Time Series Forecasting techniques. It includes data preprocessing, exploratory data analysis (EDA), feature engineering, predictive modeling, and an interactive dashboard for visualizing sales insights.

---

##  Objectives

- Clean and preprocess the pharmaceutical sales dataset.
- Perform Exploratory Data Analysis (EDA) to discover sales patterns.
- Engineer meaningful features for better model performance.
- Build and compare multiple Machine Learning regression models.
- Forecast future pharmaceutical sales using Time Series Forecasting.
- Develop an interactive dashboard for business insights.

---

##  Dataset

**Dataset Name:** Global Pharmacy Sales Dataset (2020–2025)

**Source:** Kaggle

https://www.kaggle.com/datasets/annemark/global-pharmacy-sales-dataset-20202025

### Dataset Features

- Date
- Year
- Month
- Day
- Region
- Country
- Medicine Category
- Medicine Name
- Age Group
- Units Sold
- Unit Price
- Stock Level
- Expiry Days Remaining
- COVID Flag

---

##  Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn
- XGBoost
- Prophet
- Streamlit / Power BI
- Joblib

---

##  Project Structure

```
Pharmaceutical-Sales-Forecasting/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_Data_Preprocessing.ipynb
│   ├── 02_EDA.ipynb
│   ├── 03_Feature_Engineering.ipynb
│   ├── 04_Model_Building.ipynb
│   ├── 05_Time_Series_Forecasting.ipynb
│   └── 06_Dashboard.ipynb
│
├── models/
│
├── outputs/
│
├── dashboard/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

##  Project Workflow

### 1. Data Preprocessing

- Load dataset
- Handle missing values
- Remove duplicates
- Convert data types
- Encode categorical variables
- Feature scaling

### 2. Exploratory Data Analysis (EDA)

- Sales trend analysis
- Monthly sales analysis
- Region-wise sales
- Country-wise sales
- Medicine category analysis
- Correlation heatmap
- Stock level analysis
- COVID impact analysis

### 3. Feature Engineering

- Day of Week
- Quarter
- Week Number
- Date-based features

### 4. Machine Learning Models

- Linear Regression
- Random Forest Regressor
- XGBoost Regressor

### 5. Time Series Forecasting

- Prophet
- Sales Forecasting (30–90 Days)

### 6. Dashboard

- Interactive sales dashboard using Streamlit or Power BI.

---

##  Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

---

##  Expected Outcomes

- Accurate pharmaceutical sales prediction.
- Sales trend visualization.
- Inventory planning support.
- Business decision-making insights.
- Future sales forecasting.

---

##  Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Pharmaceutical-Sales-Forecasting.git
```

Navigate to the project directory

```bash
cd Pharmaceutical-Sales-Forecasting
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook or Streamlit dashboard.

---

##  Results

The project provides:

- Data preprocessing pipeline
- Exploratory Data Analysis
- Machine Learning model comparison
- Sales forecasting
- Interactive dashboard
- Business insights and visualizations


---

##  Future Enhancements

- Deploy using Streamlit Cloud
- Hyperparameter tuning
- LSTM-based sales forecasting
- Real-time sales prediction API
- Cloud deployment

---

##  Author

**Afsal E**


