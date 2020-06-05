
# Project 4: West Nile Virus Prediction

 By : Don, Emily, Gabriel, Vincent, Will

# Executive Summary
---

# 1. Problem Statement

The deadly, mosquito-borne West Nile Virus has long infested the City of Chicago. It is imperative to develop an accurate predictive model that could identify the key contributing factors that leads to proliferation of the virus. The model and the insights drawn could help the authority to predict future outbreaks of West Nile Virus and thus effectively allocate resources to mitigate it.

Logistic Regression, Naive Bayes, Extra Trees and XGboost models will be used to model the data and Accuracy and Recall score will be used to evaluate and find the best model for production and prediction.

---

# 2.  Overview

The summary of the process is to clean the data, perform EDA, data visualization , analysis via descriptive and inferential statistics, using pipeline and gridsearch to model and fine tune the model, evaluate and select the best model for production and to use on the Kaggle data set for prediction and submission. Outside research will be conducted and the conclusions and recommendations are provided below.

---

# 3. Contents

1. [Data Cleaning](01_Data_Cleaning.ipynb)


2. [EDA and Modeling](02_EDA_and_Modeling.ipynb)


3. [Cost Benefit Analysis](03_Cost_Benefit_Analysis.ipynb)


---

# 4. Conclusion

The Logistic Regression  without PCA was selected and fine tuned as it had best balance between the Accuracy and Recall scores to generalize on unseen data as compared to the Naive Bayes, Extra Trees and XGBoost models, with a Accuracy Score of 0.702 and Recall Score of 0.772 on the test data.


---

# 5. Cost Benefits Analysis

By inferring the benefit-cost ratio of 3.34, it shows more benefit of spraying over costs implying that spraying might be a cost effective way to control the WNV in Chicago.

However according to our marked zones, there are existing spraying that was done on the low risk zones (Zone 1) which might lower the effectiveness of spraying. Furthermore, we found that there are several areas in Zone 3 which doesn't have any spraying activities. This might increase the possibilities of WNV infection as the old people residing in those areas are more prone to contract of virus.

Hence, we would like to propose to the council of Chicago to prioritise spraying in those higher risk zone (Zone 2 and Zone 3). It will be prudent to target specific areas to spray for example, the remaining Zone 3 to increase the effectiveness of vector control.

---
# 6. Recommendations

By inferring the benefit-cost ratio of 3.34, it shows more benefit of spraying over costs implying that spraying might be a cost effective way to control the WNV in Chicago.

However according to our marked zones, there are existing spraying that was done on the low risk zones (Zone 1) which might lower the effectiveness of spraying. Furthermore, we found that there are several areas in Zone 3 which doesn't have any spraying activities. This might increase the possibilities of WNV infection as the old people residing in those areas are more prone to contract of virus.

Hence, we would like to propose to the council of Chicago to prioritise spraying in those higher risk zone (Zone 2 and Zone 3). It will be prudent to target specific areas to spray for example, the remaining Zone 3 to increase the effectiveness of vector control.

---
# 7. Limitations and further considerations

Chicago uses a truck to spray insecticide, hence spraying effectiveness is limited to areas near roads where the truck is able to spray. Spraying should only be part of Chicago's toolbox to manage the vectors of the West Nile virus

There could also be other reasons for the decline in the number of WNV present such as other mosquito control efforts like larvicide implementation, varying effectivness of spraying in different ecological areas, increased implementation of personal protective measures in sprayed areas.

Chicago can consider including data on larvicide and personal protective measures to filter out their effects and increase the ability to determine spraying effectiveness.

---
# 8. References

 Data dictionary


|Feature|Type|Description|
| --- | --- | --- |
 |Id  <br/>(train.csv)            |int      | the id of the record
 |Date <br/>(train.csv)          |datetime      |date the WNV test is performed
 |Address <br/>(train.csv)     |datetime | approximate address of the location of trap. This is used to send to the GeoCoder
 |Species  <br/>(train.csv)       |str      | the species of mosquitos
 |Block <br/>(train.csv)        |str      |block number of address
 |Street <br/>(train.csv)       |str      |street name
 |Trap <br/>(train.csv)         |str    |ID  of the trap
 |AddressNumberAndStreet <br/>(train.csv)|str| approximate address returned from GeoCoder
 |Latitude <br/>(train.csv)           |float|latitude and Longitude returned from GeoCoder
 |Longitude <br/>(train.csv)           |float| longitude and Longitude returned from GeoCoder
 |AddressAccuracy <br/>(train.csv)     |int| accuracy returned from GeoCode
 |NumMosquitos <br/>(train.csv)       |int      | number of mosquitoes caught in the specific trap
 |WnvPresent  <br/>(train.csv)         |int      | whether West Nile Virus was present in the mosquitos in the traps. 1 means WNV is present, and 0 means not present
 |Date <br/>(spray.csv)|datetime | date of spray
 |Time <br/>(spray.csv)        |datetime      | time of the spray
 |Latitude <br/>(spray.csv)|float| latitude of spray
 |Longitude <br/>(spray.csv)       |float| longitude of the spray
 |Station <br/>(weather.csv) |int| weather station ID
 |Date  <br/>(weather.csv)   |datetime| date of weather measurement
 |Tmax  <br/>(weather.csv)   |int| maximum temperature (F)
 |Tmin  <br/>(weather.csv)   |int| minimum temperature (F)
 |Tavg  <br/>(weather.csv)|int| average temperature (F)
 |Depart <br/>(weather.csv)    |int| departure from normal temperature (F)
 |Dewpoint <br/>(weather.csv)   |int| average dew point (F)
 |WetBulb <br/>(weather.csv)  |int| average wet bulb (F)
 |Heat <br/>(weather.csv)    |int| degree days of heat (base 65 F)
 |Cool <br/>(weather.csv)  |int| degree days of cool (base 65 F)
 |Sunrise <br/>(weather.csv)    |int| time of sunrise (calculated)
 |Sunset <br/>(weather.csv)    |int| time of sunset (calculated)
 |CodeSum <br/>(weather.csv)    |str| code of weather type
 |Depth <br/>(weather.csv)    |int| snow depth (inch)
 |Water1 <br/>(weather.csv) |int| water equivalent (inch)
 |SnowFall <br/>(weather.csv)    |int|snowfall (inch)
 |PrecipTotal <br/>(weather.csv)    |str|Amount of rainfall (inch)
 |StnPressure <br/>(weather.csv)    |int|average station pressure (inch hg)
 |SeaLevel <br/>(weather.csv)    |int|average sea level pressure (inch hg)
 |ResultSpeed <br/>(weather.csv) |float|wind speed (mph)
 |ResultDir <br/>(weather.csv)    |int|wind direction (degrees)
 |AvgSpeed <br/>(weather.csv)    |int|average wind speed (mph)


Presentation

Bellini, R., Zeller, H. & Van Bortel, W. A review of the vector management methods to prevent and control outbreaks of West Nile virus infection and the challenge for Europe. Parasites Vectors 7, 323 (2014). https://doi.org/10.1186/1756-3305-7-323

Idph.state.il.us. 2020. West Nile Virus In Illinois - Surveillance. [online] http://www.idph.state.il.us/envhealth/wnvsurveillance_humancases_13.htm

Ruktanonchai, Duke J et al. “Effect of aerial insecticide spraying on West Nile virus disease--north-central Texas, 2012.” The American journal of tropical medicine and hygiene vol. 91,2 (2014): 240-5. doi:10.4269/ajtmh.14-0072

Yao, Yi, and Ruth R Montgomery. “Role of Immune Aging in Susceptibility to West Nile Virus.” Methods in molecular biology (Clifton, N.J.) vol. 1435 (2016): 235-47. doi:10.1007/978-1-4939-3670-0_18
