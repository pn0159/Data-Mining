# Identifying Hypertension cases using Classification models

# About the project

Hypertension plays a significant role in a group of risk factors associated with cardiovascular disease and leading causes of death. My goal in this application of data mining research is to predict hypertension in individuals based on health, biomedical, and socio-economic status data.The business case is straightforward: Societies incur significant costs, expend considerable number of resources, and experience a loss of productivity due to a lack of timely diagnosis of serious health conditions.Except in extreme cases, hypertension is not readily identifiable by individuals due to the lack of recognizable symptoms. Therefore, a predictive tool can help health professionals to identify individuals with high chance of hypertension earlier and before performing the diagnostic clinical procedure.

This data is the result of a biannual nationally representative cross-sectional study of adults and children in the United States administered by the Center for Disease Control (CDC). The NHANES studies include several surveys, measurements, and quantification of health-related variables.
I’ve selected 52 variables as input features and synthesized a target binary variable for hypertension class label using average of blood pressure readings in the data set.For the initial round of variable selection, given hundreds of available parameters in the NHANES data sets, we reviewed the scientific literature to determine which features were selected by other scholars and analysts. I then added additional variables by examining each parameter captured in the NHANES data sets. Through my investigation i am able to select variables believed to have some association with blood pressure and hypertension. 

The core of my analysis consists of the formation and evaluation of five different binary classification models: logistic regression, decision tree, random forest, gradient boosting, and neural networks. To compare the performance of the models i defined two key performance indicators aligned with the business goals: recall score and area under the receiver operating characteristic curve. At the conclusion of this project, I’ve successfully developed data-driven insights and recommendations to better understand and make decision about hypertension, and an accurate and reliable tool that can be used to predict hypertension based on health, biomedical, and socio-economic status data. The results of my analysis could be utilized in hypertension classification and could be included as inference engines in expert systems for hypertension screening tools.

# Data Source

The dataset was retrieved from the National Health and Nutrition Examination Survey https://www.cdc.gov/nchs/nhanes/about_nhanes.htm.


In my analysis, I’ve used data samples collected through the National Health and Nutrition Examination Survey (NHANES) which is one of the most comprehensive publicly available health data sets and a principal source for tracking hypertension in the U.S. population. The NHANES data collection campaigns are designed to assess the health and nutritional status of adults and children across the United States. The data in this survey is unique because it combines social determinants of health data such as smoking, alcohol consumption, dietary habits, and physical examinations with laboratory results. This survey instrument placed emphasis on the data regarding the prevalence of major diseases and risk factors for diseases for a broader population than just data from a medical facility. The latter contains only data for a small subset of the population and does not represent the entire picture of significant disease. In addition, historically, disease trends in the United States have been assessed by surveys.

# Analytical Approaches

After data preparation, i probed the data using exploratory analysis techniques such as graphical charts and statistical summaries. The objective of this step is to understand the data better and discover possible meaningful patterns. I’llperform a Chi-squared test to identify the variables that are not independent of the target variable. This step was not 
performed for the purpose of excluding any variables. But it did serve to better understand the relationship between the features and the target. Because i have calculated average values of the systolic and diastolic pressure measurements, i can build a linear regression model between blood pressure (dependent variable) and input variables. The objective of 
the project is not to predict the exact blood pressure values but building a linear regression model would be helpful to understand the relationship between the variables better.
At the core of my analysis is the building and evaluation of five different binary classification models: logistic regression, decision tree, random forest, gradient boosting, and neural networks. I’ve evaluated the performance of each model i calculated by using a confusion matrix, ROC plot, and AUC. Finally, i created an ensemble model to develop the best 
model out of the five classifiers. My goal was to predict hypertension with minimum false positive rate and maximum recall.

For this project I’ve used Python and Excel for part of the data pre-processing, Tableau for some of the visualization work, and SAS Enterprise Miner OnDemand for data exploration, model building, and evaluation.

# Data Preprocessing

1. Interval variables

2. Categorical variables

3. Linear regression analysis

# Classification Models

1. Logistic Regression

2. Decision Trees

3. Random Forest

4. Gradient Boosting

5. Neural Networks

# Model Selection

For the model selection I used sensitivity (recall) and ROC AUC scores of the optimized models in the cross-validation training phase.  My final model is gradient boosting with the hyperparameters shown below:

Optimal hyperparameter space for the gradient boosting model:

Hyperparameter Name in SAS with Optimum Value:

Maximum Branch-4 , Maximum Depth-4, Reuse Variable-3, Leaf Fraction-0.01,N Iterations-400, Shrinkage-0.01, Train Proportion-60                             

The AUC of the selected model is 0.98 and the recall scores is 0.89 which shows very few missing true positive cases. To evaluate the performance of the selected model on unseen data, i applied it on the test data set that was put aside at the beginning of the model development process.The recall score of the test data set is 0.71. Loss of the classification performance which is expected when the model is applied on new data is in a  reasonable range.

# Summary

In this project, I’ve developed a classification model to identify people with hypertension using their health, demographic, dietary habits, and lab data. Hypertension is a primary or contributing cause of approximately half a million death in the US and it can exist in a person undetected without significant symptoms. Early identification of 
hypertension by healthcare professionals can help physicians and patients start treatment earlier to prevent or reduce serious consequences. For this project, I’ve used five periods of NHANES data for data exploration and predictive tool building. This data set is collected by CDC and is one of the most comprehensive and representative publicly available health data sets and a principal source for tracking conditions such as hypertension in the U.S. population. The data set in this project consisted of 22,151 records, each represents one person in the surveys. My exploratory data analysis revealed interesting and useful patterns. On average 42% of the people whose doctor has told them they have high blood pressure, do not have hypertension based on their blood pressure readings in the NHANES survey. Also, 26% of those whom no doctor has ever said they have high blood pressure, have hypertension. While the underlying causes of this inconsistency should be investigated, a reliable predictive tool such as the one I have developed in this project can help healthcare professionals identify positive and negative cases more efficiently. My data also showed the habit of adding salt to food and eating poorly can increase the likelihood of hypertension. The associations of kidney problems, diabetes, smoking, low physical activity, and obesity with hypertension are also reflected in data. Also, being male and black is associated with high blood pressure. For developing a predictive tool, I’ve built and tuned five classification models in SAS EM. I’ve chose sensitivity score and AUC as my key performance indicators because missing a positive case can be significantly more expensive than misidentifying a negative case. Out of the five models, performance metrics of the Gradient Boosting model performed best, and was selected to be my final predictive model.The exploratory data analysis and predictive tool that i developed in this project can be directly used by healthcare professionals to both understand the patterns of hypertension and predict it in a faster, more reliable, and cheaper 
fashion.
