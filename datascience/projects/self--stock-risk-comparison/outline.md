# Outline
Available data: AMD, NVDA, INTL historical stock data.

### Goal of Analysis
Between the stocks of the two chip manufacturers AMD (_AMD_) and NVIDIA (_NVDA_), which one serves as a more risk-free investment if the total tolerance of loss is at 30% of the investment value?
#### Subquestions
- What are the volatilities of the individual stocks?
- What's the VaR values at the 30% loss threshold?
- What can be forecasted for both stocks?
- Is a single investment in one of them the most promising solution, or a weighted combination of both?

### Data Handling
* Source of data: yahoo! Finances
Trusted source for historical stock data of big companies.
* Same source = Same data structure -> Less adjuments and subsetting.
* Exported frame of time: Apr. 13 2016 - Apr. 13 2021. (5y)

Potential handling of the data:
* Subset to smaller timeframe, e.g. last 180 days for more relevant "recent" insights (time-series data as stocks might be heteroskedastic).
* Addition of extra columns, as daily percentual change to previous entry, difference of _n-1_ close to _n_ open (night market)
  
### Methods
* Most relevant columns: Date, Open, Adj. Close. Adjusted Close serves as a cleaned up version of the Close value of a day and is the standard to rather include in calculations as simple Close value.
* Secondary columns: High, Low to determine intra-day maximum range of volatility. Are the stocks volatile over the day?
  
Methods to acquire insights on risk: 
* Volatility computation and visualization of different volatility functions (CC, Parkinson or Yang Zhang).
* Value at Risk determiniation on defined risk parameters (e.g. 30% loss tolerance threshold)
* Comparison of return-per-risk with Sharpe Ratio
* Forecast on volatility model and VaR calculation with GARCH models.
* Visualization of time-series with lineplots, histograms with distribution line for visualizing and analyizing statistical values to determine distribution (normal, students t-dist, skewed t distribution?) and their implications. Scatter plots for VaR visualization, draw threshold line to highlight outliers (VaR exceedances).

