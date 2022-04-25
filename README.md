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
![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index.png)

* The plot displays the changes of Bitcoin over the past 10 years. We can see, theres a price surge at the start of 2017, this is primarily because cryptmining is becoming a thing at the time. The trend continoues until the year of 2019 where its price dips a little, but then the folowing year it surges, especially at the start of 2021. we see a massive spike in price.

### Series Stationary Checking <br>
![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index1.png)

* Theres a big difference between rolling mean and its standard deviation, it is very clear that the serires is not stationary. The p value is also greater than 0.05 then, the null hypothesis (time serires stationary) is rejected. 

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
* The trend and seasonily decmoposition. The existence of those 2 componnets indicated that the series is not stasionary <br>

![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index2.png)

### Preparing Series before Forecasting
* Applying log transformation to the series. It is done to remove the trend components and flatten out the its standard deviation, it is also a way for the ARIMA model better read the series. <br>

![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index3.png)

### AUTO ARIMA Model Building
* Automated ARIMA model for the series. AUTO ARIMA simplifies the user to define which parameters, the likes of AR (p), MA (q) and differentitation (d) suit the series best. <br>

![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index4.png)

* ARIMA Model Plot Interpretation :
* **Standardized residual**: The residual errors fluctuate around a mean of zero and have a uniform variance.
* **Histogram**: The density plot suggest normal distribution with mean.
* **Theoretical## Quantiles**: Mostly the dots fall perfectly in line with the red line. Any significant deviations would imply the distribution is skewed.
* **Correlogram**: The Correlogram, (or ACF plot) shows the residual errors are not autocorrelated. The ACF plot would imply that there is some pattern in the  residual errors which are not explained in the model.

* Forecasting <br>

![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index5.png)

### FBProphet Forecasting and Components
* Forecasting <br>

![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index6.png)

* Forecast Components <br>

![alt text](https://github.com/ELSady/Forecasting-Cryptocurrencies-Price-Forecasting/blob/main/index7.png)
