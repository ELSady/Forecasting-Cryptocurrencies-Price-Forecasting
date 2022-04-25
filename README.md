## Data Science Project Forecasting : Cryptocurrencies Price Forecasting with SARIMA and FBProphet Overview
* Analyze the time series of how cryptocurrencies price changes over the years.
* Time series stationary checking using Dickey Fuller Method
* Time series differentiation to make it stationer. Ensuring the Arima model works for the data.
* Time series Decomposition, separating the trend, seasonal and residual components.
* Preparing time series dataset for forecasting
* Build Forecasting Model and predict the Prices.

### Code and Resources Used
* Packages: pandas, numpy, datetime, matplotlib, seaborn, statsmodel, pmdarima, fbprphet.

### Project Highlight

### Time Series Visualization <br>


### Series Stationary Checking <br>
* Theres a big difference between rolling mean and its standard deviation, it is very clear that the serires is not stationary. The p value is also greater than 0.05 then, the null hypothesis (time serires stationary) is rejected.
*
* DIckey Fuller Test Result
> Test Statistics                   0.157982 <br>
> p-value                           0.969804 <br>
> No. of lags used                 31.000000 <br>
> Number of observations used    4024.000000 <br>
> critical value (1%)              -3.431976 <br>
> critical value (5%)              -2.862259 <br>
> critical value (10%)             -2.567152 <br>
>
### Decomposition
* The trend and seasonily decmoposition. The existence of those 2 componnets indicated that the series is not stasionary

### Preparing Series before Forecasting
* Applying log transformation to the series. It is done to remove the trend components and flatten out the its standard deviation, it is also a way for the ARIMA model better read the series.

### AUTO ARIMA Model Building
* Automated ARIMA model for the series. AUTO ARIMA simplifies the user to define which parameters, the likes of AR (p), MA (q) and differentitation (d) suit the series best.

* ARIMA Model Plot Interpretation :
* **Standardized residual**: The residual errors fluctuate around a mean of zero and have a uniform variance.
* **Histogram**: The density plot suggest normal distribution with mean.
* **Theoretical## Quantiles**: Mostly the dots fall perfectly in line with the red line. Any significant deviations would imply the distribution is skewed.
* **Correlogram**: The Correlogram, (or ACF plot) shows the residual errors are not autocorrelated. The ACF plot would imply that there is some pattern in the  residual errors which are not explained in the model.

### FBProphet Forecasting and Components
* Forecasting <br>


* Forecast Components <br>
