# Lung Cancer Predictive Model

## Overview

### Goal
This python code analyzes data of a fictional telco company that provided home phone and internet services to 7043 customers in California in Q3. The goal is build a classification model that could predict if a individual will have lung cancer or not. Below are the questions that the project answers.

* What are the distributions of each variable?
* What is the relationship of each variable with PLUMONARY_DISEASE?

### Data
The initial dataset contains 5000 rows, each representing a person, and 18 columns.  
Source: https://www.kaggle.com/datasets/shantanugarg274/lung-cancer-prediction-dataset  

#### Variables
* AGE
* GENDER
* SMOKING
* FINGER_DISCOLORATION
* MENTAL_STRESS
* EXPOSURE_TO_POLLUTION
* LONG_TERM_ILLNESS
* ENERGY_LEVEL
* IMMUNE_WEAKNESS
* BREATHING_ISSUE
* ALCOHOL_CONSUMPTION
* THROAT_DISCOMFORT
* OXYGEN_SATURATION
* CHEST_TIGHTNESS
* FAMILY_HISTORY
* SMOKING_FAMILY_HISTORY
* STRESS_IMMUNE
* PULMONARY_DISEASE

### Methodology
In order to create the best predictive model, 4 classification models are built: Logistic Regression (2), K-Nearest Neighbors (KNN) and Support Vector Machines (SVM). GridSearchCV is used to choose the optimal parameters in all models except for the first logistic regression model. Only 10% is used for the test set since the dataset is big. The dataset was scaled before running the models.

### Findings
The ages of participants go from 30 to 84 years with a mean of 57 years. Having lung cancer seems to be equally distributed across ages.  
Having lung cancer seems to be equally distributed across oxygen saturation.  
Energy level goes from 23.25 to 83.04 with a mean of 55.03. Participants with higher energy levels seem to have more prone to having lung cancer.  
All variables in the dataset are binary except for age, energy level and oxygen saturation.  
50% of participants are males and 50% are females. Lung cancer seems to be equally distributed across genders.  
67% of participants are smokers. Smokers seem to have much more lung cancer than non-smokers.  
60% of participants have discolored fingers. There doesn't seem to be a relationship between finger discoloration and lung cancer.  
54% of participants have mental stress. Mental stress seems to be positively correlated with having lung cancer.  
About half of participants have been exposed to pollution. Being exposed to pollution seems to increase the risk of having lung cancer.  
Only 44% of the participants have a long-term illness. Having a long-term illness seems to be positively correlated with having lung cancer.  
39% of participants have an immune weakness. Having an immune weakness seems to be positively correlated with having lung cancer.  
80% of participants have breathing issues. Having breathing issues seems to be positively correlated with having lung cancer.  
Only 35% of participants consume alcohol.  
70% of participants have throat discomfort. Having throat discomfort seems to be positively correlated with having lung cancer.  
The majority of participants (60%) have experience tightness.  
Only 30% of participants have a family history of lung cancer. Having a family history of lung cancer seems to be positively correlated with having lung cancer.  
Having a family history of smoking seems to be positively correlated with having lung cancer.  
41% of participants have lung cancer.  

According to the correlation coefficients, alcohol consumption is the weakest predictor for having lung cancer. Inversely, smoking is the strongest predictor for having lung cancer.

The logistic regression run with and without give the same results. They give an overall accuracy of 91%.  
The KNN model has an overall accuracy of 88%.  
The SVM model has an overall accuracy of 91%.  