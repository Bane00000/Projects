# [Predicting Disease Spread](https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/)
This project is about predicting the number of dengue cases each week (in each location) based on environmental variables describing changes in temperature, precipitation, vegetation, and more. Dengue fever is a mosquito-borne disease that occurs in tropical and sub-tropical parts of the world. In mild cases, it's similar to flu: fever, rash, and muscle and joint pain. In severe cases, dengue fever can cause severe bleeding, low blood pressure, and even death. Because it is carried by mosquitoes, the transmission dynamics of dengue are related to [climate variables](https://www.wabicc.org/en/manuals/using-climate-information-a-training-manual/climate-variables/). Although the relationship to climate is complex, a growing number of scientists argue that climate change is likely to produce distributional shifts that will have [significant public health implications worldwide](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2014.0135). In recent years dengue fever has been spreading. Historically, the disease has been most prevalent in Southeast Asia and the Pacific islands. These days many of the nearly [half billion](https://www.cdc.gov/dengue/) cases per year are occurring in Latin America. Using environmental data collected by various U.S. Federal Government agencies, I will predict the number of dengue fever cases in San Juan, Puerto Rico and Iquitos, Peru.

# Data
In order to download data, you'll have to make an account at [DrivenData](https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/) website.

## City and date indicators
* city – City abbreviations: sj for San Juan and iq for Iquitos
* week_start_date – Date given in yyyy-mm-dd format

## NOAA's GHCN [daily climate data](https://www.ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily) weather station measurements
* station_max_temp_c – Maximum temperature
* station_min_temp_c – Minimum temperature
* station_avg_temp_c – Average temperature
* station_precip_mm – Total precipitation
* station_diur_temp_rng_c – Diurnal temperature range

## PERSIANN [satellite precipitation measurements](https://www.ncei.noaa.gov/products/climate-data-records/precipitation-persiann) (0.25x0.25 degree scale)
* precipitation_amt_mm – Total precipitation

## NOAA's NCEP [Climate Forecast System Reanalysis](https://rda.ucar.edu/datasets/ds093.0/#metadata/detailed.html?_do=y) measurements (0.5x0.5 degree scale)
* reanalysis_sat_precip_amt_mm – Total precipitation
* reanalysis_dew_point_temp_k – Mean dew point temperature
* reanalysis_air_temp_k – Mean air temperature
* reanalysis_relative_humidity_percent – Mean relative humidity
* reanalysis_specific_humidity_g_per_kg – Mean specific humidity
* reanalysis_precip_amt_kg_per_m2 – Total precipitation
* reanalysis_max_air_temp_k – Maximum air temperature
* reanalysis_min_air_temp_k – Minimum air temperature
* reanalysis_avg_temp_k – Average air temperature
* reanalysis_tdtr_k – Diurnal temperature range

## Satellite vegetation - Normalized difference vegetation index (NDVI) - NOAA's [CDR Normalized Difference Vegetation Index](https://developers.google.com/earth-engine/datasets/catalog/NOAA_CDR_AVHRR_NDVI_V5) (0.5x0.5 degree scale) measurements
* ndvi_se – Pixel southeast of city centroid
* ndvi_sw – Pixel southwest of city centroid
* ndvi_ne – Pixel northeast of city centroid
* ndvi_nw – Pixel northwest of city centroid

# Methodology

## Support Vector Regression
Support Vector Machines (SVMs) are well known in classification problems. The use of SVMs in regression is not as well documented, however. These types of models are known as Support Vector Regression (SVR). SVR gives us the flexibility to define how much error is acceptable in our model and will find an appropriate line (or hyperplane in higher dimensions) to fit the data.

In contrast to OLS, the objective function of SVR is to minimize the coefficients — more specifically, the l2-norm of the coefficient vector — not the squared error. The error term is instead handled in the constraints, where we set the absolute error less than or equal to a specified margin, called the maximum error, ϵ (epsilon). We can tune epsilon to gain the desired accuracy of our model. Our new objective function and constraints are as follows:

![image](https://user-images.githubusercontent.com/102976455/203091430-c1562710-4802-4914-89bb-d84ca6d8ee77.png)

# Model Evaluation
In statistics, mean absolute error (MAE) is a measure of errors between paired observations expressing the same phenomenon. Examples of Y versus X include comparisons of predicted versus observed, subsequent time versus initial time, and one technique of measurement versus an alternative technique of measurement. MAE is calculated as the sum of absolute errors divided by the sample size.

![image](https://user-images.githubusercontent.com/102976455/203092058-f884bc86-be9c-4f1d-84dc-4f4030395a39.png)

# Prediction
In average, my predictions for San Juan, Puerto Rico are 16.038 away from the actual number of dengue cases each week.
![image](https://user-images.githubusercontent.com/102976455/203093351-58d42cfb-b128-46fb-8825-972f67d67ff6.png)
![image](https://user-images.githubusercontent.com/102976455/203093940-ebb2378c-bee6-4ab6-92b1-df96ea1b61ad.png)

As for the Iquitos, Peru, the model is only wrong for 7.010. <br>
![image](https://user-images.githubusercontent.com/102976455/203095008-866cdb92-e151-494f-b5f6-7e111ef2e4fb.png)
![image](https://user-images.githubusercontent.com/102976455/203095575-56269b57-fd63-423f-b762-77cc683239d4.png)


This is due to having less outliers for Iquitos, but that's also because there's less data than San Juan. There are a couple of things I did to prove this. I've split the data for San Juan. Target values (dengue cases) that are above 300, and below 100. I also did this by formula, both of which are in the 0.4 notebook. When working with only target values (dengue cases) below 100, I got a 10.92 mean absolute error. Which improved my previous model for about 5.4. <br>
![image](https://user-images.githubusercontent.com/102976455/203097446-644587c7-4e43-4fe0-ac0f-0b8a3db0917f.png)
![image](https://user-images.githubusercontent.com/102976455/203097505-c3cfe418-8928-43a3-ab1e-29a0a9e6d779.png)

When done by formula, the model is slightly better, with the mean absolute error of 10.50.


# Credits
* Methodology: https://towardsdatascience.com/an-introduction-to-support-vector-regression-svr-a3ebc1672c2
* Model Evaluation: https://en.wikipedia.org/wiki/Mean_absolute_error
