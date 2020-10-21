# Drug Price Prediction
## General Description
Drug price prediction from open source dataset, the datasets can be found in  https://github.com/databs1/med_price_prediction/tree/master/data.
two files one containing the names of the medications and another one containing textual data in one column (e.g. number of syringes, units of dosage, labels)
and rest of the columns contain structured data such as the date that the medication was taken out of market or the price of the medication.  
 
## Problems encountered
Lack of data supplied for most of the features leaves a lot of the predictors with null values makes the list of most traditional statistical models that can be used small.
Feature engineering and feature selection is a must to reduce dimensionality and lower execution time.  

## Solutions
Zero Inflated models such as the Zero Inflated Poisson regression yielded poor results.
Transforming some of the quantitative variables into qualitative variables (and also discretizing some) gives better results for Random Forest and XGBoost. 
The log transformed price gives the best results.

## Results 
I run cross validation with grid search multiple times to validate the model and find the optimal hyperparameters achieving satisfying results. GridSearch iterations can be found in grid_iterations.
Best prediction scores were made with Random Forest.
