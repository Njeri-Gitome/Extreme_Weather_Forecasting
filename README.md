# Extreme_Weather_Forecasting
WiDS Datathon 2023 - Adapting to Climate Change by Improving Extreme Weather Forecasts

 #### Data Overview
The WiDS Datathon 2023 focuses on a prediction task involving forecasting sub-seasonal temperatures (temperatures over a two-week period, in our case) within the United States. We are using a pre-prepared dataset consisting of weather and climate information for a number of US locations, for a number of start dates for the two-week observation, as well as the forecasted temperature and precipitation from a number of weather forecast models (we will reveal the source of our dataset after the competition closes). Each row in the data corresponds to a single location and a single start date for the two-week period.

#### Datasets 
- **train_data.csv**: the training dataset, where contest-tmp2m-14d__tmp2m, the arithmetic mean of the max and min observed temperature over the next 14 days for each location and start date, is provided<br>

- **test_data.csv**: the test dataset, where we withhold the true value of contest-tmp2m-14d__tmp2m for each row.<br>

#### Objective
To predict the arithmetic mean of the maximum and minimum temperature over the next 14 days, for each location and start date.

#### Variable naming
Each variable name, prefix__suffix, consists of two parts (separated by a double underscore) that inform you of the meaning of the variable. The prefix indicates from which of the above-listed file the variable was derived (e.g. Madden-Julian oscillation, pressure, and potential evaporation from NOAA's surface_gauss etc), the suffix indicates the specific type of information that was extracted from the file.

#### Variable Prefixes

- **contest-slp-14d**: file containing sea level pressure (slp)<br>

- **nmme0-tmp2m-34w**: file containing most recent monthly NMME model forecasts for tmp2m (cancm30,cancm40, ccsm30, ccsm40, cfsv20, gfdlflora0, gfdlflorb0, gfdl0, nasa0,nmme0mean) and average forecast across those models (nmme0mean)<br>

- **contest-pres-sfc-gauss-14d**: pressure<br>

- **mjo1d**: MJO phase and amplitude<br>

- **contest-pevpr-sfc-gauss-14d**: potential evaporation<br>

- **contest-wind-h850-14d**: geopotential height at 850 millibars<br>

- **contest-wind-h500-14d**: geopotential height at 500 millibars<br>
- **contest-wind-h100-14d**: geopotential height at 100 millibars<br>

- **contest-wind-h10-14d**: geopotential height at 10 millibars<br>

- **contest-wind-vwnd-925-14d**: longitudinal wind at 925 millibars<br>

- **contest-wind-vwnd-250-14d**: longitudinal wind at 250 millibars<br>
- **contest-wind-uwnd-250-14d**: zonal wind at 250 millibars<br>

- **contest-wind-uwnd-925-14d**: zonal wind at 925 millibars<br>

- **contest-rhum-sig995-14d**: relative humidity<br>

- **contest-prwtr-eatm-14d**: precipitable water for entire atmosphere<br>
- **nmme-prate-34w**: weeks 3-4 weighted average of monthly NMME model forecasts for precipitation<br>

- **nmme-prate-56w**: weeks 5-6 weighted average of monthly NMME model forecasts for precipitation<br>
- **nmme0-prate-56w**: weeks 5-6 weighted average of most recent monthly NMME model forecasts for precipitation<br>

- **nmme0-prate-34w**: weeks 3-4 weighted average of most recent monthly NMME model forecasts for precipitation<br>

- **nmme-tmp2m-34w**: weeks 3-4 weighted average of most recent monthly NMME model forecasts for target label, contest-tmp2m-14d__tmp2m<br>

- **nmme-tmp2m-56w**: weeks 5-6 weighted average of monthly NMME model forecasts for target label, contest-tmp2m-14d__tmp2m<br>

- **mei**: MEI (mei), MEI rank (rank), and Niño Index Phase (nip)<br>

- **elevation**: elevation<br>

- **contest-precip-14d**: measured precipitation<br>

- **climateregions**: Köppen-Geigerclimateclassifications<br>

- #### Variables without prefix

Some variables do not have a prefix. Instead, each variable name in its entirely indicates the information the variable captures.<br>

- **lat**: latitude of location (anonymized)<br>
- **lon**: longitude of location (anonymized)<br>
- **startdate**: startdate of the 14 day period<br>
- **sst**: sea surface temperature<br>
- **icec**: sea ice concentration<br>
- **cancm30, cancm40, ccsm30, ccsm40, cfsv20, gfdlflora0, gfdlflorb0, gfdl0, nasa0, nmme0mean**: most recent forecasts from weather models<br>
#### Target
- **contest-tmp2m-14d__tmp2m**: the arithmetic mean of the max and min observed temperature over the next 14 days for each location and start date, computed as (measured max temperature + measured mini temperature) / 2