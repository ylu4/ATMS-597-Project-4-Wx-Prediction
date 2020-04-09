# ATMS-597-Project-4-Wx-Prediction


The goal of this analysis is to (1) Use multiple linear regression to predict a WxChallenge-like forecast using past Global Forecast System (GFS) forecast data. (2) Repeat (1) with random forest regression.

Our task is to use the 12 UTC forecast and observations up to but not including the following 00 UTC to predict the following variables for the period 6 UTC to 6 UTC the following day:

Maximum Temperature (°C)
Minimum Temperature (°C)
Maximum Wind Speed (m/s)
Total precipitation accumulation (mm)


# Dependencies:
Required packages

NumPy

Xarray

Pandas

Wget

Netcdf4

Pydap

Matplotlib

Scikit Learn


# Group Members:
 
1. Carolina Bieri
2. Puja Roy
3. Yang Lu

# Notebooks:
Linear regression: ATMS597_GroupE_LR.ipynb\
Random forest: \
Data processing: ATMS597_GroupE_Utils.ipynb 

# Methodology:

These notebooks include creation and evaluation of multiple linear regression (LR) and random forest (RF) models. Simple versions of each model are created and tested followed by a version with greater complexity. The simple version of each model includes only one predictor: daily GFS maximum/minimum values. The simple models exhibit satisfactory performance which is improved once more predictors are added.
The more complex version of each model includes all available predictors except for DWPC100 (which turned out to contain bad data). In some cases, the observed rainfall variable is not used as a predictor in order to increase the amount of data available for training (rainfall observations were missing on many days, resulting in lost information for other variables). 

## Predictors:
As mentioned previously, daily GFS maximum/minimum values are used as predictors. In the higher-complexity setup, 3-hourly GFS output is used. These data are aggregated to daily means before they are passed to either model. The predictors used for both models are summarized below.

| Simple model | Higher-complexity model |
| ------------- | ------------- |
| TMAX | TMAX |
| TMIN | TMIN  |
| WMAX | WMAX  |
| RTOT | RTOT (only used in precip prediction)  |
|  | DWPC |
|  | TMPC |
|  | WSPD  |
|  | UWND  |
|  | VWND  |
|  | UWND  |

## Final RMSE values:
LR: \
TMAX - 1.91 deg C\
TMIN - 1.73 deg C\
WMAX - 1.58 m/s\
RTOT - 1.521 mm

