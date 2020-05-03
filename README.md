This repo details my progress in DrivenData's "Flu Shot Learning: Predict H1N1 and seasonal flu vaccines" challenge. 

The 'data_exploration.ipynb' Jupyter notebook details my EDA process. 

The 'models.ipynb' Jupyter notebook details my model-building attempts.

The link for the challenge is: https://www.drivendata.org/competitions/66/flu-shot-learning/

My approach takes the following steps:
	- Do background research, learn more about the problem at hand.
	- Think of hypotheses to test from the data
	- Perform exploratory data analysis (EDA) to learn more about the data
	- Create visualizations
	- Design, implement, and evaluate ML models
		- Logistic regression (as baseline)
		- Random forest
		- Feedforward neural network
		
	- (possible) - subset the data, run different ML models on different subsets of the data. 
	If this gives promising results (e.g., one model architecture does better on a certain subset of 
	the data than the other models), then we can use an ensemble of various models.
	
	- Work with test set
		- Compare training and test set, check for things such as consistency in class balance, 
		similar proportions of certain values, etc.
		- Run model on test set
		- Get predictions, submit predictions