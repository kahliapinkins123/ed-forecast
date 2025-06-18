# Emergency Department Volume Forecasting

## Background  
Emergency Departments (EDs) are inherently unpredictable. Patient volume can surge unexpectedly or follow seasonal and event-driven trends such as flu season, holiday weekends, or major local events. These fluctuations create a critical challenge: how do you plan staffing and resources when demand constantly shifts?

Before this project, planning relied on historical averages and anecdotal experience, leading to risks of both over- and under-preparation. I set out to change that with a forecasting system leveraging advanced time series modeling to make our EDs smarter, faster, and better prepared.

## Challenges  
Each hospital campus exhibited unique seasonal and operational patterns, but planning was inconsistent and reactive, lacking formal, scalable forecasting models. External drivers like holidays or events were not systematically included, leaving operations vulnerable during predictable surges.

The goal was to build a robust forecasting system that reflects real-world complexity but remains operationally usable across five hospital locations.

## Solution  
I developed a dual-model forecasting framework using ARIMA and ARIMAX methodologies to predict daily ED volumes for five campuses:

- **Seasonal Decomposition:** Historical patient visit data was decomposed into trend, seasonal, and residual components using Python’s `statsmodels`.  
- **Model Pipelines:** Two forecasting pipelines were built for each site — traditional ARIMA and ARIMAX, the latter incorporating exogenous variables such as holidays and local events.  
- **Site-Specific Models:** Each hospital’s model was independently trained and tuned to capture distinct autocorrelation and seasonal effects.  
- **Evaluation:** Models were compared using RMSE and MAE metrics. Final forecasts feed into operational dashboards guiding staffing and resource decisions.

## Key Features  
- **Dual Forecasting Pipelines:** ARIMA and ARIMAX models to assess the impact of external variables.  
- **Seasonal Decomposition:** Improved pattern isolation by breaking down time series components.  
- **Exogenous Variable Integration:** Dynamic adjustment of forecasts based on known demand drivers.  
- **Location-Specific Tuning:** Customized models per hospital campus reflecting unique operational rhythms.

## Process  
1. Collected and merged multi-year ED visit data, holiday calendars, health outcomes, and economic data.  
2. Cleaned and aligned datasets for temporal consistency, managing missing data and anomalies.  
3. Applied seasonal decomposition for each campus volume history.  
4. Developed and tuned ARIMA and ARIMAX models per site using Python libraries (`statsmodels`, `pmdarima`), optimizing parameters via AIC/BIC.  
5. Validated performance with RMSE, MAE, and compared ARIMA vs ARIMAX.  
6. Integrated final forecasts into scheduled Tableau dashboards used by leadership.

## Impact  
This forecasting system transformed ED planning from reactive guesswork to proactive, data-driven decisions. Forecasts are now actively used across five campuses to:  

- Guide daily staffing and resource allocation.  
- Inform surge planning and long-term hiring.  
- Reduce surprise volume spikes by accounting for holidays/events.  
- Improve patient throughput and reduce wait times through better staffing alignment.

This initiative established a scalable, intelligent operations foundation — setting a new standard for seasonal care delivery preparedness.
