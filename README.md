# Pharmaceutical Sales Forecasting & Market Analysis using Time Series Forecasting, Machine Learning, and Interactive Dashboard

## Project Overview

The pharmaceutical industry generates large volumes of sales data across different medicines, categories, regions, countries, and time periods. Analyzing this data helps identify sales patterns, understand business performance, and support future demand planning.

This project focuses on pharmaceutical sales analysis, machine learning-based prediction, and time series forecasting using a global pharmacy sales dataset covering 2020–2025.

The project follows an end-to-end Data Science workflow:

Data Preprocessing → Exploratory Data Analysis → Feature Engineering → Machine Learning → Model Evaluation → Time Series Forecasting → Power BI Dashboard

The final Power BI dashboard provides an interactive view of pharmaceutical sales performance and forecast results.

## Objectives

- Clean and preprocess the pharmaceutical sales dataset.
- Perform Exploratory Data Analysis (EDA).
- Analyze sales patterns across time, regions, countries, and medicine categories.
- Engineer date-based features for machine learning.
- Build machine learning regression models for sales prediction.
- Evaluate the machine learning model using regression metrics.
- Identify important features influencing sales prediction.
- Forecast future pharmaceutical sales using Prophet.
- Develop an interactive Power BI dashboard.
- Present business-oriented insights through data visualization.

## Dataset

**Dataset Name:** Global Pharmacy Sales Dataset (2020–2025)

**Source:** Kaggle

https://www.kaggle.com/datasets/annemark/global-pharmacy-sales-dataset-20202025

**Dataset Period:** 2020–2025

### Dataset Features

| Feature | Description |
|---|---|
| date | Sales date |
| year | Year of transaction |
| month | Month of transaction |
| day | Day of transaction |
| region | Sales region |
| country | Country |
| category | Medicine category |
| medicine | Medicine name |
| age_group | Customer age group |
| units_sold | Number of units sold |
| unit_price | Price per unit |
| stock_level | Available stock level |
| expiry_days_remaining | Remaining expiry days |
| covid_flag | COVID-related indicator |

## Project Workflow

1. Data Preprocessing
2. Exploratory Data Analysis
3. Feature Engineering
4. Machine Learning
5. Model Evaluation
6. Feature Importance Analysis
7. Time Series Forecasting
8. Power BI Dashboard

## 1. Data Preprocessing

The raw pharmaceutical sales dataset was loaded and examined using Python and Pandas.

### Preprocessing Steps

- Loaded the dataset.
- Checked dataset dimensions.
- Examined data types.
- Checked missing values.
- Checked duplicate records.
- Converted the date column to datetime format.
- Removed duplicate records.
- Encoded categorical variables using LabelEncoder.
- Saved the cleaned dataset for further analysis.

### Encoded Categorical Columns

The following categorical features were label encoded:

- region
- country
- category
- medicine
- age_group

The cleaned dataset was saved as:

`data/processed/cleaned_pharmacy_sales.csv`

## 2. Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the characteristics and patterns of pharmaceutical sales.

### EDA Analysis

- Correlation analysis
- Sales distribution
- Unit price distribution
- Sales by category
- Sales by region
- Sales by country
- Monthly sales trend
- COVID vs Non-COVID sales
- Stock level vs Sales
- Expiry days vs Sales

  ## 3. Feature Engineering

Additional date-based features were created to improve the machine learning model.

### Engineered Features

- dayofweek
- quarter
- week

The target variable was:

`units_sold`

The date column was removed from the machine learning feature set.

## 4. Machine Learning

Machine learning was used to predict pharmaceutical units sold.

### Models Used

- Linear Regression
- Random Forest Regressor

### Random Forest Configuration
```text
n_estimators = 200
random_state = 42
```
The dataset was divided into:

80% Training Data
20% Testing Data

using train_test_split with:
random_state = 42

The Random Forest model was used for final model evaluation and feature importance analysis.

## 5. Model Evaluation

The Random Forest model was evaluated using the following regression metrics:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### Model Performance

| Metric | Score |
|---|---:|
| MAE | 65.15 |
| RMSE | 84.83 |
| R² Score | 0.9383 |

The Random Forest model achieved an R² score of 0.9383, indicating a strong fit to the observed sales patterns.

Lower MAE and RMSE values indicate smaller prediction errors.

The model results were saved as:

`data/processed/model_results.csv`

## 6. Feature Importance

Random Forest feature importance was calculated to identify the features that contributed most to the model's predictions.

The feature importance results were saved as:

`data/processed/feature_importance.csv`

Feature importance analysis helps identify the variables that are most useful for predicting pharmaceutical units sold.
## 7. Time Series Forecasting

Time series forecasting was performed using Prophet.

The daily pharmaceutical sales data was aggregated into monthly sales before forecasting.

### Forecasting Process

Daily Sales → Monthly Aggregation → Prophet Model → Future Forecast

### Prophet Configuration

```text
yearly_seasonality = True
weekly_seasonality = False
daily_seasonality = False
```
The forecasting model uses:

- `ds` → Date
- `y` → Actual monthly units sold

### Forecast Period

The model generates 12 future monthly periods.

The forecast output contains the following columns:

| Column | Description |
|---|---|
| ds | Forecast date |
| yhat | Predicted sales |
| yhat_lower | Lower forecast bound |
| yhat_upper | Upper forecast bound |

The forecast results were saved as:

`data/processed/time_series_forecast.csv`

The Power BI dashboard presents the historical sales pattern together with the forecast period extending into 2026.

## Technologies Used

### Programming Language

- Python

### Data Analysis

- Pandas
- NumPy

### Data Visualization

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-learn

### Machine Learning Models

- Linear Regression
- Random Forest Regressor

### Time Series Forecasting

- Prophet

### Business Intelligence

- Microsoft Power BI

### Development Environment

- Google Colab
- Jupyter Notebook

### Version Control

- Git
- GitHub
## Project Structure

```text
pharmaceutical-sales-forecasting-dashboard/
│
├── dashboard/
│   └── Pharmaceutical_Sales_Forecasting_Dashboard.pbix
│
├── data/
│   ├── raw/
│   │   └── raw_global_pharmacy_sales_2020_2025_daily_dataset.csv
│   │
│   └── processed/
│       ├── cleaned_pharmacy_sales.csv
│       ├── feature_importance.csv
│       ├── model_results.csv
│       └── time_series_forecast.csv
│
├── notebooks/
│   ├── Data_Preprocessing.ipynb
│   ├── EDA.ipynb
│   ├── Feature_Engineering.ipynb
│   ├── Model_building.ipynb
│   ├── Model_Evaluation.ipynb
│   └── Time_Series_Forecasting.ipynb
│
├── README.md
└── requirements.txt

```
## Installation

### Clone the Repository

```
```

```
git clone https://github.com/yourusername/pharmaceutical-sales-forecasting-dashboard.git
```

### Navigate to the Project Directory

```
```

```
cd pharmaceutical-sales-forecasting-dashboard
```

### Install Dependencies

```
```

```
pip install -r requirements.txt

```
## Running the Project

Run the notebooks in the following order:

1. `Data_Preprocessing.ipynb`
2. `EDA.ipynb`
3. `Feature_Engineering.ipynb`
4. `Model_building.ipynb`
5. `Model_Evaluation.ipynb`
6. `Time_Series_Forecasting.ipynb`

After generating the processed datasets and forecast results, open the Power BI dashboard:

`dashboard/Pharmaceutical_Sales_Forecasting_Dashboard.pbix`

Open the file using Microsoft Power BI Desktop.

## Processed Outputs

### Cleaned Dataset

`cleaned_pharmacy_sales.csv`

Contains the cleaned and encoded pharmaceutical sales data.

### Model Results

`model_results.csv`

Contains the actual and predicted values from the machine learning model.

### Feature Importance

`feature_importance.csv`

Contains the feature importance values generated by the Random Forest model.

### Time Series Forecast

`time_series_forecast.csv`

Contains the forecast dates, predicted sales, lower forecast bounds, and upper forecast bounds.
## Key Insights

The project provides insights into:

- Overall pharmaceutical sales performance.
- Monthly sales trends.
- Regional sales performance.
- Country-level sales patterns.
- Medicine category performance.
- Stock and sales relationships.
- Expiry days and sales relationships.
- COVID-related sales patterns.
- Important features for sales prediction.
- Future pharmaceutical sales trends.

## Results

The project successfully combines machine learning and time series forecasting with an interactive Power BI dashboard.

The Random Forest model achieved:

- MAE: **65.15**
- RMSE: **84.83**
- R² Score: **0.9383**

The Prophet forecasting model provides future sales estimates together with lower and upper forecast bounds.

The Power BI dashboard presents both business performance analysis and forecasting results in an interactive format.
## Future Enhancements

- Hyperparameter tuning.
- Comparison of additional machine learning algorithms.
- Advanced time series forecasting models.
- LSTM-based sales forecasting.
- Product-level forecasting.
- Region-level forecasting.
- Automated model retraining.
- Real-time sales prediction API.
- Cloud deployment.
- Streamlit web application.
- Automated dashboard updates.

## Author

**Afsal E**

Data Science | Machine Learning | Data Analytics | AI
