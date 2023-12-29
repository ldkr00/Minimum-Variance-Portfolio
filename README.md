# MinimumVariancePortfolio

The following Python notebook solves the following tasks:
1. Pull stock returns time series from yahoo finance for ["ADBE", "ZM", "COST", "DIS", "ISRG"]
2. Estimate means and covariances using a 30-day rolling window and solve the minimum variance portfolio problem numerically. Find the weights w_1,....,w_5 such that w_1+....w_5=1 and the portfolio attains minimum variance in the following scenarios:
  a. Short selling allowed
  b. No short selling allowed
  c. Short selling and max(abs(w_i))<0.5
3. Display PnL charts for these portfolios with dynamically changing weights on a daily basis for the last 2 years

Note that all functions are coded generalizable such that one could specify different stocks, different amounts of stocks, a different start date, or different window sizes and the functions would still work. Furthermore, I added the option to use the shrunk Covariance since the historical Covariance based on 30 days has probably very high variance, and shrinking it can make it more robust.
