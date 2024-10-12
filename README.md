<p align="center">
  <a href="https://www.linkedin.com/in/paramasivam-j-386628270/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn" style="vertical-align: middle; margin-right: 10px;">
  </a>
  <span style="vertical-align: middle; margin-right: 10px;">📧 paramasivamp886@gmail.com</span>
  <a href="https://drive.google.com/file/d/16FtpPhioLH8Jmx-qPDiiT4Jz7fgYA7nS/view?usp=sharing" target="_blank">
    <img src="https://img.shields.io/badge/Resume-FFD700?style=flat&logo=adobeacrobatreader&logoColor=white" alt="Resume" style="vertical-align: middle; margin-right: 10px;">
  </a>
  
</p>

# Drug Sales Forecasting

This project aims to develop a robust forecasting model to predict monthly drug sales, leveraging advanced statistical and machine learning techniques. Accurate drug sales forecasts are crucial for optimizing inventory management, reducing stockouts, and ensuring the timely availability of essential medications. The project integrates historical sales data, epidemiological statistics, and various predictive modeling approaches to provide reliable sales forecasts.

## Table of Contents

- [Data Collection](#data-collection)
- [Data Preprocessing](#data-preprocessing)
- [Model Development](#model-development)
- [Model Evaluation](#model-evaluation)
- [Forecasting](#forecasting)
- [Results](#results)

## Data Collection

The dataset includes monthly sales data for various drug categories from January 2014 to October 2019. The key variables in the dataset are:

- `datum`: Date of the sales record
- `M01AB`, `M01AE`, `N02BA`, `N02BE`, `N05B`, `N05C`, `R03`, `R06`: Sales data for different drug categories
- `total_sales`: Total sales across all categories
- `year`, `month`, `day`: Date components for ease of analysis

## Data Preprocessing

1. **Handling Missing Values**: Checked for and addressed any missing values in the dataset.
2. **Outlier Detection and Treatment**: Identified and treated outliers to ensure data quality.
3. **Feature Engineering**: Created additional features such as moving averages to capture trends and seasonality.
4. **Normalization**: Scaled the data to normalize the range of features for better model performance.

## Model Development

The primary models we developed and evaluated include:

1. **Simple Moving Average (SMA):**

- SMA is a straightforward method that smooths out short-term fluctuations and highlights longer-term trends in the time series data. It calculates the average of the data points in a given window.
- We computed the SMA with a window size of 4 to observe the smoothed trends in monthly drug sales.
  
2. **AutoRegressive (AR) Model:**

- The AR model is a time series forecasting technique that uses the dependency between an observation and a number of lagged observations (i.e., past values). It is particularly useful for datasets with strong autocorrelations.
- We implemented an AR model with a lag order of 1. This model predicts the current value of the series based on its immediately preceding value. The model was trained on the "total_sales" column to capture the underlying patterns and trends.

## Model Evaluation
Models were evaluated based on the following metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

The AR model showed promising results, with a significant coefficient indicating that past sales values are a strong predictor of future sales.

## Forecasting

The AR model was used to forecast future sales. The forecasted values for November and December 2019 are as follows:

2019-11-30    1627.744240

2019-12-31    1896.174586

Freq: M, dtype: float64

## Results

The model successfully forecasted drug sales for the upcoming months with reasonable accuracy. The forecasted values can help in planning and managing drug inventories effectively.



