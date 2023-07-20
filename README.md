# Extreme_Weather_Forecasting
WiDS Datathon 2023 - Adapting to Climate Change by Improving Extreme Weather Forecasts

 #### Data Overview
The WiDS Datathon 2023 focuses on a prediction task involving forecasting sub-seasonal temperatures (temperatures over a two-week period, in our case) within the United States. We are using a pre-prepared dataset consisting of weather and climate information for a number of US locations, for a number of start dates for the two-week observation, as well as the forecasted temperature and precipitation from a number of weather forecast models (we will reveal the source of our dataset after the competition closes). Each row in the data corresponds to a single location and a single start date for the two-week period.

#### Datasets 
- **train_data.csv**: the training dataset, where contest-tmp2m-14d__tmp2m, the arithmetic mean of the max and min observed temperature over the next 14 days for each location and start date, is provided<br>

- **test_data.csv**: the test dataset, where we withhold the true value of contest-tmp2m-14d__tmp2m for each row.<br>

#### Objective
To predict the arithmetic mean of the maximum and minimum temperature over the next 14 days, for each location and start date.
