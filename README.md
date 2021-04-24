# Titanic_kaggle_firstModel
First submission ever on kaggle. overall a good experience but have to try to get more accuracy 
The traintit and testtit csv files contain training and testing data repectively.
Data in the both the file was skewed and had to be cleaned to go further to make any analyzation or finding any correlations between the features.

Step 1: Data Preprocessing (for both train and test data set)

Many feature columns had null values which had to removed either by completely droping them or by fill them with some relevant values.
Features with majority values as null were dropped as it was convineint at that time to do so, though i havent figured whether doing this had any significant effect on my prediction accuracy or model score .
Categorical features with null values were filled with the mode of the entire feature, and mean was used o replace the null values in the non categorical features.


After getting rid of all the Null values , it was time to handle the categorical values. I used get_dummies method of pandas to do this, instead one can use OneHotEncoder or LabelEncoder to do the same. As i was not comfortable and confident in using them i went with the get_dummies.
Doing this i had a clean dataset available to train and test my model

Step 2: Training and Testing the Model 

I was not able to determine any correlation in the features as i was not well versed with data visualization and it was my first time trying to build a model on my own ( hopefully in coming competitions i will be good with it ).But the value to be predicted was discrete it was surely a classifier to be used here. Therfore i randomly decided to use the RandomForestClassifier for training and testing and got a model accuracy of 73% which was significantly less . Therefore i used logistic regression to train and test the dataset and got a model accuracy of 77% which was better than before. 
