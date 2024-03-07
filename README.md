# Heart-Failure-Prediction
## ABSTRACT  
Cardiovascular diseases (CVDs) are the leading cause of death worldwide, accounting for 17.9 million fatalities each year. The recent coronavirus pandemic has also been linked to causing cardiac problems, further exacerbating the situation. Early detection and management are crucial for individuals with CVDs or at high risk due to risk factors such as hypertension, diabetes, hyperlipidemia, or pre-existing disease. In this project, we aim to develop a predictive model that can identify the presence of heart disease based on a set of attributes or features using machine learning techniques for pattern recognition and accurate predictions.

## 1. INTRODUCTION  
Cardiovascular diseases (CVDs) are responsible for 17.9 million fatalities each year, and the recent coronavirus pandemic has also been linked to causing cardiac problems. As a result of excessive mental stress caused by the coronavirus, heart diseases (HD) are becoming increasingly widespread, particularly in metropolitan
areas. Early detection through common symptoms can be extremely helpful in mitigating the impact of these diseases. In this project, we utilize machine learning techniques for pattern recognition and accurate predictions of heart disease, enabling early diagnosis and intervention.

## 2. PROBLEM DEFINITION  
Early detection and management are crucial for individuals with cardiovascular disease or at high risk due to risk factors such as hypertension, diabetes, hyperlipidemia, or pre-existing disease. 

### 2.1. Aim  
The primary objective of this project is to develop a predictive model that can identify the presence of heart disease based on a set of attributes or features. The model should be able to:  
* Properly analyze the leading causes that contribute to heart failure.
* Classify if a person is prone to heart failure depending on the number of attributes required.
* Achieve high accuracy and generalization in predicting heart disease presence while minimizing false predictions.

## 3. PROPOSED METHOD  
To develop an effective predictive model for heart disease, we have combined five heart datasets and preprocessed the data to obtain a clean and consistent dataset. The final dataset consists of 918 observations with 11 common features, which are a mix of categorical and numerical variables. The features include:  
* Categorical Features: Sex, ChestPainType, RestingECG, ExerciseAngina, ST_Slope, FastingBS
* Numerical Features: Age, RestingBP, Cholesterol, MaxHR, Oldpeak
* Target Feature: 0 for normal heart readings else 1 for the presence of Heart Disease

Four different machine learning models, namely Logistic Regression, Decision Tree, K-Nearest Neighbors, and Naive Bayes, have been trained and evaluated with varying feature sets to determine the most effective approach for heart disease prediction.

