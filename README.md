# KaggleCompetetion_AdvanceHousePricePrediction
This is the code of my Kaggle Competition that i have attempted recently. 

# This repository include
 1. Data Engineering 1: which is the first approach towards preprocessing
 2. Data Engineering 2: this includes the final pre-processing techniques used. 
    - Here first i have checked for correlation using heatmap then removed all the columns  having correlation more than 80%.
    - Then i have handled the categorical & numerical missing values.  
    - Then i have handled the temporal variables.
    - Then i have transformed all the columns which are not distributed in Gaussian curve using log & reciprocal transformation.
    - Then i have handled the outliers by removing all the datapoints lying outside the 3rd standard deviation.
    - Then one hot encoding is performed using pd.get_dummies() method of pandas for all those column having categorical features less than 8 & all those having categorical features more than 8, the top 7 categories are encoded and others are left.
    - Then feature selection is performed using the SelectFromModel library sklearn.model_selection.
    - Finally the data is put into a csv file for prediction.
 3. Model Selection1 : Here i have tested with different ML algorithm to check which perform best with our dataset. Using Cross validation i have found that xgboost works best.
 4. Finally here using the cleaned data & xgboost, predicted value is calculated then using the sample_submission.csv provided by kaggle is used to submit the output.
