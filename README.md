# Heart Failure Prediction Model Comparision
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

![Methodology for the Project](images/MethodologyfortheProject.png)
> Figure 1: Methodology for the Project

## 4. EXPERIMENTS
### 4.1. Exploratory Data Analysis (EDA)
4.1.1. Distribution of categorical data. The visualization of categorical features to check how they have been transformed by the Label Encoder and if the features require scaling for uniform distribution. From the graphs, we can see that the categorial feature data is almost nearly normally distributed.  

4.1.2. Distribution of numerical data. Checking the distribution of numerical features to be able to detect features in need of scaling, visually. Here, we can observe that data distribution for Oldpeak is biased towards the right and data distribution for cholestrol is bimodel i.e two modes. Hence, we can mark them as features that require scaling during feature engineering.  

4.1.3. Distribution of target feature. Here, we have visualized to ensure that we have enough cases for both scenarios i.e. presence of Heart diseases and its absence since the data should have good distribution to be able to predict if person will have a heart failure or not.  

4.1.4. Extra Insights. Plotting the matrix representation for relationship between every feature of the dataset with any other feature. This is primarily done to check the relationship of feature pairs with one another since highly correlated features can reduce the efficiency of the model. Hence, this is an important step in assessing feature importance in the dataset along with pattern recognition and outlier detection. The main purpose of this step in our project was to observe cluster segregation in order to see which features have less correlation, eg: cholesterol vs MaxHR, MaxHR vs OldPeak, bad eg, cholesterol vs restingbp.

### 4.2. Feature Engineering/Selection  
After compiling all the previous observations we did through EDA, we can move towards feature engineering where the first step would be to scale the features that don’t fit their range properly. The Oldpeak feature was normalized because it had a right-skewed distribution. This means that the data was shifted towards higher values, so normalization was used to adjust the data to a more standard distribution. The Age, RestingBP, Cholesterol, and MaxHR features were standardized because they had a normal distribution. This means that the data was evenly spread out around the mean, so standardization was used to scale down the data and make it easier to compare across features.  

Anova and chi-squared tests are used to determine the significance of the relationship between variables and the target variable, from the two tests we conclude to keep out RestingBP feature from model training and testing and consider the remaining features (since it had the lowest score).

Removing the features that don’t have much contribution in the modeling/prediction (RestingBP and RestingECG). After selecting the features, splitting the data as 80% train and 20% test data.

![CategorialDistribution](images/CategorialDistribution.png)
> Figure 2: Distribution of categorical data

![NumericalDistribution](images/NumericalDistribution.png)
> Figure 3: Distribution of numerical data

![TargetFeatureVisualization](images/TargetFeatureVisualization.png)
> Figure 4: Visualization of distribution of target feature i.e. Heart Diease

![MatrixPlot](images/MatrixPlot.png)
> Figure 5: Matrix of plots that shows the relationship between multiple pairs of features in a dataset

![CorrelationMatrix](images/CorrelationMatrix.png)
> Figure 6: Correlation matrix

![TargetCorrelation](images/TargetCorrelation.png)
> Figure 7: Correlation with respect to target variable only

![ChiSquaredTest](images/ChiSquaredTest.png)
> Figure 8: Feature Selection for Categorical Features using Chi-Squared test

![AnovaTest](images/AnovaTest.png)
> Figure 9: Feature Selection for Numerical Features using ANOVA test

### 4.3. Logistic Regression Model  

![Table1](images/Table1.png)
> Table 1: Logistic Regression Accuracies with all features 11

![Table2](images/Table2.png)
> Table 2: Logistic Regression Accuracies after Removing "RestingECG"

![Table3](images/Table3.png)
> Table 3: Logistic Regression Accuracies after Removing "RestingBP"

![Table4](images/Table4.png)
> Table 4: Logistic Regression Accuracies after Removing "RestingECG" and "RestingBP"

![Table5](images/Table5.png)
> Table  5: Logistic Regression Matrix after Removing "RestingECG" and "RestingBP"

![LRegressionCM](images/LRegressionCM.png)
> Figure 10: Logistic Regression Confusion Matrix after Removing "RestingECG" and "RestingBP"

### 4.4. Decision Tree using Random Forest

![Table6](images/Table6.png)
> Table 6: Decision Tree Accuracies with all features 11

![Table7](images/Table7.png)
> Table  7: Decision Tree Accuracies after Removing "RestingECG"

![Table8](images/Table8.png)
> Table 8: Decision Tree Accuracies after Removing "RestingBP"

![Table9](images/Table9.png)
> Table 9: Decision Tree Accuracies after Removing "RestingECG" and "RestingBP"

![Table10](images/Table10.png)
> Table 10: Decision Tree Matrix after Removing "RestingECG" and "RestingBP"

![DTreeCM](images/DTreeCM.png)
> Figure 11: Decision Tree Confusion Matrix after Removing "RestingECG" and "RestingBP"

### 4.5. Naive Bayes  

![Table11](images/Table11.png)
> Table 11: Naive Bayes Accuracies with all features 11

![Table12](images/Table12.png)
> Table 12: Naive Bayes Accuracies after Removing "RestingECG"

![Table13](images/Table13.png)
> Table 13:  Naive Bayes Accuracies after Removing "RestingBP"

![Table14](images/Table14.png)
> Table 14: Naive Bayes Accuracies after Removing "RestingECG" and "RestingBP"

![Table15](images/Table15.png)
> Table 15: Naive Bayes Matrix after Removing "RestingECG" and "RestingBP"

![NaiveBayesCM](images/NaiveBayesCM.png)
> Figure 12: Naive Bayes Confusion Matrix after Removing "RestingECG" and "RestingBP"

### 4.6. K-nearest Neighbors Classifier (k=27)

![Methodology for the Project](images/Table16.png)
> Table 16: K-nearest neighbors classifier Accuracies with all features 11 (k=27)

![Table17](images/Table17.png)
> Table 17: K-nearest neighbors classifier Accuracies after Removing "RestingECG" (k=27)

![Table18](images/Table18.png)
> Table 18: K-nearest neighbors classifier Accuracies after Removing "RestingBP" (k=27)

![Table19](images/Table19.png)
> Table 19: K-nearest neighbors classifier Accuracies after Removing "RestingECG" and "RestingBP" (k=27)

![Table20](images/Table20.png)
> Table 20: K-nearest neighbors classifier Matrix after Removing "RestingECG" and "RestingBP" (k=27)

![knnCM](images/knnCM.png)
> Figure 13: K-nearest neighbors classifier Confusion Matrix after Removing "RestingECG" and "RestingBP" (k=27)

### 4.7. K-nearest Neighbors Classifier (k=10)

![Table21](images/Table21.png)
> Table 21: K-nearest neighbors classifier Accuracies (k=10)

![Table22](images/Table22.png)
> Table 22: K-nearest neighbors classifier Matrix (k=10)

![knnCM10](images/knnCM10.png)
> Figure 14: K-nearest neighbors classifier Confusion Matrix (k=10)

## 5. CONCLUSION  

After seeing averages of all dataset variations, we choose the 4th option as the most accurate dataset. The model with highest accuracy turns out to be Logistic Regression.

![Table23](images/Table23.png)
> Table 23: Average Accuracies

![Table24](images/Table24.png)
> Table Table 24: Perfomance Metrics for the algorithms

## REFERENCES  

1. [n. d.]. How to find the optimal value of K in KNN. https://towardsdatascience.com/how-to-find-the-optimal-value-of-k-in-knn-35d936e554eb Accessed: yyyymm-dd.
2. Scaling Kaggle Competitions using XGBoost (Part 4). https://pyimagesearch.com/2023/01/23/scaling-kaggle-competitions-using-xgboost-part-4/ Accessed: yyyy-mm-dd.
3. S. Alshakranwe and S. Hilal. 2022. A Comparative Study of Heart Disease Prediction Using Classification Techniques. In 2022 International Conference on Decision Aid Sciences and Applications (DASA). IEEE, Chiangrai, Thailand, 11–16. https://doi.org/10.1109/DASA54658.2022.9765241
4. B. Gnaneswar and M. R. E. Jebarani. 2017. A review on prediction and diagnosis of heart failure. In 2017 International Conference on Innovations in Information, Embedded and Communication Systems (ICIIECS). IEEE, Coimbatore, India, 1–3. https://doi.org/10.1109/ICIIECS.2017.8276033
5. Prasanta Kumar Sahoo and Pravalika Jeripothula. 2020. Heart Failure Prediction Using Machine Learning Techniques. (Dec 2020). https://doi.org/10.2139/ssrn.3759562
6. Fede Soriano. [n. d.]. Heart Failure Prediction. https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction Accessed: yyyy-mm-dd.
