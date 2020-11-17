# week10_time_series_project
- This project forecasts the returns of Japanese Yen via Auto Regressive Moving Average (ARMA), Auto Regressive Integrated Moving Average (ARIMA) and Linear Rgression. Also th volatility of the Yen is projected via Generalized AutoRegressive Conditioal Heteroskedasticity (GARCH)

## Libraries/Technologies used
- arch
- numpy
- pandas
- pathlib
- matplotlib
- statsmodels.api
- statsmodels.tsa.arima_model
- sklearn.linear_model
- sklearn.metrics

## Tools used
- Github
- Gitbash
- Gitlab
- Slack
- Jupyter lab
- Microsoft CSV

## Data Given
- Historical prices of Japanese Yen from 1976

## Notebooks created
- time_series_analysis: ARMA, ARIMA, GARCH forecasts
- regression_analysis: Linear Regression

## Metrics calcuated
- Trend and noise, using Hodrick Prescott filter
- Percentage change in returns from 1990.
- Summary of ARMA results
- Summary of ARIMA results
- Summary of GARCH results
- Annualized 5-day volatility forecast

## Plots created
- Yen settle prices from 1990- 2019
- Yen settle prices vs trend from 2015- 2019.
- Yen noise (outliers) from 1990- 2019
- Five-day returns forecast (using ARMA)
- Five-day prices forecast (using ARIMA)
- Five-day volatility forecast
- Actual returns vs Predicted returns
  (using 2018-2019 as test data)

## Training and Test data
- Training (In-sample): 1990-2017
- Test (Out-of-sample): 2018-2019

## Interpretation of plots
- (For a detailed description, refer to the respective Jupyter notebooks)
- The settle price plot does not exhibit a predictable pattern
- The settle price from 2015- 2019 most closely resembles the trend
- For both the ARMA and ARIMA plots, the p-values are greater than 0.05, indicating that the models are not a good fit.
- For the GARCH model, all p-values except one, are less than 0.05, indicating a potential good fit.
- From the regression analysis, the Root Mean Squared Error of the in-sample data is greater than the out-of sample data, signifying that the training data is an overfit.

## Conclusion
- Based on the analysis, Yen is not a worthy investment
- The risk of the Yen is expected to increase
- The model cannot be used for trading. A Partial Auto Correlation Function (PACF) graph needs to be plotted to determine how many lags have an influence on the other days. Subsequently, the ARIMA needs to be re-run via different values of 'p' (trail and error) to find a reliable model.
- A better way of projecting returns could be to alternatively assign 3 months of data for training and 1 month of data for testing, for the period in consideration.

## Contributors
- Satheesh Narasimman

## People who helped
- Khaled Karman, Bootcamp personal tutor

## References
- https://towardsdatascience.com/understanding-partial-auto-correlation-fa39271146ac

- https://towardsdatascience.com/significance-of-acf-and-pacf-plots-in-time-series-analysis-2fa11a5d10a8

- https://www.machinelearningplus.com/time-series/time-series-analysis-python/

- https://machinelearningmastery.com/arima-for-time-series-forecasting-with-python/