# Shek-s-Guide-Richter-s-Predictor-Guide
This is a guide for you to draw inspiration to kick-start your data science competition journey. This is the Richter's Predictor: Modeling Earthquake Damage hosted by Data Driven.

This is a very basic walkthrough(if you want to call it that) of the competition. I wanted to provide the framework for elementary analysis, preprocessing and modeling. Use this as a bicycle with training wheels. Doing well in competitions is all aboout trying things others havent to get the score you need, so, please use this notebook as a starting point and expand it in anyway you see fit. Here's the description of the compition:

Based on aspects of building location and construction, your goal is to predict the level of damage to buildings caused by the 2015 Gorkha earthquake in Nepal.

Overview:
The data was collected through surveys by Kathmandu Living Labs and the Central Bureau of Statistics, which works under the National Planning Commission Secretariat of Nepal. This survey is one of the largest post-disaster datasets ever collected, containing valuable information on earthquake impacts, household conditions, and socio-economic-demographic statistics.

Problem Description:We're trying to predict the ordinal variable damage_grade, which represents a level of damage to the building that was hit by the earthquake. There are 3 grades of the damage:

1 represents low damage
2 represents a medium amount of damage
3 represents almost complete destruction
(PS: The classes are imbalanced)

Features:
The dataset mainly consists of information on the buildings' structure and their legal ownership. Each row in the dataset represents a specific building in the region that was hit by Gorkha earthquake.

There are 39 columns in this dataset, where the building_id column is a unique and random identifier. The remaining 38 features are described in the section below. Categorical variables have been obfuscated random lowercase ascii characters. The appearance of the same character in distinct columns does not imply the same original value.

We are predicting the level of damage from 1 to 3. The level of damage is an ordinal variable meaning that ordering is important. This can be viewed as a classification or an ordinal regression problem. (Ordinal regression is sometimes described as an problem somewhere in between classification and regression.)

Performance Metric:

To measure the performance of our algorithms, we'll use the F1 score which balances the precision and recall of a classifier. Traditionally, the F1 score is used to evaluate performance on a binary classifier, but since we have three possible labels we will use a variant called the micro averaged F1 score.

Fmicro=2⋅Pmicro⋅RmicroPmicro+Rmicro where, 
Pmicro=∑3k=1TPk∑3k=1(TPk+FPk),  Rmicro=∑3k=1TPk∑3k=1(TPk+FNk)
and TP is True Positive, FP is False Positive, FN is False Negative, and k represents each class in 1,2,3.

Good Luck with the competition! :)
