# Notes on GARCH Models Course

* **GARCH** Stands for Generalized AutoRegressive Conditional **Heteroskedastiscity**. In ancient greek: _hetero_ - "different" + _skedasis_ "dispersion".
  * The sytematic varying of the volatility of a time series.
* * Heteroskedasticity makes time-series modelling difficult due to the nature of the implied varying levels of fluctuations.
* The predecessor of GARCH is the ARCH model. It was invented to better describe time series with varying volatility (heteroskedastic). It's based on the assumption that the conditional variance errors by random model errors is dependent on the variance errors of the previous period. 
  * i.e. the variance error is _serially autocorrelated_
*  A common example of the difficulties with heteroskedastic time-series are **"volatility clusters"**. Commonly, a sudden upsurge of prices is followed by even more general trend to higher prices. This is due to the shock reaction of the market to rising prices and only the slow recovery from this shock attitude. [Example Image](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.VuWn7iL47b7_3kYHNknDTwHaE4%26pid%3DApi&f=1).
*  (G)ARCH makes prediction on the change in residual. A higher residual (i.e. higher volatility) calls for a prediction of following higher residual (following higher volatility).
*  A **residual** is the difference of an expected (predicted) value to the actual (observed) value. (`residual = predicted - observed`).
* Robert F. Engie, the inventor of the ARCH model,later received the Nobel Prize of Economy for his invention.
* The main difference between GARCH and ARCH Model is GARCH's implementation of a moving average over time. The new parameter `p` for number of lag variances to include allows the prediction of change in variance over time as well as time-dependent variance.
* GARCH is used nowadays for financial analyises due to its higher precision. 
* GARCH has received multiple extensions (e.g. IGARCH, EGARCH) due to its prediction biases. For example, GARCH assumes the same effect on volatility for both good and bad news, i.e. fails to include the "leveraging" effect on uplifting news to disrupt high volatility. 

  
#### Nature of the GARCH Model
* The GARCH Model is basically made out of three variance forecasts:
  * One is the constant `ω` (omega) that takes the long-run average into consideration.
  * One is the forecast `α` (alpha) that introduces new information that was not yet available in the previous forecast.
  * The last one is a forecast `β` (beta) made in the previous period.

The weights of these three determine how fast the variance chances with new information available. Furthermore, it determines how fast the prediction returns to its long-term mean.

* Autoregressive: predictions on the behaviour in the future are based on behaviours of the past.
* Volatility acts as a weighted average of past information.
* The larger `α` (alpha), the bigger the immediate impact
* The larger `β` (beta), the longer the duration of the impact
