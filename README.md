# Time_series_web_traffic
Forecasting the future values of multiple time series. More specifically the problem of forecasting future web traffic for approximately 145,000 wikipedia articles.

two csv files
one is about article and the respective visits on a specific day. (the areticles are from different languages and different regions)
the other data is about exogeneous variable which specifying weather a day is holiday or not.

Steps I followed:
1. Imported the dataset and did exploratory data analysis.
2. checked the null values and their reason.
3. Understood the page name format and splitted it to get different information.
4. Separated different values from it like title, language, access type, and access origin
5. Converted the data to a format that can be fed to the Arima model (Pivoting etc)
6. Checked the data is stationary or not using Dickey-Fuller test
7. Tried different methods for stationary using decomposition and differencing
8. Plotted the ACF and PACF plots and the corresponding orders p,q 
9. Created the training with the Arima model.
10. Used the exogenous variable to  train a sarimax model
11. Used facebook prophet for forecasting
