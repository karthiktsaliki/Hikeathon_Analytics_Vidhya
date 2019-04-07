# Hikeathon_Analytics_Vidhya

This repo contains my code for Hikeathon contest conducted by Analytics Vidhya.

### Github Link

https://github.com/karthiktsaliki/Innoplexus_NLP_Hackathon

### Libraries used

* Numpy: Numpy is free and open-source Python library used for scientific computing and technical computing.

* pandas: Pandas is a software library written for the Python programming language for data manipulation and analysis.

* sklearn: Machine learning library for the Python programming language. It features for classification and regression.

* lightgbm: For applying gradient boosting non linear model on the data


### Motivation

Social Network Analysis and Link prediction are the most common problems which data scientists has to deal in their career. In this competition hike came up with a problem statement to predict whether a pair of person will encounter in chat given their user characterstics.


### Datasets

Three datasets train and user features contain pair of users and their characterstics have been given along with is_chat variable. Predict the is_chat given the user features in test data.

### Approach

* In this competition I first thought there will not be any information at pair level so built a model aggregating at user level and setting the threshlold of thier number of times they chat as dependent variable secured LB AUC score ~75

* Then with the help of gpu trained lightgbm for the entire train data without param tuning and aggregate both the users features for training and setting dependent variable as it is. Secured an LB score of ~85

* Then I improved the AUC to ~89 by feature engineering and stacking. You can see that in the code in this repo.

### Other Approaches which I had tried:

* Catboost is too slow in my machine as data size is very large unable to pool datasets. 
* Parameter tuning has been neglected as I have no time left, Started this competiton very late but still managed to secure LB **17 Rank** without that.

### Results

I acheived a AUC score ~89 and secured 17th rank in the private leaderboard.
