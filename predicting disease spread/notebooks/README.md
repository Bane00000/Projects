# [Predicting Disease Spread](https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/)
This project is about predicting the number of dengue cases each week (in each location) based on environmental variables describing changes in temperature, precipitation, vegetation, and more. Dengue fever is a mosquito-borne disease that occurs in tropical and sub-tropical parts of the world. In mild cases, it's similar to flu: fever, rash, and muscle and joint pain. In severe cases, dengue fever can cause severe bleeding, low blood pressure, and even death. Because it is carried by mosquitoes, the transmission dynamics of dengue are related to [climate variables](https://www.wabicc.org/en/manuals/using-climate-information-a-training-manual/climate-variables/). Although the relationship to climate is complex, a growing number of scientists argue that climate change is likely to produce distributional shifts that will have [significant public health implications worldwide](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2014.0135). In recent years dengue fever has been spreading. Historically, the disease has been most prevalent in Southeast Asia and the Pacific islands. These days many of the nearly [half billion](https://www.cdc.gov/dengue/) cases per year are occurring in Latin America. Using environmental data collected by various U.S. Federal Government agencies (check credits for links), I will predict the number of dengue fever cases in San Juan, Puerto Rico and Iquitos, Peru.

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

# Model
