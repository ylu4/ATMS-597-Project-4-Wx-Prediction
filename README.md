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

# Methodology

Linear regression (LR) and random forest (RF) models were developed to complete this assignment. "Simple" versions of each model were tested first, followed by a version with greater complexity. 

