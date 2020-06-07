# Project 4: West Nile Virus Prediction
#### Group 2: Don, Emily, Gabriel, Vincent, Will 
#### 8 June, 2020


## Problem Statement

The deadly, mosquito-borne West Nile Virus has long infested the City of Chicago. It is imperative to develop an accurate predictive model that could identify the key contributing factors that leads to proliferation of the virus. The model and the insights drawn could help the authority to predict future outbreaks of West Nile Virus and thus effectively allocate resources to mitigate it.

The accuracy and recall score from different machine-learning models will be compared and used to evaluate to find the best model for production and prediction.


## Executive Summary

**Exploratory Data Analysis**

It has been found that the 3 main species of WNV-positive mosquitoes are Culex Pipens, Culex Restuans and the Culex Pipens/Restuans Complex. Peak Seasons for Mosquitos has shown to be from around June to September and the optimal temperature range is around 65 to 80 degrees Fahrenheit. 

From the data of mosquito traps collected, the WNV-positive mosquitoes mainly comes from two sources of areas.  the neighbourhoods which have the highest WNV-positive mosquitoes in traps are at O'Hare (Northwest) and South Deering (SouthEast). O'Hare has found to have many retention ponds for airport stormwater control, whereas South Deering is an industrial estate with swamplands. It can be infered as a result, the stagnation of water pool in both neighbourboods provides a habitable breeding spot for these mosquitoes. The districts adjacent to O'Hare, such as Dunning and Norwood Park, has also suffered an outbreak of WNV-positive mosquitoes.


**Modelling**

Logistic Regression, Naive Bayes, Extra Trees and XGboost models are used to model the data. There is a heavy class-imbalance in the data, at 19:1 ratio of WNV-negative against WNV-positive mosquito traps. The Synthetic Minority Over-sampling Technique (SMOTE) was used to adjust for the imbalance. 

Logistic Regression has shown to be the best performing model at an overall accuracy of 70%, with recall and specificity scores of 77% and 70% respectively. 


**Cost Benefit Analysis**  

Vector Controls, which include aerial spraying of pyretherins for six nights, has reported to have benefits in the form of both medical costs reductions as well as productivity increases. The benefit-cost ratio (in US$) has is estimated to be around 3.8.  


## Conclusions & Recommendations

To sum up, the West Nile Virus is a seasonal outbreak which peaks during the summer. Temperature and Rainfall are the main causes for the outbreaks. With this data in mind, the disease control authorities can prepare for these peak periods and mitigate the airborne of the virus through the mosquitoes. 

Spraying can be target at high risk zones, identified to be arond the Northwest (O'Hare) and Southeast (South Deering) regions. Major breeding grounds such as O'Hare and South Deering have found often to have stagnant water, especially during summer where there are increased levels in rainfall. Concentrating spraying on these areas can save limited spraying resources and amplify the effectiveness on targeting WNV-positive mosquitoes. 


### Recommendations
  

**Neighbourhood Outbreak Risk Zoning**

The authorities can consider categorizing the different Chicago districts into zones, based on their risk towards a WNV outbreak, as well as the demographics of each district. Some districts have found to have a higher porportion of citizens who can be classified as dependencies (ages under 18 and above 65). These groups of people may have a weaker immune system than an middle-aged adult and it is of importance that the welfare of these dependencies are taken care of. High-risk zones can be demarcated as districts with high WNV-positive moquito count, as well has a high dependencies number. 


### Considerations 

More research can be conducted with regards to larvicide implementation, as well as increased personal protective measures. 

For larvicide implementation, if the disease control authorities are able to halt the life cycle of mosquitoes, this will aid the prevention in mosquitoes being airborne and spreading WNV at a faster rate. 

More data can certainly be gathered about personal protective measures for an added layer of protections. Such measures can include mosquito repellents in the form of sprays, coils and patches. If the denizens of Chicago were to be aware of prevention measures, it maybe even a better solution than chemical fogging of mosquitoes.  



