# Drug price prediction from open source dataset
## General Description
The datasets can be found in the <a href="https://github.com/databs1/med_price_prediction/tree/master/data">data</a> folder.<br />
Two files one containing the names of the medication another one containing textual data (e.g. number of syringes, units of dosage, labels) with some structured data (e.g. date when the medication was taken out of market, price, route of administration). 

## Problems encountered
After using NLP to extract quantities from the textual data (e.g. number of tablets, dosage). <br />
A lack of data supplied for most of the features left a lot of predictors with null values making the list of most traditional models that can be used small. 

## Solutions
Due to important growth in size of the dataset during feature extraction. Feature engineering and feature selection was needed in order to reduce dimensionality and lower execution time.<br />
Zero Inflated models such as the Zero Inflated Poisson regression yielded poor results.<br />
Transforming some of the quantitative variables into qualitative variables (and also discretizing some) gives better results for Random Forest and XGBoost.<br /> 
The log transformation of the price gives overall better results than the box cox transformation.

## Results
I run cross validation with grid search multiple times to validate the model and find the optimal hyperparameters achieving satisfying results. <br />
Grid search iterations can be found in <a href="https://github.com/databs1/med_price_prediction/tree/master/grid_iterations">grid_iterations</a>. <br />
Best prediction scores were made with Random Forest.<br />
![Predicted vs actual](https://github.com/databs1/med_price_prediction/blob/master/Predicted_vs_actual.png)
