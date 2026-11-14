# Foreign Exchange Rate Analysis & Forecasting

## Project Overview
This project analyses historical GBP exchange rates against the Euro (EUR), US Dollar (USD) and Indian Rupee (INR) from 2019 to 2026.

The aim is to understand historical exchange-rate trends, examine currency volatility and relationships, and explore whether machine learning models can forecast the next recorded GBP/USD exchange rate.

## Objectives
- Analyse historical foreign exchange rate movements.
- Identify trends across EUR, USD and INR.
- Calculate currency volatility and correlations.
- Examine monthly and annual exchange-rate patterns.
- Build and evaluate machine learning forecasting models.

## Tools & Technologies
- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- Power BI (dashboard development)

## Methodology
1. Collected historical exchange-rate data using the Frankfurter API.
2. Cleaned and transformed the data using Pandas.
3. Performed exploratory data analysis and visualisation.
4. Calculated daily returns, volatility and correlations.
5. Created lag features for one-step-ahead GBP/USD forecasting.
6. Split the data chronologically into training and testing sets.
7. Trained and compared Linear Regression, Random Forest and a persistence baseline.

## Model Performance

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 0.0018 | 0.0026 | 0.9605 |
| Baseline | 0.0020 | 0.0029 | 0.9525 |
| Random Forest | 0.0024 | 0.0033 | 0.9392 |

Linear Regression achieved the lowest prediction errors and the highest R² score among the three approaches on the test dataset.

## Key Findings
- USD had the highest estimated volatility among the three currencies.
- GBP/USD and GBP/INR daily returns showed a strong positive correlation.
- Exchange-rate movements varied across months and years.
- Linear Regression performed better than the Random Forest model and persistence baseline for the tested forecasting period.

## Data Source
[Frankfurter API](https://frankfurter.dev/)

## Limitations
- The forecasting exercise focuses on GBP/USD.
- Historical exchange-rate patterns do not guarantee future performance.
- The dataset contains weekend observations, so the source's weekend-rate methodology and volatility annualisation assumptions require further verification.
- Model performance is evaluated on a historical test period and may change under different market conditions.

## Project Status
Python analysis and initial forecasting completed. Power BI dashboard development is in progress.
