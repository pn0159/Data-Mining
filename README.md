# Identifying Hypertension cases using Classification models

#About the project

Hypertension plays a significant role in a group of risk factors associated with cardiovascular disease and leading causes of death. My goal in this application of data mining research is to predict hypertension in individuals based on health, 
biomedical, and socio-economic status data.The business case is straightforward: Societies incur significant costs, expend considerable number of resources, and experience a loss of productivity due to a lack of timely diagnosis of serious health conditions.
Except in extreme cases, hypertension is not readily identifiable by individuals due to the lack of recognizable symptoms. Therefore, a predictive tool can help health professionals to identify individuals with high chance of hypertension earlier and before performing 
the diagnostic clinical procedure.The dataset was retrieved from the National Health and Nutrition Examination Survey https://www.cdc.gov/nchs/nhanes/about_nhanes.htm.

This data is the result of a biannual nationally representative cross-sectional study of adults and children in the United States administered by the Center for Disease Control (CDC). The NHANES studies include several surveys, measurements, and quantification of health-related variables.
I’ve selected 52 variables as input features and synthesized a target binary variable for hypertension class label using average of blood pressure readings in the data set.For the initial round of variable selection, given hundreds of available parameters in the NHANES data sets, we reviewed the scientific literature to determine which features were selected by other scholars and analysts. 
I then added additional variables by examining each parameter captured in the NHANES data sets. Through my investigation i am able to select variables believed to have some association with blood pressure and hypertension. 

The core of my analysis consists of the formation and evaluation of five different binary classification models: logistic regression, decision tree, random forest, gradient boosting, and neural networks. To compare the performance of the 
models i defined two key performance indicators aligned with the business goals: recall score and area under the receiver operating characteristic curve. The best performing model was gradient boosting. I selected this as my final 
predictive tool.

At the conclusion of this project, I’ve successfully developed data-driven insights and recommendations to better understand and make decision about hypertension, and an accurate and reliable tool that can be used to predict 
hypertension based on health, biomedical, and socio-economic status data. The results of my analysis could be utilized in hypertension classification and could be included as inference engines in expert systems for hypertension screening 
tools
