# Drug Price Prediction
## General Description
Drug price prediction from open source dataset, the datasets can be found in  https://github.com/databs1/med_price_prediction/tree/master/data , 
two files one containing the names of the medications and another one containing textual data in one column (e.g. number of syringes, units of dosage, labels)
giving a general description of the contents of the medication. 
The rest of the columns contain structured data such as the date that the medication was taken out of market or the price of the medication.  
 
I used NLP to extract entities with their corresponding values from the textual data. 
Feature engineering and feature selection was required to reduce dimensionality and increase model accuracy.  

## Problems encountered and solutions
The dataset came with its own inherit problems, one of which is a lack of data supplied for most of my features and thus leaving me with a lot of null values in my predictors. 
To overcome this problem I decided to use different Zero Inflated models such as the Zero Inflated Poisson regression yielding poor results.
I decided to go further, transforming some of my quantitative variables into qualitative variables (and also discretizing some) giving Random Forest and XGBoost a try. 

The results improved significantly, I run cross validation with grid search multiple times to validate my model and find the optimal hyperparameters achieving satisfying results. 
