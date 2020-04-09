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
Linear regression: \n
Random forest:
Data processing: 

# Methodology:

These notebooks include creation and evaluation of linear regression (LR) and random forest (RF) models. Simple versions of each model are created and tested followed by a version with greater complexity. The simple version of each model includes only one predictor: daily GFS maximum/minimum values. The simple models exhibit satisfactory performance which is improved once more predictors are added.
The more complex version of each model includes all available predictors except for DWPC100 (which turned out to contain bad data). In some cases, the observed rainfall variable is not used as a predictor in order to increase the amount of data available for training (rainfall observations were missing on many days, resulting in lost information for other variables). 

## Predictors:
As mentioned previously, daily GFS maximum/minimum values are used as predictors. In the higher-complexity 


## Final RMSE values:
LR

