# Neural Network Charity Analysis

## Overview

For this analysis, I wanted to help Alphabet Soup make better decisions when deciding which organizations to fund with their charitable efforts.
The goal was to use machine learning, specifically neural networks, to classify an organization as if it will either be successful or a failure
if funded by Alphabet Soup.  I was given a data set with their history of funding and outcomes achieved by the organization with the funding.
The data was preprocessed, the models were compiled, trained, and evaluated the data. Lastly, I attempted to optimize the model in order to
provide a better prediction accuracy.

## Results

- Data Preprocessing

	- What variable(s) are considered the target(s) for your model?

	  The only variable for a target was whether it was successful or not.

	- What variable(s) are considered to be the features for your model?

	  Application type, affiliation, classification, use case, organization, and ask amount.

	- What variables(s) are neither targets nor features, and should be removed from the input data?

	  Below is an image of columns I removed, and the reason why I removed them.
	  ![dropped columns](https://github.com/jseverin1984/Neural_Network_Charity_Analysis/blob/main/Resources/dropped_columns.png)

- Compiling, Training, and Evaluating the Model

	- How many neurons, layers, and activation functions did you select for your neural network model, and why?
	  
	  I selected 10 neurons and two hidden layers because I wanted to start low and not over-fit my training data. I chose relu for my hidden
	  layers because of having only two choices, is successful or not successful, and relu goes from 0 to infinity. Then I chose sigmoid for
	  the output layer because its values are from 0 to 1 to match my binary classification.

	- Were you able to achieve the target performance?

	  I did not reach the 75% accuracy score. The below image shows my results.
	  ![first attempt results](https://github.com/jseverin1984/Neural_Network_Charity_Analysis/blob/main/Resources/first_attempt_results.png)

	- What steps did you take to try and increase model performance?
	  
	  The image below describes how I tried to increase model performance.
	  ![third attempt](https://github.com/jseverin1984/Neural_Network_Charity_Analysis/blob/main/Resources/third_attempt.png)

## Summary

I was only able to increase my model performance by .1% after trying two rounds of optimizations.  The neural network model seemed to work pretty
well right away, without any optimization.  When you look at the epoch logs, it reaches a peak accuracy within 10 epochs.  I tried other variations
with more up to five hidden layers and random activation functions, but I couldn't get anything over 73% accuracy. I just don't know enough about
machine learning to optimize with great scrutiny. I looked for outliers in the data, but couldn't find any. I did find a couple columns that could possibly
skew my prediction results, but after taking them out, the bump in performance was negligible. I would recommend trying a random forest classifier. So the
model could build off of weak learners and grow into a better predictive model. You could also combine it with bootstrapping or boosting to help increase
the models accuracy.
	  