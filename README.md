# deep-learning-challenge: Charity Funding Predictor

## Overview
The purpose of this analysis is to identify different features of charities that Alphabet Soup has provided funding to over the years and create a model that will predict a successful charity.

#### Data Preprocessing
* What variable(s) are considered the target(s) for your model?
	* "IS_SUCCESSFUL"
* What variable(s) are considered to be the features for your model?
	* APPLICATION_TYPE
	* AFFILIATION
	* CLASSIFICATION
	* USE_CASE
	* ORGANIZATION
	* STATUS
	* INCOME_AMT
	* SPECIAL_CONSIDERATIONS

* What variable(s) are neither targets nor features, and should be removed from the input data?
	* EIN
	* NAME
	* ASK_AMT


#### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
	* I chose to use 200 neurons, 2 layers, and the relu & sigmoid activation functions for my neural network model.  After several changes to the model, I settled on these parameters.  Several other combinations returned a similar accuracy score, and this seemed good enough.  I ran the model with epochs between 10-100, and didn't find any benefits to running the model more than 10 times.  One thing I didn't try was adding more than two layers.  The biggest change, in accuracy score was including the "ASK_AMT" column from the charity dataset, which likely caused significant noise when binary-encoded.
	* I also used keras-tuner to confirm my results, and it too had a similar accuracy score.

* Were you able to achieve the target model performance?
	* No, I was not able to achieve the target model performance.

* What steps did you take to try and increase model performance?
	* Experimenting with the cutoff filters in "Application_Type" and "Classification"
	* Deleted features in the dataframe before binary-encoding
	* Randomly chose a number of neurons between 2-200 for each of the layers
	* Randomly chose an activation between "relu", "tanh", and "sigmoid"


#### Summary
***This deep learning model didn't achieve the target model performance.  The highest score I was able to achieve after many iterations was around 73%.  Supervised Learning models, like Logistic Regression with scaled data or Random Forest with unscaled data might achieve target performance.  I recommend Supervised Learning models in this case because we have the features defined and labeled. 
